# LLM Lora Fine Tuning
介紹大型語言模型的 LoRA 微調技術，涵蓋理論基礎、訓練流程、Tokenizer 原理與實作 Lab，幫助學員實際微調出能創作歌詞的 LLM 模型。

- [PPT](https://github.com/SDPM-lab/llm-lora-fine-tuning-course/blob/main/docs/presentations/2025%E6%99%BA%E6%85%A7%E5%89%B5%E6%96%B0%E9%97%9C%E9%8D%B5%E4%BA%BA%E6%89%8D-%E5%A4%A7%E5%9E%8B%E8%AA%9E%E8%A8%80%E6%A8%A1%E5%9E%8BLoRA%E5%BE%AE%E8%AA%BF%E8%A8%93%E7%B7%B4.pptx)
- [Example Code](https://github.com/SDPM-lab/llm-lora-fine-tuning-course/blob/main/lyrics-llm-lora-demo.ipynb)

## Setup
- Python: 3.11

### Install
```bash
pip install torch transformers peft gradio tqdm matplotlib
```

### Download Based Model
```bash
pip install -U "huggingface_hub[cli]"

huggingface-cli login --token <your-huggingface-token>

SAVE_PATH="hf_models/gemma-3-1b-it"
MODEL_NAME="google/gemma-3-1b-it"
huggingface-cli download ${MODEL_NAME} --local-dir ${SAVE_PATH}
```