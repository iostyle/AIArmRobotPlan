# Model Plan

## 1. 初识HuggingFace
https://huggingface.co
## 2. 环境搭建
### 1. 依赖安装
- UV
```shell
brew install uv
```
- Create a virtual environment to install Transformers in.
```
uv venv .env
source .env/bin/activate
```
- Python

Install Transformers with the following command.
```
uv pip install transformers
```
For GPU acceleration, install the appropriate CUDA drivers for PyTorch.

Run the command below to check if your system detects an NVIDIA GPU.
```
nvidia-smi
```
To install a CPU-only version of Transformers, run the following command.

```
uv pip install torch --index-url https://download.pytorch.org/whl/cpu
uv pip install transformers
```
Test whether the install was successful with the following command. It should return a label and score for the provided text.
```
python -c "from transformers import pipeline; print(pipeline('sentiment-analysis')('hugging face is the best'))"
[{'label': 'POSITIVE', 'score': 0.9998704791069031}]
```

## 3. 离线模型运行

## 4. LoRA微调

## 5. 模型蒸馏