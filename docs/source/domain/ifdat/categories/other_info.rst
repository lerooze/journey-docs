OTHER_INFO: Other Information Data 
==================================

Used to provide information data about:

* the financial assets owned by the ``OA``. 

* issuers of the financial assets owned by the ``OA``.

* real estate owned by the ``OA``. 

* the holders of eqyity/fund units/bonds issued by the ``OA``. 

Below dimensions and measures of each table are discussed:

ISSUER
------

Used to provide information data regarding the issuers of financial assets
owned by the ``OA``.  The measures of this table can take at most one value
during the issuer lifecycle.  There is no need to resubmit the data on an
issuer in case related data have already been submitted in :doc:`self_info` 

DIMENSIONS
~~~~~~~~~~

ID
    Issuer identification code (:ref:`org`).


MEASURES
~~~~~~~~

BIRTHDATE (DT_BRTH)
    Birth date if known.

CLOSEDATE (DT_CLS)
    Close date if known and if applicable.

ESCB ID (ESCB_ID)
    Identifier code that is assigned by the ``ESCB`` known also as the ``RIAD code``.

LEI ID (LEI_ID)
    Identifier code based on the ISO-17442 standard.

TAX ID (TAX_ID)
    Tax identifier code of the format ``{CC}{CODE}`` where ``CC`` is a
    placeholder for  ISO 3166-1 alpha-2 country code that has issued the the
    tax code and ``CODE`` is a placeholder for the actual tax code without the
    country code in case it starts with it.

NBR ID (NBR_ID)
    Business identifier code of the format ``{CC}{CODE}`` where ``CC`` is a
    placeholder for  ISO 3166-1 alpha-2 country code that has issued the the
    code and ``CODE`` is a placeholder for the actual business identifier code
    without the country code in case it starts with it.

INTERNAL ID (INTRNL_ID)
    Internal identifier formatted as ``{UID}_{CODE}`` where ``CODE`` is a
    placeholder for the code that the ``RA`` has assigned to the issuer.

INTERNATIONAL ORGANISATION (INTRNTNL_ORGNSTN)
    In case of international organisation choose from ``ORG_INTRNTNL_ORGNZTN_CD_ENUM``.

SPLIT FROM (SPLT_FRM)
    In case the issuer was created by a corporate split the identifier code of
    the counterpart entity of the split is provided (:ref:`org`). 

MERGED WITH (MRGD_WTH)
    In case of closure of the issuer via a merger event the identifier code of
    the entity that the issuer merged with is provided (:ref:`org`).

DEDUPLICATE OF (DDPLCT_OF)
    In case the ``RA`` of the ``OA`` changes it is used to deduplicate internal
    (:ref:`org`) ids assigned by the old ``RA`` with those assigned by the new
    ``OA``.

STATIC_ISSUER
-------------
Used to provide information data regarding the issuers of financial assets
owned by the ``OA``.  The measures of this table can change during the issuer lifecycle.
There is no need to resubmit the data on an
issuer in case related data have already been submitted in :doc:`self_info` 

DIMENSIONS
~~~~~~~~~~

ID
    Issuer identification code (:ref:`org`).

VALID FROM (VLD_FRM)
    Date from which the measure values are valid.  
    For further details see :doc:`../../../generic`. 

VALID TO (VLD_T)
    Date to which the measure values are valid.  
    For further details see :doc:`../../../generic`. 

MEASURES
~~~~~~~~~~

NAME (NM)
    Official name.

COUNTRY OF RESIDENCE (CNTRY_RSDNC)
    Country of residence choosing from ``GEN_CNTRY_ENUM``. 
    
LEGAL PROCEEDINGS STATUS (LGL_PRCDNG_STTS)
    Status of legal proceedings choosing from ``ORG_LGL_PRCDNG_STTS_ENUM``.

INSTITUTIONAL SECTOR (INSTTTNL_SCTR)
    Institutional sector choosing from ``ORG_INSTTTNL_SCTR_ENUM`` defined in ESA2010.

ECONOMIC ACTIVITY (ECNMC_ACTVTY)
    Economic activity choosing from ``ORG_ECNMC_ACTVTY_TYP_ENUM``. 


