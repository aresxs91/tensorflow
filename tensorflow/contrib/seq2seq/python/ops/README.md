# Amortized Context Vector Inference for Sequence-to-Sequence Networks

The changes introduced to the `attention_wrapper.py` correspond to the suggested changes made in:

Sotirios Chatzis, Aristotelis Charalampous, Kyriacos Tolias et al. "Amortized Context Vector Inference for Sequence-to-Sequence Networks".
https://arxiv.org/abs/1805.09039

These can be enabled by instantiating an `AttentionWrapper` object with the `do_acvi=True` option.

In summary, if enabled, the model will be trained to infer a posterior distribution for the computed attention over a set of introduced latent variables. To approximate the reviewed loss function, we also rely on the he reparameterization trick for drawn Monte-Carlo samples in order to ensure their low variance.

The changes here depend on similar changes made in [this](https://github.com/aresxs91/nmt/commit/011e7d25e519033c15ed577975d74c994dee8f66) repository's commit.
