OTHER_KEY: Key Financial Data of Instruments owned by the OA
============================================================

Used to submit key financial data of instruments owned by the ``OA``.

Below the dimensions and the measures are described and if needed the attributes of the measures for each table of the data category. 

SHARE
-----

Used to submit periodic key financial data of shares/investment fund units owned by the ``OA``.

DIMENSIONS
~~~~~~~~~~

ID
    Identifier code of the share/investment fund unit (:ref:`shr`).

DATE (DT)
    Reference date.  For further details see :doc:`../../../generic`. 

MEASURES
~~~~~~~~

PRICE (PRC)
    Price.  In case of a listed security closing price is provided.


DIVIDEND
--------

Used to provide data about dividends distributed by shares/investment fund units owned by the ``OA``.


DIMENSIONS
~~~~~~~~~~
ID
    Identifier code of the share/investment fund unit (:ref:`shr`).

DATE (DT)
    Date at which the ``OA`` checks its books to find its investors.  An investor must be recorded in this date to be eligible for the dividend.

MEASURES
~~~~~~~~~~
TYPE (TYP)
    Dividend type choosign from ``DVDND_TYP_ENUM``.

.. _currency_div:

CRRNCY (CURRENCY)
    Dividend transaction currency choosing from ``GEN_CRRNCY_ENUM`` (if applicable).

AMOUNT (AMNT)
    Amount expressed in currency_div_ in case of monetary dividend payments.

SPLIT
-----

Used to provide data regarding splits and reverse splits of shares/investment fund units owned by the ``OA``.

DIMENSIONS
~~~~~~~~~~
ID
    Identifier code of the share/investment fund unit (:ref:`shr`).


DATE (DT)
    Date of split/reverse-split.

MEASURES
~~~~~~~~

FACTOR (FCTR)
    Factor ratio defined as number of shares before the split/reverse-split divided by the number of shares after the split/reverse-split.

DEBT
----

Used to submit key financial data regarding the debt instruments owned by the ``OA``.

DIMENSIONS
~~~~~~~~~~
ID
    Identifier code of the share/investment fund unit (:ref:`shr`).

DATE (DT)
    Reference date. For further details see :doc:`../../../generic`. 

MEASURES
~~~~~~~~~~

PRICE (PRC)
    Price (closing price) expressed as a percentage of the nominal price.  For coupon-bonds accrued interest is not included in the price.

ACCRUED INTEREST (ACCRD_INTRST)
    For coupon payment bonds accrued interest as a percentage of the nominal
    price is provided computed from the last coupon payment or the start date
    of the coupon payment.

COUPON
------

Used to submit data regarding coupon payments on debt securities owned by the ``OA``.

DIMENSIONS
~~~~~~~~~~

ID
    Identifier code of the share/investment fund unit (:ref:`shr`).

DATE (DT)
    Coupon payment date.

MEASURES
~~~~~~~~~~

RATE (RT)
    Annualized coupon interest rate.

EXT_DERIVATIVE
--------------

Used to submit price data regarding exchange traded derivatives owned by the ``OA``.

DIMENSIONS
~~~~~~~~~~
ID
    Identifier code of the exchange traded derivative (:ref:`edr`)·

DATE (DT)
    Reference date.  For further details see :doc:`../../../generic`. 
    
MEASURES
~~~~~~~~

PRICE (PRC)
    Closing price.


OTC_DERIVATIVE
--------------

Used to submit price data regarding over the counter derivatives owned by the ``OA``.

DIMENSIONS
~~~~~~~~~~
ID
    Identifier code of the over the counter derivative (:ref:`edr`)·

DATE (DT)
    Reference date.  For further details see :doc:`../../../generic`. 
    

MEASURES
~~~~~~~~~~

PRICE (PRC)
    Price.