HOLDER
------
Used to provide information data regarding the holders of instruments issued by
the ``OA``.  The measures of this table can take at most one value during the
holder lifecycle.  There is no need to resubmit the data on a holder in case
related data have already been submitted in :doc:`self_info` or in ISSUER_. 


DIMENSIONS
~~~~~~~~~~

ID
    Holder identification code (:ref:`org`).

MEASURES
~~~~~~~~

BIRTHDATE (DT_BRTH)
    Birth date if known.

CLOSEDATE (DT_CLS)
    Close date if known and if applicable.

ESCB ID (ESCB_ID)
    Identifier code that is assigned by the ``ESCB`` known also as the ``RIAD code``.

LEI ID (LEI_ID)
    Identifier code based on the ISO-17442 standard.

TAX ID (TAX_ID)
    Tax identifier code of the format ``{CC}{CODE}`` where ``CC`` is a
    placeholder for  ISO 3166-1 alpha-2 country code that has issued the the
    tax code and ``CODE`` is a placeholder for the actual tax code without the
    country code in case it starts with it.

NBR ID (NBR_ID)
    Business identifier code of the format ``{CC}{CODE}`` where ``CC`` is a
    placeholder for  ISO 3166-1 alpha-2 country code that has issued the the
    code and ``CODE`` is a placeholder for the actual business identifier code
    without the country code in case it starts with it.

INTERNAL ID (INTRNL_ID)
    Internal identifier formatted as ``{UID}_{CODE}`` where ``CODE`` is a
    placeholder for the code that the ``RA`` has assigned to the issuer.

INTERNATIONAL ORGANISATION (INTRNTNL_ORGNSTN)
    In case of international organisation choose from ``ORG_INTRNTNL_ORGNZTN_CD_ENUM``.

SPLIT FROM (SPLT_FRM)
    In case the holder was created by a corporate split the identifier code of
    the counterpart entity of the split is provided (:ref:`org`). 

MERGED WITH (MRGD_WTH)
    In case of closure of the issuer via a merger event the identifier code of
    the entity that the issuer merged with is provided (:ref:`org`).

DEDUPLICATE OF (DDPLCT_OF)
    In case the ``RA`` of the ``OA`` changes it is used to deduplicate internal
    (:ref:`org`) ids assigned by the old ``RA`` with those assigned by the new
    ``OA``.
    
STATIC_HOLDER
-------------
Used to provide information data regarding the holders of instruments issued by
the ``OA``.  The measures of this table can change during the
holder lifecycle.  There is no need to resubmit the data on a holder in case
related data have already been submitted in :doc:`self_info` or in STATIC_ISSUER_. 

DIMENSIONS
~~~~~~~~~~

ID
    Holder identification code (:ref:`org`).

VALID FROM (VLD_FRM)
    Date from which the measure values are valid.  
    For further details see :doc:`../../../generic`. 

VALID TO (VLD_T)
    Date to which the measure values are valid.  
    For further details see :doc:`../../../generic`. 

MEASURES
~~~~~~~~~~

NAME (NM)
    Name.

COUNTRY OF RESIDENCE (CNTRY_RSDNC)
    Country of residence choosing from ``GEN_CNTRY_ENUM``. 

INSTITUTIONAL SECTOR (INSTTTNL_SCTR)
    Institutional sector choosing from ``ORG_INSTTTNL_SCTR_ENUM`` defined in ESA2010.


DEPOSIT
-------

Used to submit data regarding regarding the deposit accounts of the ``OA``.
The measures of this table can take at most one value during the lifecycle of the deposit account.

DIMENSIONS
~~~~~~~~~~

ID
    Deposit identifier code (:ref:`dep`).

MEASURES
~~~~~~~~~~

BIRTHDATE (DT_BRTH)
    Issue date, activation date, initialization date.

.. _oidepclose:

CLOSEDATE (DT_CLS)
    Close date (if applicable).

IBAN ID (IBAN_ID)
    Identifier code according to the IBAN standard.

INTERNAL ID (INTRNL_ID)
    Internal identifier formatted as ``{UID}_{CODE}`` where ``CODE`` is a
    placeholder for the code that the ``RA`` has assigned to the deposit account.

TYPE (TYP)
    Type choosing from ``DEP_TYP_ENUM``.

PERIOD OF NOTICE (NTC)
    Notice period choosing from ``DEP_NTC_ENUM``.

.. _depcurrency:

