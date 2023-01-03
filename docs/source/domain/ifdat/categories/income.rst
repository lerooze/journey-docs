INCOME: Observed Agent Income
=============================

Used to submit analytic data on income sources of the ``RA`` in accrual basis.
Data is collected on the level of each share/investment fund unit of the ``RA`` and not on the level of the ``RA`` itself.

Below the dimensions, measures and if needed the attributes of the measures for each table:

REVENUE
-------

Used to submit revenue data.

DIMENSIONS
~~~~~~~~~~

IID
    Identifier code of the share/investment fund unit of the ``OA`` (:ref:`shr`).

TYPE (TYP)
    Revenue type choosing from ``INCM_RVN_ENUM``.
    
DATE (DT)
    Reference date.  For further details see :doc:`../../../generic`. 

FREQUENCY (FRQNCY)
    Reference period. For further details see :doc:`../../../generic`.

MEASURES
~~~~~~~~

.. _revenue:

AMOUNT (AMNT)
    Revenue by each share/investment fund unit expressed in :ref:`currency <sishrcurrency>` ·

AMOUNT IN EURO (EUR_AMNT)
    revenue_ in euro.
    

EXPENSE
-------

Used to submit expense data.

DIMENSIONS
~~~~~~~~~~

IID
    Identifier code of the share/investment fund unit of the ``OA`` (:ref:`shr`).

TYPE (TYP)
    Expense type choosing from ``INCM_EXPNS_ENUM``.
    
DATE (DT)
    Reference date.  For further details see :doc:`../../../generic`. 

FREQUENCY (FRQNCY)
    Reference period. For further details see :doc:`../../../generic`.

MEASURES
~~~~~~~~

.. _expense:

AMOUNT (AMNT)
    Expense by each share/investment fund unit expressed in :ref:`currency <sishrcurrency>` ·

AMOUNT IN EURO (EUR_AMNT)
    expense_ in euro.
