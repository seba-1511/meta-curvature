# Meta-Curvature 

This repo contains code for reproducing the experimental results (sinusoid regression and Omniglot classification) in the paper, [Meta-Curvature (Park et al., NeurIPS 2019)](https://arxiv.org/abs/1902.03356). This is basd on [original MAML implementation](https://github.com/cbfinn/maml).


### Usage
For sinuosoid experiments,
```bash
python main.py --datasource=sinusoid --logdir=logs/sine/ --metatrain_iterations=70000 --norm=None --update_batch_size=10 --mc=True
```

For Omniglot experiments,
```bash
# 5-way 1-shot
python main.py --datasource=omniglot --metatrain_iterations=60000 --meta_batch_size=32 --update_batch_size=1 --num_classes=5 --update_lr=0.4 --num_updates=1 --logdir=logs/omniglot5way/ --mc=True
```

```bash
# 5-way 5-shot
python main.py --datasource=omniglot --metatrain_iterations=60000 --meta_batch_size=32 --update_batch_size=5 --num_classes=5 --update_lr=0.4 --num_updates=1 --logdir=logs/omniglot5way/ --mc=True
```

```bash
# 20-way 1-shot
python main.py --datasource=omniglot --metatrain_iterations=60000 --meta_batch_size=32 --update_batch_size=1 --num_classes=20 --update_lr=0.4 --num_updates=1 --logdir=logs/omniglot20way/ --mc=True
```

```bash
# 20-way 5-shot
python main.py --datasource=omniglot --metatrain_iterations=60000 --meta_batch_size=32 --update_batch_size=5 --num_classes=20 --update_lr=0.4 --num_updates=1 --logdir=logs/omniglot20way/ --mc=True
```