CURRENCY (CRRNCY)
    Currency of transaction choosing from ``GEN_CNTRY_ENUM``.

IS TRANSFERABLE (IS_TRNSFRBL)
    Transferable flag.

IS SHARED (IS_SHRD)
    Shared account flag.

DEDUPLICATE OF (DDPLCT_OF)
    In case the ``RA`` of the ``OA`` changes it is used to deduplicate internal
    (:ref:`dep`) ids assigned by the old ``RA`` with those assigned by the new
    ``OA``.


STATIC_DEPOSIT
--------------
Used to submit data regarding regarding the deposit accounts of the ``OA``.
The measures of this table can change during the
lifecycle of the deposit account.


DIMENSIONS
~~~~~~~~~~

ID
    Deposit identifier code (:ref:`dep`).

VALID FROM (VLD_FRM)
    Date from which the measure values are valid.  
    For further details see :doc:`../../../generic`. 

VALID TO (VLD_T)
    Date to which the measure values are valid.  
    For further details see :doc:`../../../generic`. 

MEASURES
~~~~~~~~

MATURITY DATE (MTRTY_DT) 
    Maturity date (if applicable).  It is possible that this date can change.  In this case oidepclose_ is updated.

NOMINAL INTEREST (NMNL_INTRST) 
    Nominal annualized interest rate.

COMPOUND TIMES (CMPND_TMS)
    Number of compounds in one year.
    Αριθμός ανατοκισμών σε ένα έτος·

DEBTOR (DBTR) 
    Identifier code of the credit institution that maintains the deposit account (:ref:`org`)

CREDITOR (CRDTR) 
    Identifier code of the ``OA`` that owns this deposit account (:ref:`org`)


SFT
---

Used to provide information data for security financing transactions that involve the ``OA``.  The measures of this table can take at most one value during the lifecycle of the security financing transaction. 

DIMENSIONS
~~~~~~~~~~

ID
    Idenitfier code of the security financing transaction (:ref:`sft`).


MEASURES
~~~~~~~~~~

BIRTHDATE (DT_BRTH)
    Creation date.

.. _oisftclose:

CLOSEDATE (DT_CLS)
    Maturity date.

INTERNAL ID (INTRNL_ID) 
    Internal identifier formatted as ``{UID}_{CODE}`` where ``CODE`` is a
    placeholder for the code that the ``RA`` has assigned to the security
    financing transaction.

.. _sftcurrency:

CURRENCY (CRRNCY) 
    Currency of transaction choosing from ``GEN_CNTRY_ENUM`` (applicable if one side of the transaction involves cash or cash equivalent).

TYPE (TYP)
    Type choosing from ``SFT_TYP_ENUM`` ·

DEDUPLICATE OF (DDPLCT_OF)
    In case the ``RA`` of the ``OA`` changes it is used to deduplicate internal
    (:ref:`sft`) ids assigned by the old ``RA`` with those assigned by the new
    ``OA``.



STATIC_SFT
----------

Used to provide information data for security financing transactions that involve the ``OA``. 
The measures of this table can change during the
lifecycle of the security financing transaction.

DIMENSIONS
~~~~~~~~~~

ID
    Idenitfier code of the security financing transaction (:ref:`sft`).

VALID FROM (VLD_FRM)
    Date from which the measure values are valid.  
    For further details see :doc:`../../../generic`. 

VALID TO (VLD_T)
    Date to which the measure values are valid.  
    For further details see :doc:`../../../generic`. 

MEASURES
~~~~~~~~

MATURITY DATE (MTRTY_DT) 
    Maturity date (if applicable).  It is possible that this date can change.  In this case oisftclose_ is updated.

NOMINAL INTEREST (NMNL_INTRST) 
    Annualized nominal interest rate in case one side of the transacion
    involves cash or cash equivalent.  The net interest rate is provided
    subtracting any annualized interest rate of debt instruments belonging to
    the other side of the transaction. 

DEBTOR (DBTR) 
    Identifier code of the entity that has temporarily lent debt instruments and in the case that the transaction involves cash or cash equivalent has borrowed cash (:ref:`org`).

CREDITOR (CRDTR) 
    Identifier code of the entity that has temporarily borrowed debt instruments and in the case that the transaction involves cash or cash equivalent has lent cash (:ref:`org`).


