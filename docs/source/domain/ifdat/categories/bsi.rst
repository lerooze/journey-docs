BSI: Balance Sheet Items
========================

Used to submit analytic data on balance sheet items of the ``OA``.

Below the dimensions, measures and if needed the attributes of the measures for each table:

CASH
----

Χρησιμοποιείται για την παροχή λογιστικών στοιχείων των χρηματικών διαθέσιμων των ``ΥΕΟ``.

DIMENSIONS
~~~~~~~~~~

CURRENCY (CRRNCY)
    Cash currency choosing from ``GEN_CRRNCY_ENUM``.

ID
    ``OA`` identifier code (:ref:`org`).

DATE (DT)
    Reference date.  For further details see :doc:`../../../generic`. 

MEASURES
~~~~~~~~~~

.. _cashstock:

STOCK (STCK)
    Nominal value·

STOCK IN EURO (EUR_STCK)
    Η cashstock_ in euro·
    

DEPOSIT
-------

Used to submit deposit account data of ``OA``.  For the definition of a deposit see :ref:`here <dep>`.  Measure values are expressed in :ref:`currency <depcurrency>` of the deposit except stated otherwise in the measure definition.

DIMENSIONS
~~~~~~~~~~

IID
    Deposit identifier code (:ref:`dep`).

DATE (DT)
    Reference date.  For further details see :doc:`../../../generic`. 

MEASURES
~~~~~~~~

.. _depstock:

STOCK (STCK)
    Outstanding amount including accrued interest as well as interest arrears and not excluding any haircuts/writeoff/writedowns.

STOCK IN EURO (EUR_STCK)
    depstock_ in euro.

ACCRUALS (ACCRLS)
    Accrued interest.

ARREARS (ARRRS)
    Interest arrears.
    
WRITE-OFFS (WRT_OFFS)
    Write offs, writedowns, haircuts.

ASSET_SFT
---------

Used to submit account data of security financing transaction in which the ``OA`` has loaned cash.  For the definition of a security financing transaction see :ref:`here <sft>`.  Measure values are expressed in :ref:`currency <sftcurrency>` of the transaction except stated otherwise in the measure definition.

DIMENSIONS
~~~~~~~~~~

IID
    Identifier code of the security financing transaction (:ref:`sft`).

DATE (DT)
    Reference date.  For further details see :doc:`../../../generic`. 

MEASURES
~~~~~~~~

.. _asftstock:

STOCK (STCK)
    Amount of cash that the ``OA`` has loaned in the transaction.

STOCK IN EURO (EUR_STCK)
    asftstock_ in euro. 
    
    
ASSET_DEBT
----------

Used to submit account data of debt instruments owned by the ``OA``.  For the definition of a debt instrument see :ref:`here <dbt>`.  Measure values are expressed in :ref:`currency <dbtcurrency>` of the debt instrument except stated otherwise in the measure definition.

DIMENSIONS
~~~~~~~~~~

IID
    Debt instrument identifier code (:ref:`dbt`).

ID
    ``OA`` identifier code (:ref:`org`).

DATE (DT)
    Reference date.  For further details see :doc:`../../../generic`. 

FRQNCY (FREQUENCY)
    Reference period. For further details see :doc:`../../../generic`.

MEASURES
~~~~~~~~~~

.. _adbtstock:

STOCK (STCK)
    Market value including accrued interest but not including interest arrears.

STOCK IN EURO (EUR_STCK)
    adbtstock_ in euro.

TRANSACTIONS (TRNSCTNS)
    Transactions net of any commissions and/or transaction taxes (**flow measure**). 

.. _debt_nominal:

NOMINAL STOCK (NMNL_STCK)
    Nominal value.

LOANED FOR REPOS (LND_FR_RPS)
    Amount of debt_nominal_ that the ``OA`` has lent to ``REPOS`` transactions.

LOANED FOR SCLB (LND_FR_SCLB)
    Amount of debt_nominal_ that the ``OA`` has lent to securities or commodities lending/borrowing transactions.

LOANED FOR BSBT (LND_FR_BSBT)
    Amount of debt_nominal_ that the ``OA`` has lent to ``sell-buy back`` transactions.

LOANED FOR MLT (LND_FOR_MLT)
    Amount of debt_nominal_ that the ``OA`` has lent to ``margin`` transactions.

ACCRUALS (ACCRLS)
    Accrued interest.

ARREARS (ARRRS)
    Interest arrears.


