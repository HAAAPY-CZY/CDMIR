ANM (Additive Noise Model)
============================

Introduction
------------

ANM is a functional-based causal discovery method that identifies causal relationships by testing the independence between the cause and the noise term in an additive noise model.

Usage
-----

.. code-block:: python

    from cdmir.discovery.funtional_based.anm.ANM import ANM
    # Initialize ANM model
    anm = ANM()
    # Test causal direction
    nonindepscore_forward, nonindepscore_backward = anm.cause_or_effect(X, Y)


Parameters
----------

- **x**: Input data array of shape (n,) or (n, 1)
- **y**: Output data array of shape (n,) or (n, 1)

Returns
-------

- **nonindepscore_forward**: HSIC statistic in the X→Y direction
- **nonindepscore_backward**: HSIC statistic in the Y→X direction


References
----------

.. [1] Hoyer, Patrik O., et al. "Nonlinear causal discovery with additive noise models." Advances in Neural Information Processing Systems. 2008.