DEBT
----

Used to provide information data for debt instruments owned by the ``OA``.  
The measures of this table can take at most one value during the lifecycle of the debt instrument. 

DIMENSIONS
~~~~~~~~~~

ID
    Debt instrument identifier code (:ref:`dbt`).

MEASURES
~~~~~~~~~~

.. _other_debt_birth:

BIRTHDATE (DT_BRTH)
    Issue date.

.. _other_debt_close:

CLOSEDATE (DT_CLS)
    Maturity date/redumption date (if applicable)

ORIGINAL MATURITY (ORGNL_MTRTY)
    Original maturity date/redumption date (if applicable).

ISIN ID (ISIN_ID) 
    Debt identifier code based on the ISIN ISO-6166 standard.

INTERNAL ID (INTRNL_ID) 
    Internal identifier formatted as ``{UID}_{CODE}`` where ``CODE`` is a
    placeholder for the code that the ``RA`` has assigned to the debt instrument.

.. _dbtcurrency:

CURRENCY (CRRNCY) 
    Currency of transaction choosing from ``GEN_CNTRY_ENUM``.

ISSUE PRICE (ISS_PRC)
    Issue price given as a percentage of the nominal price.

REDEMPTION PRICE (RDMPTN_PRC)
    Redemption price given as a percentage fo the nominal price.

MARKET (MRKT)
    Trading market choosing from ``GEN_MRKT_ENUM`` based on the ISO-10383 standard.

ACCRUAL STARTDATE (ACCRL_STRTDT)
    Accrual start date.  In case of a couponless debt instrument the value of 
    other_debt_birth_ is provided.

PRIMARY CLASS (PRMRY_CLSS)
    Primary class choosing from ``DBT_PRMRY_ENUM``.

GUARANTEE LEVEL (GRNT_LVL)
    Guarantee level choosing from ``DBT_GRNT_LVL_ENUM``.
    
RANK LEVEL (RNK_LVL)
    Rank level choosing from ``DBT_RNK_LVL_ENUM``.

SECURITY LEVEL (SCRTY_LVL)
    Security level choosing from ``DBT_SCRTY_LVL_ENUM``.

IS SECURITIZATION (IS_SCRTZTN)
    Securitization flag as defined in ECB/2015/15.

SECURITIZATION TYPE (SCRTZTN_TYP)
    Securitization type choosing from ``DBT_SCRTZTN_TYP_ENUM``.

IS COVERED (IS_CVRD)
    Covered flag as defined in ECB/2014/60.

COVERED TYPE (CVRD_TYP)
    Covered type choosing from ``DBT_CVRD_TYP_ENUM``.

COUPON TYPE (CPN_TYP)
    Coupon type choosing from ``DBT_CVRD_TYP_ENUM``.

COUPON CURRENCY (CPN_CRRNCY)
    Coupon currency choosing from ``GEN_CRRNCY_ENUM`` ·

COUPON FREQUENCY (CPN_FRQNCY)
    Coupon payment frequency choosing from ``DBT_CPN_FRQNCY_ENUM``.

COUPON RATE SPREAD (CPN_SPRD)
    Coupon rate spread given in basis points.

COUPON MULTIPLIER (CPN_MLTPLR)
    Coupon rate multiplier.

COUPON CAP (CPN_CP)
    Maximum coupon rate.

COUPON FLOOR (CPN_FLR)
    Minimum coupon rate.

FIRST COUPON DATE (FRST_CPN_DT)
    Date of first coupon payment.

LAST COUPON DATE (LST_CPN_DT)
    Date of last coupon payment.

UNDERLYING INSTRUMENT (UNDRLYNG)
    Underlying debt instrument that the coupon payment depends on (:ref:`dbt`).

DEDUPLICATE OF (DDPLCT_OF)
    In case the ``RA`` of the ``OA`` changes it is used to deduplicate internal
    (:ref:`dbt`) ids assigned by the old ``RA`` with those assigned by the new
    ``OA``.


STATIC_DEBT
-----------

Used to submit information data regarding debt instruments owned by the
``OA``.  
The measures of this table can change during the lifecycle of the debt instrument.

DIMENSIONS
~~~~~~~~~~

ID
    Debt instrument identifier code (:ref:`dbt`).

