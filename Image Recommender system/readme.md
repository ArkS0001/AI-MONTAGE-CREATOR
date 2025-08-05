Simple image rec. sys.

Given 200 reference artworks/photos, out of which 10 have been liked/used as reference, in batches of 5, suggest/recommend/curate most likely set of images a user would like

A llama model or any similarty model to check for like/dislikes

https://huggingface.co/vidore/colqwen-omni-v0.1

https://huggingface.co/spaces/black-forest-labs/FLUX.1-Kontext-Dev


```
+--------------------------------+
|         Image Dataset          |
+--------------------------------+
                 |
                 v
+------------------------------------------------------------------------+
|   LLM Aware (Vision model + Similarity score for like and dislike )    |
+------------------------------------------------------------------------+
                 |
                 v
+--------------------------------------+
|      ColQwen Omni to Parse Image     |
+--------------------------------------+
                 |
                 v
+-------------------------------------+
| Display 10 Images Selected by User  |
|      or Top 3 Ranked                |
|               (UI)                  |
+-------------------------------------+
                 |
                 v
+-------------------------------------+
|      Images + Prompt ---> Images    |
|       Flux.1 Kontext Dev            |
+-------------------------------------+
                 |
                 v
+--------------------------------+
|    Result Displayed on UI      |
+--------------------------------+
```
```mermaid
graph TD
    A["<div style='padding:10px;'><b>Image Dataset</b></div>"] --> B;
    B["<div style='padding:10px;'><b>LLM Aware</b><br/>(Vision model + Similarity score for like and dislike)</div>"] --> C;
    C["<div style='padding:10px;'><b>ColQwen Omni to Parse Image</b></div>"] --> D;
    D{"<div style='padding:10px;'><b>Display 10 Images Selected by User</b><br/>or Top 3 Ranked<br/>(UI)</div>"} --> E;
    E["<div style='padding:10px;'><b>Images + Prompt ⟶ Images</b><br/>(Flux.1 Kontext Dev)</div>"] --> F;
    F["<div style='padding:10px;'><b>Result Displayed on UI</b></div>"];

    %% Styling
    style A fill:#f9f9f9,stroke:#333,stroke-width:2px
    style B fill:#e6fffa,stroke:#333,stroke-width:2px
    style C fill:#e6fffa,stroke:#333,stroke-width:2px
    style D fill:#fff0e6,stroke:#333,stroke-width:2px
    style E fill:#e6faff,stroke:#333,stroke-width:2px
    style F fill:#f9f9f9,stroke:#333,stroke-width:2px
