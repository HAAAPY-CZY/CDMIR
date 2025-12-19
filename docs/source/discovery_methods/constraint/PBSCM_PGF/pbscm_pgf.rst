PBSCM_PGF (Poisson Branching Structural Causal Model using Probability Generating Function)
=========================================================================================

Introduction
------------

PBSCM_PGF is a causal discovery method that identifies causal relationships using Probability Generating Functions (PGF). It extends the Poisson Branching Structural Causal Model (PBSCM) by leveraging PGFs to analyze the structure of causal relationships in data.


Usage
-----

.. code-block:: python

    from cdmir.effect.PBSCM_PGF.PB_SCM_PGF import PBSCM_PGF

    # Initialize PBSCM_PGF model
    pbscm_pgf = PBSCM_PGF(data)

    # Learn the causal graph
    causal_graph = pbscm_pgf.get_causal_graph()




Parameters
----------

**PBSCM_PGF Class Initialization**

- **data**: Input data matrix with shape (n_samples, n_features)


Returns
-------

- **causal_graph**: Causal matrix of the data, where causal_graph[i][j] = 1 indicates a causal relationship from variable i to variable j, and 0 otherwise


References
----------

.. [1] Xiang Y, Qiao J, Liang Z, et al. On the identifiability of poisson branching structural causal model using probability generating function[J]. Advances in Neural Information Processing Systems, 2024, 37: 11664-11699.
