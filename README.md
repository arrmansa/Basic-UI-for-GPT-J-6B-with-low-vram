# Basic-UI-for-GPT-J-6B-with-low-vram
A repository to run GPT-J-6B on low vram systems by using both ram, vram and pinned memory.

## How to run : 
Replace modeling_gpt_neo.py (wherever your environment's transformers\models\gpt_neo\modeling_gpt_neo.py is stored) with the one in this repo. <br>
Use the link - https://drive.google.com/file/d/19nmS8ToTkuQdKZnxZWi4HBwQzRqp5xok/view?usp=sharing to dowload the model that has been saved as described here - https://github.com/arrmansa/saving-and-loading-large-models-pytorch

# Timing
system - <br>
16 gb ddr4 ram . 1070 8gb gpu. <br> 
24 blocks on ram (ram_blocks = 24) out of which 18 are on shared/pinned memory (max_shared_ram_blocks = 18).<br>

timing - 
single run of the model(inputs) takes 7.5 seconds.<br>
42 seconds to generate 25 tokens at 2000 context. (1.7 seconds/token)<br>
