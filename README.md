# RL-PLUS: Countering Capability Boundary Collapse of LLMs in Reinforcement Learning with Hybrid-policy Optimization

[![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2508.00222) [![Github](https://img.shields.io/badge/RL--PLUS-000000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/YihongDong/RL-PLUS) 

## 🔧 Usage

### Training RL-PLUS

Run the main RL-PLUS training script:

```bash
cd exp_scripts
bash train_RL-PLUS.sh
```

### Installation

```bash
# Create conda environment
conda create -n rlplus python=3.10
conda activate rlplus

# Install dependencies
cd rl_plus
pip install -r requirements.txt
pip install -e .

# Install veRL framework
cd verl
pip install -e .
```

**Flash Attention Installation (Recommended):**
If you encounter issues with flash-attn, install from the official release:
```bash
wget https://github.com/Dao-AILab/flash-attention/releases/download/v2.7.3/flash_attn-2.7.3+cu12torch2.4cxx11abiFALSE-cp310-cp310-linux_x86_64.whl
pip install flash_attn-2.7.3+cu12torch2.4cxx11abiFALSE-cp310-cp310-linux_x86_64.whl
```

### Repository Structure

This repository includes:

- **rl_plus:** Our main code changes are in `rl_plus/verl/verl/recipe/`.
- **data:** Data and code for training and evaluating RL-PLUS models.
- **exp_scripts:** Example scripts to train RL-PLUS.
- **eval_scripts:** Evaluation scripts on math and out-of-distribution benchmarks.

RL-PLUS is built on top of the GRPO framework and supports plug-and-play integration with sft data.


## 🌻 Acknowledgement

RL-PLUS leverages verl, deepscaler, LUFFY, and simpleRL-reason and uses vLLM for efficient inference. We evaluate its mathematical reasoning capabilities with Math-Verify. We appreciate their high-quality code and outstanding work.  Moreover, we would like to thank the open-source community for their invaluable contributions of datasets and foundational models, including NuminaMath, OpenR1-Math-220k, Qwen2.5-Math, and the DeepSeek-R1 model.


## 🎈 Citation

If you find RL-PLUS useful for your research, please cite our paper:

```bibtex
@article{dong2025rlplus,
  title={RL-PLUS: Countering Capability Boundary Collapse of LLMs in Reinforcement Learning with Hybrid-policy Optimization}, 
  author={Dong, Yihong and Jiang, Xue and Tao, Yongding and Liu, Huanyu and Zhang, Kechi and Mou, Lili and Cao, Rongyu and Ma, Yingwei and Chen, Jue and Li, Binhua and Jin, Zhi and Huang, Fei and Li, Yongbin and Li, Ge},
  journal={arXiv preprint arXiv:2508.00222},
  year={2025}
}
```
