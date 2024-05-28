
# Self-Exploring Language Models (SELM)

Code for Self-Exploring Language Models: Active Preference Elicitation for Online Alignment.

Authors: [Shenao Zhang](https://shenao-zhang.github.io), [Donghan Yu](https://plusross.github.io/), [Hiteshi Sharma](https://scholar.google.com/citations?user=-9geUIIAAAAJ), [Ziyi Yang](https://ziyi-yang.github.io/), [Shuohang Wang](https://sites.google.com/site/shuohangsite/), [Hany Hassan Awadalla](https://www.microsoft.com/en-us/research/people/hanyh/), [Zhaoran Wang](https://zhaoranwang.github.io)

![algo.png](figs/algo.png)
![illustration.jpg](figs/illustration.png)

🤗 <a href="https://huggingface.co/collections/ZhangShenao/selm-zephyr-66564a84765632c7cce38b25" target="_blank">Zephyr Models</a>\
🤗 <a href="https://huggingface.co/collections/ZhangShenao/selm-llama-66564aa2024269cbcfc39171" target="_blank">Llama-3 Models</a>\
🤗 <a href="https://huggingface.co/collections/ZhangShenao/selm-phi-66564aa7323470ad86aac21d" target="_blank">Phi-3 Models</a>

## Run the Code

To run the code in this project, first, create a Python virtual environment using e.g. Conda:

```shell
conda create -n selm python=3.10 && conda activate selm
```

You can then install the remaining package dependencies as follows:

```shell
 python -m pip install .
```

You will also need Flash Attention 2 installed, which can be done by running:

```shell
python -m pip install flash-attn==2.3.6 --no-build-isolation
```

Next, log into your Hugging Face account as follows:

```shell
huggingface-cli login
```

Finally, install Git LFS so that you can push models to the Hugging Face Hub:

```shell
sudo apt-get install git-lfs
```

To train SELM on [Meta-Llama-3-8B-Instruct](https://huggingface.co/meta-llama/Meta-Llama-3-8B-Instruct), you need to first apply for the access.

Replace `HF_USERNAME` in run_zephyr.sh and run_llama.sh with your huggingface username.
After the above preparation, run the following commands:

Train SELM on [Zephyr-SFT](https://huggingface.co/HuggingFaceH4/mistral-7b-sft-beta):
```shell
sh run_zephyr.sh
```

Train SELM on [Meta-Llama-3-8B-Instruct](https://huggingface.co/meta-llama/Meta-Llama-3-8B-Instruct):
```shell
sh run_llama.sh
```

Train SELM on [Phi-3-mini-4k-instruct](https://huggingface.co/microsoft/Phi-3-mini-4k-instruct):
```shell
sh run_phi.sh
```


## Acknowledgement
This repo is built upon [The Alignment Handbook](https://github.com/huggingface/alignment-handbook). We thank the authors for their great work. 