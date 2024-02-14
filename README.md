# Official repo for StableLLaVA
**Enhanced Visual Instruction Tuning with Synthesized Image-Dialogue Data**

**This repository offers a collection of AI-generated datasets specifically tailored for visual instruction tuning.**

## Install

```
conda create -n stablellava python=3.10 -y
conda activate stablellava
pip install --upgrade pip 
pip install -e .
```

## Evaluation
### MMBench
1. Download mmbench [dev/test set](https://github.com/open-compass/MMBench), then put it under ```./playground/data/eval/mmbench ```

2. Set model_path and model_base in ``` scripts/v1_5/eval/mmbench.sh ```
   
   For model_path, you can download from [google drive](https://drive.google.com/file/d/1GgI4SDzWLj_16baKHzYyoDa-9zBdVrsk/view?usp=drive_link)
   
   For model_base, we adopt vicuna-13b-v1.5, and you can download from [huggingface](https://huggingface.co/lmsys/vicuna-13b-v1.5)

   Test with single-gpu

   ``` CUDA_VISIBLE_DEVICES=0 bash scripts/v1.5/eval/mmbench.sh ```
   
4. Submit the results under ```./playground/data/eval/mmbench/answers_upload/ ``` to [MMBench](https://mmbench.opencompass.org.cn/home)
   

