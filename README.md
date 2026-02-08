# Deconstructing Pre-training: Knowledge Attribution in MoE and Dense Models

Code for the paper **"Deconstructing Pre-training: Knowledge Attribution Analysis in MoE and Dense Models"** (arXiv:2601.08383, accepted by AAAI 2026).

This repository extends neuron-level attribution analysis from dense models to **Mixture-of-Experts (MoE)** models, and compares knowledge acquisition dynamics between MoE and dense architectures.

Paper: https://arxiv.org/abs/2601.08383


## Environment Setup

```bash
conda env create -f environment.yml
conda activate attribution
```

## Running Code

Before running notebooks, replace the `transformers` modeling files in your environment with the modified files in this repository.

1. Locate your Python environment path, e.g.:
`.../envs/<YOUR_ENV>/lib/python3.8/site-packages/transformers/models/olmo/modeling_olmo.py`
`.../envs/<YOUR_ENV>/lib/python3.8/site-packages/transformers/models/olmoe/modeling_olmoe.py`

2. Backup original files and replace them with:
`modeling_olmo.py`
`modeling_olmoe.py`

3. Run:
`OLMo_view_knowledge.ipynb` (Dense OLMo)
`OLMoE_view_knowledge.ipynb` (MoE OLMoE)

4. In notebooks, set:
`modelname = "your own model dir"`
output directory variables (currently placeholder `Output_Dir`) to your target path.


## Citation

```bibtex
@article{wang2026deconstructing,
  title={Deconstructing Pre-training: Knowledge Attribution Analysis in MoE and Dense Models},
  author={Wang, Bo and Li, Junzhuo and Chen, Hong and Chu, Yuanlin and Fan, Yuxuan and Hu, Xuming},
  journal={arXiv preprint arXiv:2601.08383},
  year={2026}
}
```