VALID FROM (VLD_FRM)
    Date from which the measure values are valid.  
    For further details see :doc:`../../../generic`. 

VALID TO (VLD_T)
    Date to which the measure values are valid.  
    For further details see :doc:`../../../generic`. 

MEASURES
~~~~~~~~~~

NAME (NM) 
    Name.

STATUS (STTS) 
    Instrument status choosing from ``DBT_STTS_ENUM``.
    
MATURITY DATE (MTRTY_DT) 
    Maturity or redumption date (if applicable).  In some rare circumstances this date can change during the lifecycle of the instrument and in this case other_debt_close_ is updated.

ISSUED BY (ISSD_BY)
    Issuer identification code (:ref:`org`).


LOAN
----

Used to submit data regarding regarding loans given to the ``OA``.
The measures of this table can take at most one value during the lifecycle of the loan.


DIMENSIONS
~~~~~~~~~~

ID
    Loan identifier code (:ref:`lon`).

MEASURES
~~~~~~~~~~

BIRTHDATE (DT_BRTH)
    Date at which the loan credit contract becomes binding.  For loans without a contract the date at which the debtor receives the money from the creditor is given.

.. _oilonclose:

CLOSEDATE (DT_CLS)
    Maturity or redumption date.

INTERNAL ID (INTRNL_ID) 
    Internal identifier formatted as ``{UID}_{CODE}`` where ``CODE`` is a
    placeholder for the code that the ``RA`` has assigned to the loan.

.. _loncurrency:

CURRENCY (CRRNCY) 
    Currency of transaction choosing from ``GEN_CNTRY_ENUM``.

TYPE (TYP)
    Type choosing from ``LOAN_ENUM``.

DEDUPLICATE OF (DDPLCT_OF)
    In case the ``RA`` of the ``OA`` changes it is used to deduplicate internal
    (:ref:`lon`) ids assigned by the old ``RA`` with those assigned by the new
    ``OA``.



STATIC_LOAN
-----------
Used to submit data regarding regarding loans given to the ``OA``.
The measures of this table can change during the lifecycle of the loan.

DIMENSIONS
~~~~~~~~~~

ID
    Loan identifier code (:ref:`lon`).

VALID FROM (VLD_FRM)
    Date from which the measure values are valid.  
    For further details see :doc:`../../../generic`. 

VALID TO (VLD_T)
    Date to which the measure values are valid.  
    For further details see :doc:`../../../generic`. 

MEASURES
~~~~~~~~~~

MATURITY DATE (MTRTY_DT) 
    Maturity or redumption date (if applicable).  In some rare circumstances this date can change during the lifecycle of the loan and in this case oilonclose_ is updated.

NOMINAL INTEREST (NMNL_INTRST) 
    Annualized nominal interest rate.  In the case of credit card loan the average of the convenience credit interest rate and extended credit interest rate is given weighted by the respective amounts.

DEBTOR (DBTR) 
    Identifier code of the ``OA`` that has received the loan.

CREDITOR (CRDTR) 
    Identifier code of the entity that gave the loan, the creditor.


SHARE
-----

Used to submit information data regarding equity/investment fund shares owned 
by the ``OA``.  The measures of this table can take at most one value during
the lifecycle of the debt instrument.


DIMENSIONS
~~~~~~~~~~

ID
    Identifier code of the share/investment fund unit (:ref:`shr`).

MEASURES
~~~~~~~~~~

BIRTHDATE (DT_BRTH)
    Issue date, activation date, initialization date.

CLOSEDATE (DT_CLS)
    Close date (if applicable).

ISIN ID (ISIN_ID) 
    Instrument identifier based on the ISIN ISO-6166 standard.

INTERNAL ID (INTRNL_ID) 
    Internal identifier formatted as ``{UID}_{CODE}`` where ``CODE`` is a
    placeholder for the code that the ``RA`` has assigned to the share/investment fund unit.

.. _shrcurrency:

CURRENCY (CRRNCY) 
    Currency of transaction choosing from ``GEN_CNTRY_ENUM``.

MARKET (MRKT)
    Trading market choosing from ``GEN_MRKT_ENUM`` based on the ISO-10383 standard.
    
TYPE (TYP)
    Type choosing from ``SHR_TYP_ENUM``.

PRIMARY CLASS (PRMRY_CLSS)
    Primary class choosing from ``SHR_PRMRY_CLSS_ENUM``.

