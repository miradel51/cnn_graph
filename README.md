# Spectral Graph Convolutional Neural Network (SGCNN)

The code in this repository implements an efficient generalization of the
popular Convolutional Neural Networks (CNNs) to arbitrary graphs, presented in
our paper:

Michaël Defferrard, Xavier Bresson, Pierre Vandergheynst, [Convolutional Neural
Networks on Graphs with Fast Localized Spectral Filtering][arXiv], Neural
Information Processing Systems (NIPS), 2016.

* Please cite the above paper if you use our code.
* The code is released under the terms of the [MIT license](LICENSE.txt).

[arXiv]: https://arxiv.org/abs/1606.09375

## Installation

1. Clone this repository.
   ```sh
   git clone https://github.com/mdeff/cnn_graph
   cd cnn_graph
   ```

2. Install the dependencies. Please edit `requirements.txt` to choose the
   TensorFlow version (CPU / GPU, Linux / Mac) you want to install, or install
   it beforehand. The code was developed with TF 0.8.
   ```sh
   pip install -r requirements.txt  # or make install
   ```

3. Play with the Jupyter notebooks.
   ```sh
   jupyter notebook
   ```

## Reproducing our results

Run all the notebooks to reproduce the experiments on
[MNIST](nips2016/mnist.ipynb) and [20NEWS](nips2016/20news.ipynb) presented in
the paper.
```sh
cd nips2016
make
```

## Using the model

To use our graph ConvNet on your data, you need:

1. a data matrix where each row is a sample and each column is a feature,
2. a target vector,
3. optionally, an adjacency matrix which encodes the structure as a graph.

See the [usage notebook](usage.ipynb) for a simple example with fabricated
data. Please get in touch if you are unsure about applying the model to
a different setting.
