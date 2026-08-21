
Dynamic-LoRA-Inference-Server

                  Client Request
                        │
                        ▼
                 REST / OpenAI API
                        │
                +-------+--------+
                |  Request Router |
                +-------+--------+
                        │
          Adapter ID: "finance-lora"
                        │
                        ▼
             Adapter Cache Manager
          (GPU Cache + CPU Cache + Disk)
                        │
         Loads adapter if not already cached
                        │
                        ▼
        Base LLM (loaded once on GPU)
                 +
        Selected LoRA Adapter
                        │
                        ▼
               Generate Response
