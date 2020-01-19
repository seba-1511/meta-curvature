# Meta-Curvature 

This repo contains code for reproducing the experimental results (sinusoid regression and Omniglot classificaiont) in the paper, [Meta-Curvature (Park et al., NeurIPS 2019)](https://arxiv.org/abs/1902.03356). This is basd on [original MAML implementation](https://github.com/cbfinn/maml).


### Usage
For sinuosoid experiments,
```bash
python main.py --datasource=sinusoid --logdir=logs/sine/ --metatrain_iterations=70000 --norm=None --update_batch_size=10 --mc=True
```
