Quantum Machine Learning Reading Group @ ICFO
=============================================

The reading group serves a dual purpose.
On one hand, we would like to develop an understanding of statistical learning theory and how quantum resources can make a difference.
On the other hand, we would like to develop skills that are marketable outside academia.
To achieve this dual purpose, we structure the meetings along three topics:

1. A recent, but already important paper on classical machine learning.

2. A quantum machine learning paper.

3. Coding exercises that implement a learning algorithm or a simulation of a quantum protocol.

Papers will be announced a week in advance.
Each week there will be a person responsible for a paper, but everybody is expected to read the two papers in advance and prepare with questions.
Coding will be done collaboratively through this repository.
The reading group requires commitment: apart from the 1.5-2 contact hours a week, at least another 2-3 hours must be dedicated to reading and coding.
You are not expected to know machine learning or programming before joining the group, but you are expected to commit the time necessary to catch up and develop the relevant skills.

The language of choice is Python 3.
MATLAB users will be shot on sight.
Julia is an upcoming language in which the bleeding-edge of machine learning and quantum simulation are easier to implement, and therefore it is an accepted alternative.

Resources
---------
The broader QML community is still taking shape.
We are attempting to organize it through the website [quantummachinelearning.org](http://quantummachinelearning.org/). You can also sign up for the mailing list there.
Please also consider contributing to the recently rewritten [Wikipedia article on QML](https://en.wikipedia.org/wiki/Quantum_machine_learning).
Apart from new content, stylistic and grammatical edits, figures, and translations are all welcome.

The best way to learn machine learning is by doing it.
The book [Python Machine Learning](https://www.packtpub.com/big-data-and-business-intelligence/python-machine-learning) is a good starter, along with its [GitHub repository](https://github.com/rasbt/python-machine-learning-book).
[Kaggle](http://kaggle.com/) is a welcoming community of data scientists.
It is not only about competitions: several hundred datasets are hosted on Kaggle, along with notebooks and scripts (collectively known as kernels) that do interesting stuff with the data.
These provide perfect stepping stones for beginners.
Find a dataset that is close to your personal interests and dive in.
For a sufficiently engaging theoretical introduction to machine learning, the book [The Elements of Statistical Learning: Data Mining, Inference, and Prediction](https://statweb.stanford.edu/~tibs/ElemStatLearn/) is highly recommended.

[Anaconda](https://www.continuum.io/downloads) is the recommended Python distribution if you are new to the language.
It ships with most of the scientific and machine learning ecosystem around Python.
It includes [Scikit-learn](http://scikit-learn.org/), which is excellent for prototyping machine learning models.
For scalable deep learning, [Keras](https://keras.io/) is recommended: it can transparently change between TensorFlow and Theano as back-ends.
[QuTiP](http://qutip.org/) is an excellent quantum simulation library, and with the latest version (4.1), it is [reasonably straightforward](http://qutip.org/docs/4.1/installation.html#platform-independent-installation) to install it in Anaconda with [conda-forge](https://conda-forge.github.io/).
QuTiP is somewhat limited in scalability, so perhaps it is worth checking out other simulators, such as [ProjectQ](http://projectq.ch/).

As for [Julia](http://julialang.org/), the [JuliaML](https://github.com/JuliaML) project collects most of the machine learning efforts.
It includes cool stuff like [Transformations](https://github.com/JuliaML/Transformations.jl), which allows you to define arbitrary computational graphs, not just the run-of-the-mill static ones implemented in TensorFlow and Theano.
[Quantum simulators](https://juliaquantum.github.io/) lag behind a bit, but there are interesting initiatives for doing [tensor network calculations](https://github.com/Jutho/TensorOperations.jl).

We will follow the good practices of [software carpentry](http://software-carpentry.org/), that is, elementary IT skills that every scientist should have.
In particular, we use [git](https://rogerdudler.github.io/git-guide/) as a version control system and host the repository right here on GitHub.
When editing text or [Markdown](https://guides.github.com/features/mastering-markdown/) documents like this one, please write every sentence in a new line to ensure that conflicts are efficiently resolved when several people edit the same file.

Meeting 1
---------
10.00-11.30, 16 February 2017, Seminar Room (201).

Papers:

- Kingma, D. & Ba, J. [Adam: A Method for Stochastic Optimization](https://arxiv.org/abs/1412.6980). *Proceedings of ICLR-15, 3rd International Conference for Learning Representations*, 2014.
This paper introduces a derivative of stochastic gradient descent that is now widely used in training deep learning networks.
For instance, it is one of the [available optimizers](https://keras.io/optimizers/) in Keras.

- Wan, K. H.; Dahlsten, O.; Kristjánsson, H.; Gardner, R. & Kim, M. S. [Quantum generalisation of feedforward neural networks](https://arxiv.org/abs/1612.01045). *arXiv:1612.01045*, 2016.
Papers on quantum neural networks are typically written by crackpots, and this work is one of the refreshing exceptions.
It gives a twist on gradient descent to train neural networks of the quantum generalization of classical tasks. One of the examples is an autoencoder: a [related and equally interesting paper](https://arxiv.org/abs/1612.02806) came out a few days later, which is also worth reading.
This latter paper explicitly mentions that all simulations were implemented in Python with QuTiP.

Coding exercise:

- The first week does not have a coding exercise.
Instead, please ensure that your computational environment is up and running.
Python with the recommended libraries should be there, along with an editor.
Either use your favourite text editor, or opt for Spyder, which is also bundled in Anaconda.
Ensure that you can open and run Jupyter notebooks.
Go through a git tutorial, like the one linked under Resources, fork this repository, clone it, and add the upstream repo to follow.
If you need help, we will be around in 372 from 5pm on Wednesday, 15 Feb.

Tutorial 1
----------
16.00-17.30, 21 February 2017, Yellow Lecture Room (247).

This tutorial is about the importance of using a version control system. The focus is on git, starting with using it locally, for collaborating on LaTeX documents on Overleaf, and finishing with some examples using GitHub. The [notes](Tutorials/Git.md) are in the Tutorials folder.


Meeting 2
---------
10.00-11.30, 23 February 2017, Seminar Room (201).

Papers:

- Abadi, M.; Barham, P.; Chen, J.; Chen, Z.; Davis, A.; Dean, J.; Devin, M.; Ghemawat, S.; Irving, G.; Isard, M.; Kudlur, M.; Levenberg, J.; Monga, R.; Moore, S.; Murray, D. G.; Steiner, B.; Tucker, P.; Vasudevan, V.; Warden, P.; Wicke, M.; Yu, Y. & Zheng, X.
[TensorFlow: A System for Large-scale Machine Learning](https://arxiv.org/abs/1603.04467).
*Proceedings of the 12th USENIX Conference on Operating Systems Design and Implementation*, 2016, 265-283.
This is the only systems paper we will discuss.
Given the hype around it, its actual importance, and its relevance for getting a job in real life, it is worth looking at it.
An earlier open source effort, [Theano](http://deeplearning.net/software/theano/) implements the same idea of using a data flow graph as a computational abstraction; see the [matching paper](https://arxiv.org/abs/1605.02688).

- Lau, H.-K.; Pooser, R.; Siopsis, G. & Weedbrook, C.
[Quantum machine learning over infinite dimensions](https://arxiv.org/abs/1603.06222). *arXiv:1603.06222*, 2016.
This paper is the only proposal so far for using continuous variable systems for doing machine learning.
These systems are attractive for both their theoretical and experimental properties, and the paper also allows us to talk about building blocks of machine learning algorithms.

Coding exercises:

- Implement an autoenconder in TensorFlow, say, random ten dimensional vectors encoded on a six dimensional hidden layer.
Use Adam as the optimization routine.
Keras is a recommended abstraction layer around TensorFlow.

- Simulate a swap test.
The [circuit](https://en.wikipedia.org/wiki/Quantum_digital_signature#Public_Key_should_be_the_same_for_every_recipient_.28Swap_Test.29) is nothing but a Fredkin gate and a Hadamard gate, followed by a local measurement on the ancilla.
This task is trivial to do in QuTiP, but you can also try your hands on ProjectQ, or the [IBM Quantum Experience](https://www.research.ibm.com/quantum/).

Tutorial 2
----------
16.00-17.30, 07 March 2017, Yellow Lecture Room (247).

This is a Python introduction without talking about introductory stuff on Python. The goal was to give a general idea of what goes into designing a programming language and what kind of trade-offs have to be made, followed by some idiomatic expressions in Python and some caveats. The [corresponding notebook](Tutorials/Python_Introduction.ipynb) is in the Tutorials folder.

Meeting 3
---------
10.00-11.30, 09 March 2017, Seminar Room (201).

Papers:

- Silver, D.; Huang, A.; Maddison, C. J.; Guez, A.; Sifre, L.; van den Driessche, G.; Schrittwieser, J.; Antonoglou, I.; Panneershelvam, V.; Lanctot, M.; Dieleman, S.; Grewe, D.; Nham, J.; Kalchbrenner, N.; Sutskever, I.; Lillicrap, T.; Leach, M.; Kavukcuoglu, K.; Graepel, T. & Hassabis, D. [Mastering the game of *Go* with deep neural networks and tree search](http://doi.org/10.1038/nature16961). *Nature*, 2016, 529, 484-489. It is the state-of-the-art in reinforcement learning. The scheme combines deep learning with a heuristic search, which is a pattern that is seen over and over again since this paper came out. The simpler, but equally glamorous task of playing Atari games was published by the same group; [that paper](https://arxiv.org/abs/1312.5602) is also worth a look.

- Dunjko, V.; Taylor, J. M. & Briegel, H. J. [Quantum-Enhanced Machine Learning](https://arxiv.org/abs/1610.08251). *Physical Review Letters*, 2016, 117, 130501. This paper takes a comprehensive look at what quantum agents can learn in a reinforcement learning scenario. It is worth looking at an [earlier and much longer version](https://arXiv.org/abs/1507.08482) of this paper.

Coding exercises:

- Teach an agent to learn a reinforcement learning task. [OpenAI Gym](http://gym.openai.com) is a collection of environments in which you can benchmark reinforcement learning algorithms. It was officially announced at NIPS in December 2016. [This](https://github.com/claymcleod/dqn) works fine with Pacman, it uses Keras and Theano for implementing the agent, and it is barely a hundred lines of code.

- Optional: The classical first-person shooter Doom is [one of the possible environments](https://gym.openai.com/envs#doom). Installing the Doom environment is fairly intricate as it is not included by default. Follow [these](https://github.com/peterwittek/qml-rg/issues/8#issuecomment-282140692) instructions to get it right.

Meeting 4
---------
10.00-11.30, 16 March 2017, Seminar Room (201).

Papers:

- LeCun, Y.; Bengio, Y. & Hinton, G. [Deep learning](http://doi.org/10.1038/nature14539). *Nature*, 2015, 521, 436-444. This is a review paper by the three greatest giants in deep learning. The paper gives you an idea of the most important neural network architectures that we use today. The current flood of deep learning was unleashed on us by [this paper on convolutional neural networks](http://papers.nips.cc/paper/4824-imagenet-classification-with-deep-convolutional-neural-networks) by Geoff Hinton. It is also well worth reading: you seldom come across a paper that accumulated over 10,000 citations in five years. [This blog post](http://www.asimovinstitute.org/neural-network-zoo/) gives an entertaining overview of neural network architectures.

- Wiebe, N.; Kapoor, A. & Svore, K. M. [Quantum Deep Learning](http://arxiv.org/abs/1412.3489). *arXiv:1412.3489*, 2014. This is an insightful paper on stacked Boltzmann machines that highlights many possibilities and limitations of using quantum protocols for learning. It was also one of the first papers to consider Boltzmann machines for quantum-enhanced learning -- since then, this line of research took off and now there are N+1 papers on it.

Coding exercises:

- Implement Q-learning from scratch for a [simple toy example](Meeting 4/rl_toy_example.py). The state space is trivial and the agent has full access to it, there is no adversary and the distribution does not change depending on the actions of the agent. After the classical agent, try it with simulated quantum agents. See, for instance, [this paper](https://arxiv.org/abs/1401.4997) or [this one](https://arxiv.org/abs/1601.07358) for clues. The trivial solution is to replace the search by Grover's.

- Optional: Do the same thing with tic-tac-toe against a perfect AI (i.e., you cannot win). See the instructions in the [corresponding file](Meeting 4/tictactoe.py). Here the state and the action space might prove too large for a classical simulation of a quantum agent, so you might want to introduce heuristics to reduce it.

Tutorial 3
----------
16.00-17.30, 21 March 2017, Yellow Lecture Room (247).

The tutorial will be on Python and the scientific ecosystem: using Python for science and machine learning, plotting and visualization, how to write beautiful scientific code, and the best practices of providing a computational appendix to your papers.


Meeting 5
---------
10.00-11.30, 23 March 2017, Seminar Room (201).

Papers:

- Chen, T. & Guestrin, C. [XGBoost: A Scalable Tree Boosting System](https://arxiv.org/abs/1603.02754). *Proceedings of KDD-16,  22nd International Conference on Knowledge Discovery and Data Mining*. 2016, 785-794. XGBoost is a simple boosting algorithm for a class of ensemble methods and it has been winning Kaggle competitions. The popularity is not yet evidenced in the citation record, but it is in the [matching GitHub repo](https://github.com/dmlc/xgboost). Boosting is an ancient method, the most well-known example being [AdaBoost](https://link.springer.com/chapter/10.1007/3-540-59119-2_166). Pay attention to how regularization is done.

- Neven, H.; Denchev, V. S.; Drew-Brook, M.; Zhang, J.; Macready, W. G. & Rose, G. [Binary classification using hardware implementation of quantum annealing](https://www.google.com/googleblogs/pdfs/nips_demoreport_120709_research.pdf). *Demonstrations at NIPS-09, 24th Annual Conference on Neural Information Processing Systems*, 2009, 1-17. Perhaps the earliest implementation of a quantum machine learning algorithm. It relies on one of D-Wave's early annealing chips and exploits nonconvex optimization for a better regularized boosting algorithm.

Coding exercise:

- Crack the annoying APS captcha. A cleaned up data set is available as a [zip](Meeting 5/images.zip), along with a [Python file to load the images](Meeting 5/image_loader.py). Use a convolutional neural network like [LeNet in Keras](http://www.pyimagesearch.com/2016/08/01/lenet-convolutional-neural-network-in-python/). You definitely do not need [Inception](https://arxiv.org/abs/1602.07261) to crack this. The real-life images contain sheared examples: once you are done with the basic example, turn to this set as testing examples. The labels are given in a text file. You can solve this two ways. 1) Use a hack: APS was stupid enough to include enough information in the images to de-shear them. A function `deshear` is included in the image loader to help you. 2) Do it the deep learning way and [use data augmentation](http://ankivil.com/kaggle-first-steps-with-julia-chars74k-first-place-using-convolutional-neural-networks/). This is a crucially important technique in data science.

Meeting 6
---------
10.00-11.30, 30 March 2017, Seminar Room (201).

On this meeting, we will only discuss one paper. Then we will spend half an hour discussing what we learned over the first six weeks to consolidate our knowledge.

Paper:

- Rebentrost, P.; Mohseni, M. & Lloyd, S. [Quantum Support Vector Machine for Big Data Classification](https://arxiv.org/abs/1307.0471). *Physical Review Letters*, 2014, 113, 130503. Take a look at the [experimental demonstration](https://arxiv.org/abs/1410.1054) too.

Coding exercise:

- Continue working on the APS captcha collection. Do the same thing as the week before, but replacing the neural network. Try the following three algorithms: [XGBoost](https://github.com/dmlc/xgboost), [random forests](https://en.wikipedia.org/wiki/Random_forest), and [support vector machines](https://en.wikipedia.org/wiki/Support_vector_machine). The former two are still competitive in Kaggle challenges even in the face of deep neural networks, whereas support vector machines ruled the machine learning landscape for a decade between about 1995 and 2005. [Random forests](http://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html) and [support vector machines](http://scikit-learn.org/stable/modules/svm.html) are available as part of Scikit-learn, and XGBoost also [plays along nicely](https://github.com/dmlc/xgboost/blob/master/demo/guide-python/sklearn_examples.py) with the package. Visualize the decision boundaries of the algorithms, along with different choices of parameters and regularization.

Meeting 7
---------
10.00-11.30, 6 April 2017, Seminar Room (201).

Papers:

- Srivastava, N.; Hinton, G. E.; Krizhevsky, A.; Sutskever, I. & Salakhutdinov, R. [Dropout: a simple way to prevent neural networks from overfitting](http://jmlr.org/papers/v15/srivastava14a.html). *Journal of Machine Learning Research*, 2014, 15, 1929-1958. This is a great example of how regularization is done in deep learning. For a prehistoric paper on regularizing neural networks, read [Optimal Brain Damage](https://papers.nips.cc/paper/250-optimal-brain-damage) from 1989.

- Amin, M. H.; Andriyash, E.; Rolfe, J.; Kulchytskyy, B. & Melko, R. [Quantum Boltzmann Machine](https://arxiv.org/abs/1601.02036). *arXiv:1601.02036*, 2016. This paper uses the D-Wave machine for Gibbs sampling to train Boltzmann machines. Unlike some other proposals that suggest using this hardware-based sampling for increasing connectivity (and thus complexity), the authors used an actually quantum Hamiltonian and analyzed the outcome.

Coding exercise:

- Simulate a full quantum support vector machine. It has many components, so you might want to consider distributing the workload across the programming groups. For an example on the HHL, look at [this notebook](https://github.com/mariaschuld/phdthesis/blob/master/QLSE%20algorithm.ipynb). Once you have the simulation ready, downsample the APS captcha collection to a ridiculously low resolution (say, 2x2), and train your QSVM on the collection. You could also use a classical autoencoder instead of raw downsampling. Or a quantum one.

Tutorial 4
----------
16.00-17.30, 18 April 2017, Yellow Lecture Room (247).

The tutorial will be on advanced data science, covering data collection, filtering, cleaning, and visual analysis. We will study whether arXiv metadata alone is predictive enough to tell the impact factor of the journal where the manuscript will be published.

Meeting 8
---------
10.00-11.30, 20 April 2017, Seminar Room (201).

Papers:

- Sutskever, I.; Vinyals, O. & Le, Q. V. [Sequence to Sequence Learning with Neural Networks](http://papers.nips.cc/paper/5346-sequence-to-sequence-learning-with-neural-networks). *Advances in Neural Information Processing Systems*, 2014, 27, 3104-3112. [Long short-term memory](https://dx.doi.org/10.1162%2Fneco.1997.9.8.1735) has been used for two decades for sequence learning, and this paper makes it deep.

- Schuld, M.; Fingerhuth, M. & Petruccione, F. [Quantum machine learning with small-scale devices: Implementing a distance-based classifier with a quantum interference circuit](https://arxiv.org/abs/1703.10793). *arXiv:1703.10793*, 2017. There is no connection to the classical paper, but it just came out and it is a really fun paper. It flips the perspective: instead of trying to come up with an abstract formulation of a quantum-enhanced learning protocol that needs a million qubits, a universal quantum computer, a QRAM, plus an oracle just in case, this manuscript takes the IBM Quantum Experience as the starting point and looks at what kind of learning can be done with it.

Coding exercise:

- Do what everyone who learns machine learning coming from science background does first: predict stock prices. Grab a data set (e.g. [Dow Jones Index](https://archive.ics.uci.edu/ml/datasets/Dow+Jones+Index)) and unleash a [phased LSTM](https://github.com/dannyneil/public_plstm) on it. The [paper on phased LSTMs](https://arxiv.org/abs/1610.09513) was published on NIPS last year, trying to address mid-term memory. Ordinary LSTMs are routinely deployed on stock prices, for instance, see [this kernel](https://www.kaggle.com/pablocastilla/d/dgawlik/nyse/predict-stock-prices-with-lstm) on Kaggle. I take a 10% cut if you make money on this.

Meeting 9
---------
10.00-11.30, 27 April 2017, Seminar Room (201).

Paper:

- Wattenberg, M.; Viégas, F. & Johnson, I. [How to Use t-SNE Effectively](https://doi.org/10.23915/distill.00002). *Distill*, 2016. Manifold learning as it is known, took off with [Isomap](https://doi.org/10.1126/science.290.5500.2319), although there were some precursors to it, like [self-organizing maps](https://en.wikipedia.org/wiki/Self-organizing_map), that used a two-dimensional grid of neurons to do an embedding. The original [t-SNE paper](http://www.jmlr.org/papers/v9/vandermaaten08a.html) appeared in 2008, and it became the most popular manifold learning method. It is, however, not easy to get it right, and this interactive paper gives insights on the inner workings of the algorithm. [Add the Jonker-Volgenant algorithm](https://blog.sourced.tech/post/lapjv/), and you have visualizing superpowers.

Coding exercise:

- Assume that cats and dogs lie on a high-dimensional manifold. Get the images from the [CIFAR10](https://www.cs.toronto.edu/~kriz/cifar.html) data set. Embed the manifold in two-dimensions with a globally optimal method (SVD or MDS), and three local methods (Isomap, spectral embedding, and t-SNE). Plot sample images along with the actual points. Scikit-learn has a [handy tutorial](http://scikit-learn.org/stable/modules/manifold.html) on this. There is another [awesome explanation](https://colah.github.io/posts/2014-10-Visualizing-MNIST/) in 2 and 3D. Then do the same thing, but first train a CNN on the images, and visualize the last representation layer before the ordinary FNN part. [Here is](https://blog.keras.io/how-convolutional-neural-networks-see-the-world.html) a tutorial on the raw output, and [here is](https://colah.github.io/posts/2015-01-Visualizing-Representations/) a blog post that uses manifold learning to visualize the abstract representation. Following [this comment](https://github.com/peterwittek/qml-rg/commit/94af3599969d04c63a0bbec2a3ab8f40c40f1ab6#commitcomment-21929565), it is a good idea to pull off a pre-trained model from [keras.applications](https://keras.io/applications/).

Tutorial 5
----------
16.00-17.30, 02 May 2017, Yellow Lecture Room (247).

We will go through the different functions of Kaggle, promoting you from [Novice to Contributor](https://www.kaggle.com/progression). It is assumed that you are able to solve the exercises given in the first four tutorials.

Meeting 10
---------
11.00-13.00, 04 May 2017, Yellow Lecture Room (247).

Papers:

- Zheng, S.; Jayasumana, S.; Romera-Paredes, B.; Vineet, V.; Su, Z.; Du, D.; Huang, C. & Torr, P. H. S. [Conditional Random Fields as Recurrent Neural Networks](https://arxiv.org/abs/1502.03240). *Proceedings of ICCV-15, International Conference on Computer Vision*, 2015, 1529-1537. This is an important paper that draws a parallel between probabilistic graphical models (here Markov networks and conditional random fields) and neural networks.

- Benedetti, M.; Realpe-Gómez, J.; Biswas, R. & Perdomo-Ortiz, A. [Quantum-assisted learning of graphical models with arbitrary pairwise connectivity](https://arxiv.org/abs/1609.02542). *arXiv:1609.02542*, 2016. In probabilistic graphical models, both learning and inference are computationally expensive. This paper looks at how we can embed arbitrary graphs in a contemporary quantum annealing architecture to learn the structure of a model efficiently.
