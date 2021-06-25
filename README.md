# Basic-UI-for-GPT-J-6B-with-low-vram
A repository to run GPT-J-6B on low vram systems by using both ram, vram and pinned memory.<br>

## How to run : 
Use - pip install git+https://github.com/finetuneanon/transformers@gpt-neo-localattention3 <br>
Use the link - (upload in progress)  to dowload the model that has been saved as described here - https://github.com/arrmansa/saving-and-loading-large-models-pytorch <br>

## Timing
### system - <br>
16 gb ddr4 ram . 1070 8gb gpu. <br> 
23 blocks on ram (ram_blocks = 23) out of which 18 are on shared/pinned memory (max_shared_ram_blocks = 18).<br>

### timing - <br>
single run of the model(inputs) takes 6.5 seconds.<br>
35 seconds to generate 25 tokens at 2000 context. (1.4 seconds/token)<br>
