# Issue

**Title:** feat(button): add button implementation

## Description

Close #23 .

A draft implementation of add button to the view.

```r
r3dmol() %>%
  m_add_model(data = pdb_1j72, format = "pdb") %>%
  m_zoom_to() %>%
  m_button(
    name = "cartoon",
    label = "Cartoon",
    func = "
      function(){
        viewer.setStyle({cartoon:{}});
        viewer.render();
      }
    "
  )
```

## Initiation
<img width="723" alt="截屏2021-03-11 22 34 25" src="https://user-images.githubusercontent.com/20528423/110795432-2dde3f80-82ba-11eb-9b1e-f065a695d71a.png">

## After Click the `Cartoon` Button
<img width="721" alt="截屏2021-03-11 22 34 35" src="https://user-images.githubusercontent.com/20528423/110795452-346cb700-82ba-11eb-80ff-bf6be0812400.png">

There is only one problem about this feature.

```r
r3dmol() %>%
  m_add_model(data = pdb_1j72, format = "pdb") %>%
  m_zoom_to() %>%
  m_button(
    name = "cartoon",
    label = "Cartoon",
    func = "
      function(){
        viewer.setStyle({cartoon:{}});
        viewer.render();
      }
    "
  ) %>%
  m_button(
    name = "stick",
    label = "Stick",
    func = "
      function(){
        viewer.setStyle({stick:{}});
        viewer.render();
      }
    "
  )
```

<img width="719" alt="截屏2021-03-11 22 38 44" src="https://user-images.githubusercontent.com/20528423/110796340-2e2b0a80-82bb-11eb-946a-145c5cc7ba13.png">

 If you add multiple buttons in the view, the css style of the button position needs to be automatically adjusted according to the number of button, or expose the position argments to the user. 
https://github.com/swsoyee/r3dmol/blob/ed45b5e1fe8a1d84651a1265840cedffd9f19546/inst/htmlwidgets/r3dmol.js#L191

@BradyAJohnston Could you mind helping to finish this implement?

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `135aaf5512e2`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.