DEDUPLICATE OF (DDPLCT_OF)
    In case the ``RA`` of the ``OA`` changes it is used to deduplicate internal
    (:ref:`shr`) ids assigned by the old ``RA`` with those assigned by the new
    ``OA``.


STATIC_SHARE
------------

Used to submit information data regarding equity/investment fund shares owned  
by the ``OA``.  
The measures of this table can change during the lifecycle of the share/investment fund unit.

DIMENSIONS
~~~~~~~~~~

ID
    Identifier code of the share/investment fund unit (:ref:`shr`).

VALID FROM (VLD_FRM)
    Date from which the measure values are valid.  
    For further details see :doc:`../../../generic`. 

VALID TO (VLD_T)
    Date to which the measure values are valid.  
    For further details see :doc:`../../../generic`. 

MEASURES
~~~~~~~~~~

NAME (NM) 
    Name. 

ISSUED BY (ISSD_BY)
    Issuer identification code (:ref:`org`).


EXT_DER
-------

Used to submit information data regarding exchange traded derivatives traded by the by the ``OA``.  

DIMENSIONS
~~~~~~~~~~

ID
    Identifier code of the exchange traded derivative (:ref:`edr`).

MEASURES
~~~~~~~~
BIRTHDATE (DT_BRTH)
    Issue date, activation date, initialization date.

CLOSEDATE (DT_CLS)
    Maturity date (if applicable).

NAME (NM) 
    Name.

ISIN ID (ISIN_ID) 
    Instrument identifier based on the ISIN ISO-6166 standard.

TICKER (TCKR)
    Identifier code that is given by the market at which the derivative is traded.

INTERNAL ID (INTRNL_ID) 
    Internal identifier formatted as ``{UID}_{CODE}`` where ``CODE`` is a
    placeholder for the code that the ``RA`` has assigned to the derivative.

TYPE (TYP)
    Type choosing from ``DRVTV_TYP_ENUM``.

.. _edrcurrency:

CURRENCY (CRRNCY) 
    Currency of transaction choosing from ``GEN_CNTRY_ENUM``.

MULTIPLIER (MLTPLR)
    The multiplier of the derivative.
    
WRITER (WRTR)
    The main counterparty for the exchange traded derivative choosing from  ``GEN_MRKT_ENUM`` that is derived from ISO-10383 standard.

DEDUPLICATE OF (DDPLCT_OF)
    In case the ``RA`` of the ``OA`` changes it is used to deduplicate internal
    (:ref:`edr`) ids assigned by the old ``RA`` with those assigned by the new
    ``OA``.

OTC_DER
-------

Used to submit information data regarding over the counter derivatives traded by the by the ``OA``.  

DIMENSIONS
~~~~~~~~~~

ID
    Identifier code of the over the counter derivative (:ref:`odr`).

MEASURES
~~~~~~~~~~

BIRTHDATE (DT_BRTH)
    Issue date, activation date, initialization date.

CLOSEDATE (DT_CLS)
    Maturity date (if applicable).

NAME (NM)
    Name.

INTERNAL ID (INTRNL_ID)
    Internal identifier formatted as ``{UID}_{CODE}`` where ``CODE`` is a
    placeholder for the code that the ``RA`` has assigned to the derivative.

TYPE (TYP)
    Type choosing from ``DRVTV_TYP_ENUM``.

.. _odrcurrency:

CURRENCY (CRRNCY)
    Currency of transaction choosing from ``GEN_CNTRY_ENUM``.

MULTIPLIER (MLTPLR)
    The multiplier of the derivative.
    
WRITER (WRTR)
    Identifier code of the party that writes and sells the derivative (:ref:`org`).

BUYER (BYR)
    Identifier code of the party that buys the derivative (:ref:`org`).

DEDUPLICATE OF (DDPLCT_OF)
    In case the ``RA`` of the ``OA`` changes it is used to deduplicate internal
    (:ref:`odr`) ids assigned by the old ``RA`` with those assigned by the new
    ``OA``.

RES_RE
------

Used to submit information data regarding residential real estate owned by the ``OA``.

DIMENSIONS
~~~~~~~~~~

ID
    Identifier code of the residential real estate (:ref:`rre`).

MEASURES
~~~~~~~~~~

