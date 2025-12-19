SHP (Structural Hawkes Processes)
=================================

Introduction
------------

SHP is a functional-based causal discovery method for learning causal structure from discrete-time event sequences. It extends the traditional Hawkes process by incorporating structural learning to identify causal relationships between event types.

Usage
-----

.. code-block:: python

    from cdmir.discovery.funtional_based.SHP.SHP import SHP

    # Initialize SHP model
    shp = SHP(
        event_table=event_table,
        decay=0.35,
        time_interval=5,
        penalty='BIC',
        reg=0.85,
        seed=2025
    )

    # Train the model with Hill Climb search
    likelihood, alpha, mu = shp.train_model(hill_climb=True)

Parameters
----------

**SHP Class Initialization**

- **event_table**: Event data table containing columns 'seq_id', 'time_stamp', and 'event_type'
- **decay**: The decay coefficient of the exponential kernel
- **time_interval**: Time interval size for discretizing timestamps (default: None)
- **init_structure**: Initial adjacency matrix for causal structure (default: None)
- **penalty**: Penalty method, either 'BIC' or 'AIC' (default: 'BIC')
- **seed**: Random seed for reproducibility (default: None)
- **reg**: Regularization parameter (default: 3.0)

**train_model Parameters**

- **hill_climb**: Whether to use Hill Climb search for structure learning (default: True)

Returns
-------

- **likelihood**: Likelihood value of the learned model
- **alpha**: Matrix of causal effect parameters between event types, where :math:`\alpha_{ij}` represents the causal effect from event type :math:`i` to :math:`j`
- **mu**: Vector of base intensity parameters for each event type, where :math:`\mu_j` is the base intensity for event type :math:`j`

References
----------

.. [1] Qiao J, Cai R, Wu S, et al. Structural hawkes processes for learning causal structure from discrete-time event sequences[J]. arXiv preprint arXiv:2305.05986, 2023.
