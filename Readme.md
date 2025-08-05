AI Montage Creator

Given selected images or collections, create a montage using a computer vision model, that selects the optimal images, according to a written prompt instruction, and according to the mood of the montage, ordering images optimally (to weave a narrative) or randomly, and adding a piece of music according to the mood and the prompt.

Flow

User selects n images from their meta collection

User instructs Wizzy/the system: "Create a montage for my trip to the Rockies. Add exciting music. I want the montage to be…..."

The system finds the optimal images using a multimodal model, that can have high coherence to the user’s instructions (so a purely vision model won’t be good enough), stitches them together, retrieves a piece of music (based on description of the piece and the prompts instructions), adds it to the collection and generates the montage collection.



https://huggingface.co/Qwen/Qwen-Image

https://huggingface.co/openai/gpt-oss-120b

```
+--------------------------------+
|    LLM CHAT Interface          |
|   low latency model GPT OSS    |
+--------------------------------+
                 |
                 v
+--------------------------------------------------+
|   Generate multiple search queries from prompt   |
|    Retrieve images in parallel   [ColQwen Omni]  |      
+--------------------------------------------------+
                 |
                 v
+--------------------------------------------------+
|      ColQwen Omni to Parse Image                 |
|    (enhance image if needed Qwen_Image)          |
|     LLM will choose music from library as well   |
+--------------------------------------------------+
                 |
                 v
+------------------------------------------+
|    Combine all into a compressed mp4     |
+------------------------------------------+
