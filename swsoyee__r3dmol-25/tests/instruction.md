# Issue

**Title:** feat(gridView): implement feature

## Description

A dirty solution, but it works.

```r
library(r3dmol)

m1 <- r3dmol() %>%
  m_add_model(data = pdb_6zsl, format = "pdb") %>%
  m_zoom_to()

m2 <- m1 %>%
  m_set_style(style = m_style_cartoon(color = "spectrum"))

m3 <- m1 %>%
  m_set_style(style = m_style_stick())

m4 <- m1 %>%
  m_set_style(style = m_style_sphere())

m_grid(
  viewer = list(m1, m2, m3, m4),
  configs = list(rows = 2, cols = 2, control_all = TRUE),
  viewer_config = list(backgroundColor = "black")
)
```

<img width="727" alt="截屏2021-03-07 23 47 09" src="https://user-images.githubusercontent.com/20528423/110243841-7686b780-7f9f-11eb-9dfe-d048309b09a2.png">

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `27a5ebbf9652`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.