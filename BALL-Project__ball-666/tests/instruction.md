# Issue

**Title:** fix(ufg-02): macOS rendering glitches for v1.7.0-rc2

## Description

## Summary

Four fixes addressing UFG-02 (macOS rendering glitches in v1.7.0-rc1):

- **QSS scoping** (`8b1ff967cb` → `26380badca`) — scope `QPushButton`/`QToolButton` to `QMainWindow ...` descendants and `QMenuBar` to `QMainWindow > QMenuBar`, so dialogs keep QMacStyle Aqua chrome and the in-window menubar stops fighting Cocoa's global menu.
- **Unified toolbar + native-siblings caveat** (`5cb1a2d353` → `f6cc4d094d`) — add `setUnifiedTitleAndToolBarOnMac(true)` in `Mainframe::show()` under `Q_OS_MACOS` (Handover §09-cross-platform.md row 30) + document the Qt 6 / Apple Silicon GL-flicker caveat on `AA_DontCreateNativeWidgetSiblings` (kept because Qt WebEngine still requires it via HTMLPage/HTMLView/EXTENSIONS).
- **Stale comment** (`ca8aeab32f` → `25c74c3fe2`) — drop `BALL_UI_V2` reference from `main.C` ThemeManager init comment (flag removed in 999.48 §8.7).
- **Status doc** (`50c2bbc9ad` → `16eafc5371`) — mark UFG-02 FIXED in `.planning/v1.7-USER-FEEDBACK-GATE.md`.

UFG-05 fix at `sectionHeader.C:52` (`WA_OpaquePaintEvent`) verified still in place + not regressed.

## Test plan

- [x] macOS-arm64 local smoke build green (`make -j8 BALLView` — built `libVIEW.dylib` + `BALLView.app` cleanly with the modified `theme-neutral.qss`, `mainframe.C`, `main.C`)
- [x] Bare-selector grep returns only intentional residual rules (`QMainWindow`, `QMenu`, `QStatusBar`, `QGroupBox`, `QLineEdit`, `QComboBox` — see commit rationale)
- [ ] CI: 3-OS build + render-smoke (this PR)
- [ ] Visual smoke: open Preferences / About / MolecularFileDialog on macOS and confirm native Aqua chrome restored
- [ ] Visual smoke: toolbar renders as unified NSToolbar (no drag handles, no separate strip)

🤖 Generated with [Claude Code](https://claude.com/claude-code)

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `94a6873d89e7`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.