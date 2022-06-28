# Local PyTorch/Tensorflow Development on M1 MacBooks

Conda environments for local PyTorch and/or Tensorflow development on Apple Silicon Mac Books.

Prequisites:
* An Apple Silicon Mac Book
* miniforge (and conda) for M1:
  * <code> brew install miniforge </code>
  * <code> conda init zsh </code>

To import, run:

<code> conda env create -f pytorch_mac_m1.yml</code>

and/or

<code> conda env create -f tensorflow_mac_m1.yml</code>

To list environments, type:

<code>conda env list</code>

To activate, run:

<code>conda activate pytorch</code>

or

<code>conda activate tf2</code>

*NOTE:* Do not update the PyTorch environment using <code>conda env update -n pytorch --all </code>, as long as the Apple Silicon support is available only in nightly builds. Such an update would override the pytorch and torchvision with the versions from the stable channel. And that one, at the moment of writing, doesn't support the Apple Silicon accelerated training natively.
