# Basic-UI-for-GPT-J-6B-with-low-vram
A repository to run GPT-J-6B on low vram systems by using both ram, vram and pinned memory.<br>

## There seem to be some issues with the weights in the drive link. There seems to be some performance loss, most likely because of poor fp16 conversion.

## How to run : 
Use - pip install git+https://github.com/finetuneanon/transformers@gpt-neo-localattention3 <br>
Use the link - https://drive.google.com/file/d/1tboTvohQifN6f1JiSV8hnciyNKvj9pvm/view?usp=sharing  to dowload the model that has been saved as described here - https://github.com/arrmansa/saving-and-loading-large-models-pytorch <br>

## Timing (2000 token context)
### 1
#### system - <br>
16 gb ddr4 ram . 1070 8gb gpu. <br> 
23 blocks on ram (ram_blocks = 23) out of which 18 are on shared/pinned memory (max_shared_ram_blocks = 18).<br>

#### timing - <br>
single run of the model(inputs) takes 6.5 seconds.<br>
35 seconds to generate 25 tokens at 2000 context. (1.4 seconds/token)<br>

### 2
#### system - <br>
16 gb ddr4 ram . 1060 6gb gpu. <br> 
26 blocks on ram (ram_blocks = 26) out of which 18 are on shared/pinned memory (max_shared_ram_blocks = 18).<br>

#### timing - <br>
40 seconds to generate 25 tokens at 2000 context. (1.6 seconds/token)<br>