SHARE
-----

Used to submit accounting data of share/investment fund units owned by the ``OA``.  For the definition of a share/investment fund unit instrument see :ref:`here <shr>`.  Measure values are expressed in :ref:`currency <shrcurrency>` of the debt instrument except stated otherwise in the measure definition.


DIMENSIONS
~~~~~~~~~~

IID
    Identifier code of the share/investment fund unit (:ref:`shr`).

ID
    ``OA`` identifier code (:ref:`org`).

DATE (DT)
    Reference date.  For further details see :doc:`../../../generic`. 

FRQNCY (FREQUENCY)
    Reference period. For further details see :doc:`../../../generic`.

MEASURES
~~~~~~~~

.. _shrstock:

STOCK (STCK)
    Market value or fair value if not available.  Fair value is estimated by one of the following ways:

    * based on the value of listed shares;
    * based on equity capital value;
    * based on discounting of future profits.
    
STOCK IN EURO (EUR_STCK)
    shrstock_ in euro·

TRANSACTIONS (TRNSCTNS)
    Transactions net of any commissions and/or transaction taxes (**flow measure**). 

.. _share_nominal:

QUANTITY (QNTTY)
    Number of shares/investment fund units owned by the ``OA``.

LOANED_FOR_REPOS (LND_FR_RPS)
    Quantity of share_nominal_ that the ``OA`` has lent to ``REPOS`` transactions.

LOANED_FOR_SCLB (LND_FR_SCLB)
    Quantity of share_nominal_ that the ``OA`` has lent to securities or commodities lending/borrowing transactions.

LOANED FOR BSBT (LND_FR_BSBT)
    Quantity of share_nominal_ that the ``OA`` has lent to ``sell-buy back`` transactions.

LOANED FOR MLT (LND_FOR_MLT)
    Quantity of share_nominal_ that the ``OA`` has lent to ``margin`` transactions.


EXT_DERIVATIVE
--------------

Used to submit accounting data of exchange traded derivatives traded by the ``OA``.  For the definition of an exchange traded derivative see :ref:`here <edr>`.  Measure values are expressed in :ref:`currency <edrcurrency>` of the debt instrument except stated otherwise in the measure definition.

DIMENSIONS
~~~~~~~~~~

IID
    Identifier code of the exchange traded derivative (:ref:`edr`)·

ID
    ``OA`` identifier code (:ref:`org`).

DATE (DT)
    Reference date.  For further details see :doc:`../../../generic`. 

FRQNCY (FREQUENCY)
    Reference period. For further details see :doc:`../../../generic`.

MEASURES
~~~~~~~~~~

.. _edrstock:

STOCK (STCK)
    Market value which could fluctuate from positive to negative for futures and forward contracts.
    Some of the call/put options and future products work with a margin account in which profit and losses are recorded daily and in this case their market value is always zero. 
    
STOCK IN EURO (EUR_STCK)
    edrstock_ in euro. 

GRSS_STCK (GROSS STOCK)
    edrstock_ adding to it any net cumulative profits of call/put options, forward contracts that work with a margin account and in those cases edrstock_ is zero.

TRANSACTIONS (TRNSCTNS)
    Transactions net of any commissions and/or transaction taxes (**flow measure**). 

QUANTITY (QNTTY)
    Quantity held of the derivative.

STRATEGY (STRTGY)
    Investment strategy for the derivative transaction choosing from ``DRVTV_STRTGY_ENUM``.

OTC_DERIVATIVE
--------------

Used to submit accounting data of over the counter derivatives traded by the ``OA``.  For the definition of an over the counter derivative see :ref:`here <odr>`.  Measure values are expressed in :ref:`currency <odrcurrency>` of the debt instrument except stated otherwise in the measure definition.

DIMENSIONS
~~~~~~~~~~

IID
    Identifier code of the over the counter derivative (:ref:`odr`)·

DATE (DT)
    Reference date.  For further details see :doc:`../../../generic`. 

FRQNCY (FREQUENCY)
    Reference period. For further details see :doc:`../../../generic`.

MEASURES
~~~~~~~~

.. _odrstock:

STOCK (STCK)
    Market or fair value of the over the counter derivative.
    
STOCK IN EURO (EUR_STCK)
    odrstock_ in euro·

TRANSACTIONS (TRNSCTNS)
    Transactions net of any commissions and/or transaction taxes (**flow measure**). 

