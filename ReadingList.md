# Reading List

Papers and resources for each project, in reading order. Core = read before coding. Optional = read if you want more depth.

**How to read a paper:** abstract -> figures and tables -> introduction -> method -> experiments -> skim the rest. First pass: 30-45 minutes, goal is to understand what problem it solves and the core idea. Second pass: derive the math yourself.

---

## 00. Background (read alongside Phase 0)

- **Dive into Deep Learning** (d2l.ai): free interactive book, good for filling gaps
- **Deep Learning** (Goodfellow, Bengio, Courville): https://www.deeplearningbook.org/ (chapters 6 and 8 cover MLPs, backprop, optimization)
- **3Blue1Brown, Neural Networks series** (YouTube): geometric intuition for backprop

## 01. MLP + Backpropagation

**Core**
- Rumelhart, Hinton, Williams (1986). *Learning representations by back-propagating errors.* Nature 323, 533-536. https://doi.org/10.1038/323533a0 (paywalled; access through LTH library or a university proxy)
- LeCun, Bottou, Bengio, Haffner (1998). *Gradient-Based Learning Applied to Document Recognition.* The MNIST paper. http://yann.lecun.com/exdb/publis/pdf/lecun-98.pdf (read the MLP and training sections first, skip the rest on a first pass)

**Optional**
- Glorot & Bengio (2010). *Understanding the difficulty of training deep feedforward neural networks.* Why initialization matters. https://proceedings.mlr.press/v9/glorot10a.html
- Kingma & Ba (2014). *Adam: A Method for Stochastic Optimization.* Good extra experiment: compare SGD vs Adam. https://arxiv.org/abs/1412.6980

## 02. Autograd Engine

**Core**
- Karpathy, *The spelled-out intro to neural networks and backpropagation: building micrograd.* https://www.youtube.com/watch?v=VMj-3S1tku0
- micrograd repo (look only after you have tried it yourself): https://github.com/karpathy/micrograd

**Optional**
- Baydin et al. (2015). *Automatic differentiation in machine learning: a survey.* https://arxiv.org/abs/1502.05767

## 03. CNN and ResNet

**Core**
- Krizhevsky, Sutskever, Hinton (2012). *ImageNet Classification with Deep Convolutional Neural Networks* (AlexNet). https://papers.nips.cc/paper/2012/hash/c399862d3b9d6b76c8436e924a68c45b-Abstract.html (PDF: https://proceedings.neurips.cc/paper/2012/file/c399862d3b9d6b76c8436e924a68c45b-Paper.pdf)
- He, Zhang, Ren, Sun (2015). *Deep Residual Learning for Image Recognition* (ResNet). https://arxiv.org/abs/1512.03385
- Ioffe & Szegedy (2015). *Batch Normalization.* https://arxiv.org/abs/1502.03167
- Hinton et al. (2012). *Improving neural networks by preventing co-adaptation of feature detectors* (Dropout). https://arxiv.org/abs/1207.0580

**Optional**
- Simonyan & Zisserman (2014). *Very Deep Convolutional Networks* (VGG). https://arxiv.org/abs/1409.1556
- He et al. (2016). *Identity Mappings in Deep Residual Networks* (ResNet v2). https://arxiv.org/abs/1603.05027

## 04. Transformer / mini-GPT

**Core**
- Vaswani et al. (2017). *Attention Is All You Need.* https://arxiv.org/abs/1706.03762
- Jay Alammar, *The Illustrated Transformer.* https://jalammar.github.io/illustrated-transformer/
- 3Blue1Brown, *Visualizing Attention.* https://www.youtube.com/watch?v=eMlx5fFNoYc
- Karpathy, *Let's build GPT: from scratch, in code, spelled out.* (YouTube; watch in stages, after you have attempted each part yourself)

**Optional**
- Bahdanau, Cho, Bengio (2014). *Neural Machine Translation by Jointly Learning to Align and Translate.* Where attention started. https://arxiv.org/abs/1409.0473
- Ba, Kiros, Hinton (2016). *Layer Normalization.* https://arxiv.org/abs/1607.06450
- Radford et al. (2019). *Language Models are Unsupervised Multitask Learners* (GPT-2). https://cdn.openai.com/better-language-models/language_models_are_unsupervised_multitask_learners.pdf
- *The Annotated Transformer* (Harvard NLP), contains full code, so use only to check your work: https://nlp.seas.harvard.edu/annotated-transformer/
- nanoGPT, same caveat: https://github.com/karpathy/nanoGPT

## 05. Extension (choose one)

**VAE**
- Kingma & Welling (2013). *Auto-Encoding Variational Bayes.* https://arxiv.org/abs/1312.6114

**GAN**
- Goodfellow et al. (2014). *Generative Adversarial Networks.* https://arxiv.org/abs/1406.2661

**Diffusion (hardest)**
- Ho, Jain, Abbeel (2020). *Denoising Diffusion Probabilistic Models.* https://arxiv.org/abs/2006.11239

**Reinforcement learning (DQN)**
- Mnih et al. (2013). *Playing Atari with Deep Reinforcement Learning.* https://arxiv.org/abs/1312.5602
- Mnih et al. (2015). *Human-level control through deep reinforcement learning.* Nature. https://doi.org/10.1038/nature14236

**Word embeddings (short warm-up)**
- Mikolov et al. (2013). *Efficient Estimation of Word Representations in Vector Space.* https://arxiv.org/abs/1301.3781

---

## Notes on storing papers

- Link to papers rather than committing PDFs to the repo: it keeps the repo small, and some papers (Nature, IEEE) are not freely redistributable.
- If you want local copies, keep them in a `papers/` folder and add `papers/` to `.gitignore`.
- Use `notes/` for your own summaries and derivations, one file per paper.