# TODO

## Phase 0: Setup and Python/NumPy (week 0)

- [x] Create GitHub repo `ml-from-scratch`
- [x] Add README, TODO, `.gitignore` (`.venv/`, `data/`, `*.pt`, `__pycache__/`), MIT license
- [x] Create folder structure (`common/`, `01_...` to `05_...`, `notes/`)
- [ ] Set up venv and `requirements.txt` (numpy, matplotlib, jupyter; torch later)
- [ ] Python crash course: classes and dunder methods, comprehensions, slicing
- [ ] NumPy drills: shapes, `@`, `axis`, broadcasting, vectorizing a loop
- [ ] Write `common/` helpers: seeding, MNIST loader, plotting
- [ ] First commit and push

## Phase 1: MLP + Backprop (weeks 1-2)

- [ ] Read the paper (abstract, figures, method)
- [ ] Derive forward pass and gradients on paper (chain rule, per layer); save in `notes/`
- [ ] Write spec: layers, parameter shapes, input/output shapes per function
- [ ] Implement initialization, forward pass, loss (softmax + cross-entropy)
- [ ] Implement backward pass
- [ ] **Gradient check** against numerical gradients
- [ ] Overfit a tiny batch (loss -> ~0)
- [ ] Mini-batch SGD training loop on MNIST
- [ ] Experiments: learning rate, hidden size, init scheme, activation
- [ ] Plot loss and accuracy curves; reach >=97% test accuracy
- [ ] Project README with results and reflection; tag `v0.1-mlp`

## Phase 2: Autograd Engine (week 3)

- [ ] Watch/read Karpathy's micrograd lecture in stages, pausing to predict next step
- [ ] Design a `Value` class: data, grad, parents, operation
- [ ] Implement operators via dunder methods (+, *, **, neg, sub, div)
- [ ] Implement activations (tanh/ReLU) and exp/log if needed
- [ ] Implement topological sort and `backward()`
- [ ] Test: compare gradients to PyTorch on several expressions
- [ ] Build a small MLP on top and train on a toy dataset
- [ ] Reflect: how does this differ from Project 1's manual backprop?
- [ ] Project README; tag `v0.2-autograd`

## Phase 3: CNN and ResNet (weeks 4-5)

- [ ] Learn PyTorch basics: tensors, `nn.Module`, optimizer, training loop, device handling
- [ ] Read AlexNet and ResNet papers; note the degradation problem
- [ ] Implement a plain CNN; train on CIFAR-10; baseline accuracy
- [ ] Add data augmentation, BatchNorm, Dropout; measure each effect
- [ ] Implement residual blocks and a small ResNet
- [ ] **Ablation:** same depth with and without skip connections
- [ ] Compare training curves at increasing depth
- [ ] Project README with plots; tag `v0.3-cnn-resnet`

## Phase 4: Transformer / mini-GPT (weeks 6-8)

- [ ] Read "Attention Is All You Need"; derive scaled dot-product attention by hand
- [ ] Track tensor shapes through every step on paper first
- [ ] Implement tokenizer (character level) and data pipeline for tiny Shakespeare
- [ ] Implement single-head causal self-attention
- [ ] Extend to multi-head attention
- [ ] Add positional encoding, residuals, LayerNorm, feed-forward block
- [ ] Assemble decoder-only model and training loop
- [ ] Overfit a tiny batch, then train properly; track train/val loss
- [ ] Generate text; experiment with temperature and context length
- [ ] Project README with samples and loss curves; tag `v0.4-transformer`

## Phase 5: Extension (weeks 9-10)

- [ ] Choose one: VAE / DQN / DDPM
- [ ] Read paper, derive core objective
- [ ] Implement, verify on a small problem, document
- [ ] Project README; tag `v0.5-extension`

## Phase 6: Polish (week 11)

- [ ] Fill in the results table in the main README
- [ ] Clean code, add docstrings and comments for non-obvious parts
- [ ] Verify setup instructions work from a fresh clone
- [ ] Add plots/GIFs to READMEs
- [ ] Write a short blog-style summary of lessons learned
- [ ] Pin the repo on GitHub profile and link it from CV

## Ongoing habits

- [ ] Commit small and often, with clear messages
- [ ] One branch per project, merge when done
- [ ] Keep derivations in `notes/`
- [ ] After each project: write down 3 things that surprised me