STRATEGY (STRTGY)
    Investment strategy for the derivative transaction choosing from ``DRVTV_STRTGY_ENUM``.


RESIDENTIAL_RE
--------------

Used to submit accounting data of residential real estate owned by the ``OA``.  Measure values are expressed in :ref:`currency <fscurrency>` except stated otherwise in the measure definition.


DIMENSIONS
~~~~~~~~~~

IID
    Identifier code of the residential real estate (:ref:`rre`).

DATE (DT)
    Reference date.  For further details see :doc:`../../../generic`. 

FRQNCY (FREQUENCY)
    Reference period. For further details see :doc:`../../../generic`.

MEASURES
~~~~~~~~~~

.. _rrestock:

STOCK (STCK)
    Market value or purchase value for residential real estate.

STOCK IN EURO (EUR_STCK)
    rrestock_ in euro·

TRANSACTIONS (TRNSCTNS)
    Amount for renovations (**flow variable**)·

ACCRUALS (ACCRLS)
    Accrued rents.

ARREARS (ARRRS)
    Rents in arrears.

WRITE-OFFS (WRT_OFFS)
    Rent write-offs


COMMERCIAL_RE
-------------

Used to submit accounting data of commercial real estate owned by the ``OA``.  Measure values are expressed in :ref:`currency <fscurrency>` except stated otherwise in the measure definition.

DIMENSIONS
~~~~~~~~~~
IID
    Identifier code of the residential real estate (:ref:`cre`).

DATE (DT)
    Reference date.  For further details see :doc:`../../../generic`. 

FRQNCY (FREQUENCY)
    Reference period. For further details see :doc:`../../../generic`.

MEASURES
~~~~~~~~~~

.. _crestock:

STOCK (STCK)
    Market value or purchase value for commercial real estate.

STOCK IN EURO (EUR_STCK)
    crestock_ in euro·

TRANSACTIONS (TRNSCTNS)
    Amount for renovations (**flow variable**)

ACCRUALS (ACCRLS)
    Accrued rents.

ARREARS (ARRRS)
    Rents in arrears.

WRITE-OFFS (WRT_OFFS)
    Rent write-offs

REM_FIXED
---------

Used to submit accounting data of remaining non financial assets owned by the ``OA``.  Measure values are expressed in :ref:`currency <fscurrency>` except stated otherwise in the measure definition.

DIMENSIONS
~~~~~~~~~~

TYPE (TYP)
    Type of remaining non financial asset choosing from ``BSI_RMNG_FXD_ENUM`` ·

COUNTRY (CNTRY)
    Location country of the non-financial asset choosing from ``GEN_CNTRY_ENUM`` ·

ID
    ``OA`` identifier code (:ref:`org`).

DATE (DT)
    Reference date.  For further details see :doc:`../../../generic`. 

FRQNCY (FREQUENCY)
    Reference period. For further details see :doc:`../../../generic`.


MEASURES
~~~~~~~~

.. _remstock:

STOCK (STCK)
    Value according to the valuation rules as described chapter 7 of ``ESA2010``.

STOCK IN EURO (EUR_STCK)
    remstock_ in euro.

TRANSACTIONS (TRNSCTNS)
    Amount for renovations (**flow variable**)·

ACCRUALS (ACCRLS)
    Accrued rents.

ARREARS (ARRRS)
    Rents in arrears.

WRITE-OFFS (WRT_OFFS)
    Rent write-offs

ASSET_REM
---------

Used to submit accounting data of remaining financial assets owned by the ``OA``.

DIMENSIONS
~~~~~~~~~~

ID
    ``OA`` identifier code (:ref:`org`).

COUNTERGROUP (CNTRGRP)
    Counterparty group choosing from ``GRP_CNTRGRP_ENUM`` ·

.. _aremcurrency:

CURRENCY (CRRNCY) 
    Grouped by currency of the remaining financial asset choosing from ``GEN_CNTRY_ENUM``.

DATE (DT)
    Reference date.  For further details see :doc:`../../../generic`. 

MEASURES
~~~~~~~~~~

.. _aremstock:

STOCK (STCK)
    Nominal value expressed in aremcurrency_·

STOCK IN EURO (EUR_STCK)
    aremstock_ in euro.



LIAB_SFT
--------

Used to submit account data of security financing transaction in which the ``OA`` has borrowed cash.  For the definition of a security financing transaction see :ref:`here <sft>`.  Measure values are expressed in :ref:`currency <sftcurrency>` of the transaction except stated otherwise in the measure definition.

