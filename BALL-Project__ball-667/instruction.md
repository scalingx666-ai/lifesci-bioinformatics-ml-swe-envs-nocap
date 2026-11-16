# Issue

**Title:** fix(ufg-06/bottomdrawer): drive maximumHeight from current height and resizeDocks

## Description

## Summary

Fixes UFG-06 — clicking the collapsed `Logs ▾` strip at the bottom of the BALLView window did not expand the drawer to its 240 px state. Drawer stayed at the 24 px collapsed strip.

## Root cause

`BottomDrawer::setExpanded(true)` called `setMaximumHeight(kExpandedHeight)` (240) BEFORE `animateTo()`, and `animateTo()` read `maximumHeight()` as the animation start value — so the `QPropertyAnimation` ran 240→240 (zero delta) and Qt's `QMainWindow` dock-area layout never received a relayout cue. The chevron `clicked` → `toggle()` → `setExpanded(true)` signal chain was wired correctly; `expanded_` flipped to `true` and `body_->setVisible(true)` was called, but the bottom dock row stayed pinned at 24 px so the body had zero visible pixels.

## Fix

Three coordinated edits in `source/VIEW/WIDGETS/bottomDrawer.C` (+40/-5):

1. `animateTo()` now drives `maximumHeight` from the current rendered `height()` (not the cap), so the animation start always matches what the user sees.
2. `setExpanded()` no longer pre-sets `maximumHeight` to the target before animating; `animateTo()` lifts the cap to `max(currentHeight, targetHeight)` so the animation has room to grow into without short-circuiting itself.
3. `animateTo()` explicitly calls `QMainWindow::resizeDocks({this}, {targetHeight}, Qt::Vertical)` — animating `maximumHeight` alone is not enough for `QDockWidget` because `QMainWindow` caches the previous row geometry and will not re-grow it without an explicit hint.

## Test plan

- [x] macOS-arm64 incremental rebuild — `cmake --build build -j8 --target VIEW` and `--target BALLView` both clean, no new warnings on `bottomDrawer.C`.
- [ ] CI 3-OS matrix green.
- [ ] User runs v1.7.0-rc2 build — chevron click on the `Logs ▾` strip animates the dock open over 200 ms, revealing the Log / Files tabs.

Refs: UFG-06 in `.planning/v1.7-USER-FEEDBACK-GATE.md` (now marked ✅ FIXED for rc2).

🤖 Generated with [Claude Code](https://claude.com/claude-code)

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `94a6873d89e7`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.