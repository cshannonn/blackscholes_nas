# Black Scholes NAS
Can an artificial neural network learn the Black Scholes option pricing formula .... yes, and quite easily.
This problem will be used as a starting point for implementing neural architecture search (NAS). See the following two papers [Neural Architecture Search With Reinforcement Learning](https://arxiv.org/pdf/1611.01578.pdf) and [Efficient Neural Architecture Search via Parameter Sharing](https://arxiv.org/pdf/1802.03268.pdf) for an overview.

See [here](https://www.youtube.com/watch?v=pr-u4LCFYEY) for an overview of the Black Scholes formula. 

Notebook (Option_Data.ipynb) creates a dataset of approximately 1 million examples by pricing a call option using the Black Scholes formula over a range of possible parameters. This dataset will be used to train a neural network.

Notebook (BS_Keras.ipynb) implements a simple feed forward neural network using Keras to approximate the Black Scholes formula. It achieves fairly high accuracy after minimal amount of training time.

Notebook(BS_RandomSearch.ipynb) uses the GridSearch library from Scikit-learn to perform a non-exhaustive hyperparameter search (i.e., different optimizers).

Future notebooks will compare different libraries that allow you to search more parameters and/or are directed, such as [Talos](https://github.com/autonomio/talos), [Hyperas](https://github.com/maxpumperla/hyperas), [Auto-Keras](https://autokeras.com), and [DARTS](https://www.groundai.com/project/darts-differentiable-architecture-search/).
