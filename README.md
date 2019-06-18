*Note*: I will maintain this version as best I can until the original `hlda` library is updated for Python3.

Hierarchical Latent Dirichlet Allocation
----------------------------------------

Hierarchical Latent Dirichlet Allocation (hLDA) addresses the problem of learning topic hierarchies from data. The model relies on a non-parametric prior called the nested Chinese restaurant process, which allows for arbitrarily large branching factors and readily accommodates growing
data collections. The hLDA model combines this prior with a likelihood that is based on a hierarchical variant of latent Dirichlet allocation.

[Hierarchical Topic Models and the Nested Chinese Restaurant Process](http://www.cs.columbia.edu/~blei/papers/BleiGriffithsJordanTenenbaum2003.pdf)

[The Nested Chinese Restaurant Process and Bayesian Nonparametric Inference of Topic Hierarchies](http://cocosci.berkeley.edu/tom/papers/ncrp.pdf)

Implementation
--------------

- [hlda/sampler.py](hlda/sampler.py) is the Gibbs sampler for hLDA inference, based on the implementation from [Mallet](http://mallet.cs.umass.edu/topics.php) having a fixed depth on the nCRP tree.


Installation
------------

- To get the version from *this* repo use: `pip install git+https://github.com/jreades/hlda.git` (using `pip install hlda` will give you the original version that hasn't been updated for Python3).
- An example notebook that infers the hierarchical topics on the BBC Insight corpus can be found in [notebooks/bbc_test.ipynb](notebooks/bbc_test.ipynb).