DIMENSIONS
~~~~~~~~~~

IID
    Identifier code of the security financing transaction (:ref:`sft`).

DATE (DT)
    Reference date.  For further details see :doc:`../../../generic`. 

MEASURES
~~~~~~~~~~

.. _lsftstock:

STOCK (STCK)
    Amount of cash that the ``OA`` has borrowed in the transaction.

STOCK IN EURO (EUR_STCK)
    lsftstock_ in euro.
    

L_DEBT
------

Used to submit account data of debt instruments issued by the ``OA``.  For the definition of a debt instrument see :ref:`here <dbt>`.  Measure values are expressed in :ref:`currency <dbtcurrency>` of the debt instrument except stated otherwise in the measure definition.

DIMENSIONS
~~~~~~~~~~

IID
    Debt instrument identifier code (:ref:`dbt`).

ID
    Holder identifier code (:ref:`org`).

DATE (DT)
    Reference date.  For further details see :doc:`../../../generic`. 

FRQNCY (FREQUENCY)
    Reference period. For further details see :doc:`../../../generic`.

MEASURES
~~~~~~~~

.. _ldbtstock:

STOCK (STCK)
    Market value including accrued interest but not including interest arrears.

STOCK IN EURO (EUR_STCK)
    ldbtstock_ in euro.

TRANSACTIONS (TRNSCTNS)
    Transactions net of any commissions and/or transaction taxes (**flow measure**). 

NOMINAL STOCK (NMNL_STCK)
    Nominal value.

ACCRUALS (ACCRLS)
    Accrued interest

ARREARS (ARRRS)
    Interest arrears.


LOAN
----

Used to submit accounting data of loans received by the.  Measure values are expressed in :ref:`currency <loncurrency>` except stated otherwise in the measure definition.

DIMENSIONS
~~~~~~~~~~

IID
    Identifier code of the loan (:ref:`lon`).

DATE (DT)
    Reference date.  For further details see :doc:`../../../generic`. 


MEASURES
~~~~~~~~

.. _lonstock:

STOCK (STCK)
    Nominal value.

STOCK IN EURO (EUR_STCK)
    lonstock_ in euro·

UNDRAWN AMOUNT (UNDRN_AMNT)
    Undrawn amount.

WRITE-OFFS (WRT_OFFS)
    Write-offs by mutual agreement.

ACCRUALS (ACCRLS)
    Accrued interest.

ARREARS (ARRRS)
    Interest in arrears.


LIAB_REM
--------

Used to submit accounting data of remaining financial liabilities owed by the ``OA``.

DIMENSIONS
~~~~~~~~~~

ID
    ``OA`` identifier code (:ref:`org`).

COUNTERGROUP (CNTRGRP)
    Counterparty group choosing from ``GRP_CNTRGRP_ENUM`` ·

.. _lremcurrency:

CURRENCY (CRRNCY) 
    Grouped by currency of the remaining financial liability choosing from ``GEN_CNTRY_ENUM``.

DATE (DT)
    Reference date.  For further details see :doc:`../../../generic`. 


MEASURES
~~~~~~~~~~

.. _lremstock:

STOCK (STCK)
    Nominal value expressed in lremcurrency_·

STOCK IN EURO (EUR_STCK)
    lremstock_ in euro.


HOLDER
------

Used to submit accounting data regarding shares/investment fund units issued by the ``OA``.
Measure values are expressed in :ref:`currency <sishrcurrency>` of the share/investment fund unit unless stated otherwise in the measure definition.

DIMENSIONS
~~~~~~~~~~

IID
    Identifier code of the share/investment fund unit (:ref:`shr`).

ID
    Holder identifier code (:ref:`org`).

DATE (DT)
    Reference date.  For further details see :doc:`../../../generic`. 

FRQNCY (FREQUENCY)
    Reference period. For further details see :doc:`../../../generic`.


MEASURES
~~~~~~~~~~

QUANTITY (QNTTY)
    Number of shares/investment fund units. 

SUBSCRIPTIONS (SBSCRPTNS)
    Subscriptions gross of any commissions (**flow variable**).

SUBSCRIPTION CHARGES (SUB_CHRGS)
    Subscription commissions (**flow variable**).
    
REDEMPTIONS (RDMPTNS)
    Redemptions net of any commissions (**flow variable**).

REDEMPTION CHARGES (RED_CHRGS)
    Redemption commissions (**flow variable**).