NATIONAL ID (NTNL_ID)
    National identifier code formatted as ``{CC}{CODE}`` where position ``CC`` is a placeholder for the ISO 3166-1 alpha-2 code of the country that issues the code and ``CODE`` is the actual code without country code if it starts with it.  

INTERNAL ID (INTRNL_ID) 
    Internal identifier formatted as ``{UID}_{CODE}`` where ``CODE`` is a
    placeholder for the code that the ``RA`` has assigned to the residential real estate.

COUNTRY (CNTRY)
    Location country of the real estate choosing from ``GEN_CNTRY_ENUM``.

.. _res_type:

TYPE (TYP)
    Type choosing from ``RRE_TYPE_ENUM`` ·

CITY (CTY)
    City/area.

POSTAL CODE (PSTL_CD)
    Postal code.

TERRITORY (TRRTRY)
    Territory choosing from ``GEN_NUTS_ENUM`` ·

DEDUPLICATE OF (DDPLCT_OF)
    In case the ``RA`` of the ``OA`` changes it is used to deduplicate internal
    (:ref:`rre`) ids assigned by the old ``RA`` with those assigned by the new
    ``OA``.


ORG_TO_RRE
----------

Used to submit data regarding ownership links between ``OA`` and residential real estate.

DIMENSIONS
~~~~~~~~~~

LID
    Identifier code of the owner (:ref:`org`).

RID
    Identifier code of the residential real estate (:ref:`rre`).

VALID FROM (VLD_FRM)
    Date from which the measure values are valid.  
    For further details see :doc:`../../../generic`. 

VALID TO (VLD_T)
    Date to which the measure values are valid.  
    For further details see :doc:`../../../generic`. 

MEASURES
~~~~~~~~~~

IS OWNER (IS_OWNR)
    Flag that the ``OA`` identified by ``LID`` code owns real estate identified with ``RID`` code.

RATE (RT)
    Ownership rate that ``OA`` with identifier code ``LID`` has on residential real estate with identifier code ``RID``.


COM_RE
------

Used to submit information data regarding commercial real estate owned by the ``OA``.

DIMENSIONS
~~~~~~~~~~

ID
    Identifier code of the commercial real estate (:ref:`cre`).

MEASURES
~~~~~~~~~~

NATIONAL ID (NTNL_ID)
    National identifier code formatted as ``{CC}{CODE}`` where position ``CC`` is a placeholder for the ISO 3166-1 alpha-2 code of the country that issues the code and ``CODE`` is the actual code without country code if it starts with it.  

INTERNAL ID (INTRNL_ID) 
    Internal identifier formatted as ``{UID}_{CODE}`` where ``CODE`` is a
    placeholder for the code that the ``RA`` has assigned to the commercial real estate.

COUNTRY (CNTRY)
    Location country of the real estate choosing from ``GEN_CNTRY_ENUM``.

.. _com_type:

TYPE (TYP)
    Type choosing from ``CRE_TYPE_ENUM`` ·

CITY (CTY)
    City/area.

POSTAL CODE (PSTL_CD)
    Postal code.

TERRITORY (TRRTRY)
    Territory choosing from ``GEN_NUTS_ENUM`` ·

DEDUPLICATE OF (DDPLCT_OF)
    In case the ``RA`` of the ``OA`` changes it is used to deduplicate internal
    (:ref:`cre`) ids assigned by the old ``RA`` with those assigned by the new
    ``OA``.

ORG_TO_CRE
----------

Used to submit data regarding ownership links between ``OA`` and commercial real estate.

DIMENSIONS
~~~~~~~~~~

LID
    Identifier code of the owner (:ref:`org`).

RID
    Identifier code of the commercial real estate (:ref:`cre`).

VALID FROM (VLD_FRM)
    Date from which the measure values are valid.  
    For further details see :doc:`../../../generic`. 

VALID TO (VLD_T)
    Date to which the measure values are valid.  
    For further details see :doc:`../../../generic`. 

MEASURES
~~~~~~~~~~

IS OWNER (IS_OWNR)
    Flag that the ``OA`` identified by ``LID`` code owns real estate identified with ``RID`` code.

RATE (RT)
    Ownership rate that ``OA`` with identifier code ``LID`` has on commercial real estate with identifier code ``RID``.
