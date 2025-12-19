PBSCM (Poisson Branching Structural Causal Model)
=============================================

Introduction
------------

PBSCM is a functional-based causal discovery method that identifies causal relationships using high-order cumulants with path analysis. It assumes that the causal relationships can be modeled as a Poisson branching process.


Usage
-----

.. code-block:: python


    from cdmir.discovery.funtional_based.PBSCM.PB_SCM import PB_SCM

    # Initialize PBSCM model
    pbscm = PB_SCM(data)

    # Get causal graph
    causal_graph = pbscm.get_causal_graph(alpha=0.04, max_order=4, threshold=0)


Parameters
----------

**PB_SCM Class Initialization**

- **data**: Input data matrix (n_samples x n_variables)

**get_causal_graph**


- **alpha**: Confidence level (default: 0.04)
- **max_order**: The maximum order of Lambda_k (default: 4)
- **threshold**: Threshold when bootstrap test fails (default: 0)

Returns
-------

- **causal_graph**: Causal matrix of the data

References
----------

.. [1] Qiao J, Xiang Y, Chen Z, et al. Causal discovery from poisson branching structural causal model using high-order cumulant with path analysis[C]//Proceedings of the AAAI Conference on Artificial Intelligence. 2024, 38(18): 20524-20531.
