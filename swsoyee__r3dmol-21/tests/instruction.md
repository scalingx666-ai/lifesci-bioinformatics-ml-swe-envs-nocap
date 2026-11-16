# Issue

**Title:** Added m_quick_look() funciton

## Description

For convenience, I have added a new `m_quick_look()`. I mainly made it to quickly look at `{bio3d}` objects, but it can also just take a PDB ID string and will fetch the structure file.

```r
# from a {bio3d} object
pdb <- bio3d::read.pdb("4ozs")

pdb %>%
  m_quick_look()

# just using string
"4ozs" %>%
  m_quick_look()
```

I included some useful presets that can quickly be tweaked to get some different looks.

```r
highlight = m_sel(),
zoom = TRUE,
spin = FALSE,
nomouse = FALSE,
ribbon = FALSE,
outline = TRUE,
backgroundColor = "white"
```

`ribbon`, `outline` and `backgroundColor` are straightforward aesthetic options.
`nomouse` and `spin` are for enabling / disabling mouse input and spinning.
`highlight` takes an `m_sel()` selection and adds "ball-n-stick" representation to the selection to highlight a particular selection. If `zoom == TRUE` then the viewer is centered around the `highlight` selection.


The function can be chained with additional functions to further customise the view viewer as well. 

```r
pdb %>%
  m_quick_look() %>%
  m_add_surface()
```

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `f902283f3bee`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.