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
+--------------------------------+
|   LLM Aware (Vision + Sim.)    |
+--------------------------------+
                 |
                 v
+--------------------------------+
|      Qwen-VL to Parse Image     |
+--------------------------------+
                 |
                 v
+--------------------------------+
| Display 10 Images Selected by  |
|      User or Top 3 Ranked      |
|               (UI)             |
+--------------------------------+
                 |
                 v
+--------------------------------+
|      Images + Prompt ---->     |
|   Flux.1 for Content Dev       |
+--------------------------------+
                 |
                 v
+--------------------------------+
|    Result Displayed on UI      |
+--------------------------------+
