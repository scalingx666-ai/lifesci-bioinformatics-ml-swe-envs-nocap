# Issue

**Title:** fix: grid layout dose not update in Shiny app

## Description

Example code to test the behavior.
```r
library(shiny)
library(r3dmol)

ui <- fluidPage(
  sidebarLayout(
    sidebarPanel(
      selectInput("selected_id", "Choose a PDB ID:", choices=c("3G5X","7A2A","5IJ5")),
    ),
    mainPanel(
      ## Choose multi or individual, but not both at the same time
      r3dmolOutput(outputId = "structure_multi"),
      r3dmolOutput(outputId = "structure_individual"),
    )
  )
)

server <- function(input, output, session) {
  
  output$structure_individual <- renderR3dmol({
    r3dmol() %>%
      m_add_model(data = m_fetch_pdb(input$selected_id)) %>%
      m_zoom_to() %>%
      m_set_style(style = m_style_cartoon(color = "spectrum"))
  })
  
  output$structure_multi <- renderR3dmol({
    m1 <- r3dmol() %>%
      m_add_model(data = m_fetch_pdb(input$selected_id)) %>%
      m_zoom_to()
    
    m2 <- m1 %>%
      m_set_style(style = m_style_cartoon(color = "spectrum"))
    
    m3 <- m1 %>%
      m_set_style(style = m_style_stick())
    
    m4 <- m1 %>%
      m_set_style(style = m_style_sphere())
    
    grid <- m_grid(
      viewer = list(m1, m2, m3, m4),
      control_all = TRUE,
      viewer_config = m_viewer_spec(
        backgroundColor = "black"
      )
    )
    grid$elementId <- NULL # suppress the `Shiny doesn't use them` warning
    grid
  })
}

shinyApp(ui, server)
```

<img width="1185" alt="2021-09-17 00 41 32" src="https://user-images.githubusercontent.com/20528423/133643094-8b56e455-3074-42cb-8b65-626b1563d94f.png">
<img width="1186" alt="2021-09-17 00 41 44" src="https://user-images.githubusercontent.com/20528423/133643111-ead406ca-85b7-437d-957e-c3489e42aa2e.png">

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `ac1144705722`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.