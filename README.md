# ML From Scratch

Re-implementing landmark machine learning papers from first principles, to understand what the libraries actually do.

Each project has: the paper, my own implementation, a reproduced result, and a short reflection on what I learned and where I deviated from the paper.

## Projects

| # | Project | Paper | Stack | Target | Status |
|---|---------|-------|-------|--------|--------|
| 01 | [MLP + Backpropagation](01_mlp_backprop/) | Rumelhart, Hinton, Williams (1986) | NumPy | >=97% MNIST | Not started |
| 02 | [Autograd Engine](02_autograd/) | micrograd-style | Python | Gradients match PyTorch | Not started |
| 03 | [CNN & ResNet](03_cnn_resnet/) | AlexNet (2012), ResNet (2015) | PyTorch | ResNet > plain CNN on CIFAR-10 | Not started |
| 04 | [Transformer / mini-GPT](04_transformer/) | Vaswani et al. (2017) | PyTorch | Coherent text on tiny Shakespeare | Not started |
| 05 | [Extension](05_extension/) | VAE / DQN / DDPM (TBD) | PyTorch | TBD | Not started |

## Repository structure

```
ml-from-scratch/
├── README.md
├── TODO.md
├── requirements.txt
├── .gitignore
├── common/              # shared utilities: data loading, plotting, seeding
├── 01_mlp_backprop/
│   ├── README.md        # paper summary, method, results, reflection
│   ├── src/
│   ├── tests/           # e.g. gradient checking
│   └── results/         # plots, logs, final metrics
├── 02_autograd/
├── 03_cnn_resnet/
├── 04_transformer/
├── 05_extension/
└── notes/               # math derivations, reading notes
```

## Setup

```bash
git clone <repo-url>
cd ml-from-scratch
python -m venv .venv
source .venv/bin/activate      # Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

Each project folder has its own README with run instructions.

## Principles

- **Read the paper first**, derive the math on paper, then code.
- **No reference implementations** until I am stuck.
- **Verify before scaling:** gradient checks, and overfit a tiny batch before training for real.
- **Reproducible:** fixed seeds, logged hyperparameters, saved results.
- **Document honestly:** include what did not work and why.

## Per-project README template

1. Paper and one-paragraph summary
2. Method (key equations in my own words)
3. Implementation notes and design decisions
4. Results (table + plots) vs. the paper
5. Ablations / experiments
6. What I learned and what surprised me

## Results summary

_Fill in as projects finish._

| Project | Metric | Mine | Paper / baseline |
|---------|--------|------|------------------|
| 01 MLP | MNIST test accuracy | | |
| 02 Autograd | Max gradient diff vs PyTorch | | |
| 03 ResNet | CIFAR-10 test accuracy | | |
| 04 GPT | Validation loss | | |

## Resources

- Karpathy, *Neural Networks: Zero to Hero*
- *Dive into Deep Learning* (d2l.ai)
- 3Blue1Brown, Neural Networks series
- Papers With Code

## License

MIT