SELF_INFO: Self Information Data 
================================

It is used for the submission of information data regarding the ``OA``, the
instruments issued by the ``OA``, the ``RA`` in case it is different from the
``OA`` and the contact person responsible for submitting data on behalf of the
``RA``.

Below the dimensions and the measures are provided for each table of the data category.

FUND
----

Used to submit information data regarding the ``OA``.  The measures of this table have at most one
value during the life cycle of the ``OA``.

DIMENSIONS
~~~~~~~~~~

ID
    Identifier code of the ``OA`` (:ref:`org`).

MEASURES
~~~~~~~~~~

BIRTHDATE (DT_BRTH)
    Birth date.

CLOSEDATE (DT_CLS)
    Close date (if applicable).

COUNTRY OF BIRTH (CNTRY_BRTH)
    Country of incorporation choosing from ``GEN_CNTRY_ENUM``.

ESCB ID (ESCB_ID)
    Identifier code that is assigned by the ``ESCB`` known also as the ``RIAD code``.

LEI ID (LEI_ID)
    Identifier code based on the ISO-17442 standard.

TAX ID (TAX_ID)
    Tax identifier code of the format ``{CC}{CODE}`` where ``CC`` is a
    placeholder for  ISO 3166-1 alpha-2 country code that has issued the
    tax code and ``CODE`` is a placeholder for the actual tax code without the
    country code in case it starts with it.

NBR ID (NBR_ID)
    Business identifier code of the format ``{CC}{CODE}`` where ``CC`` is a
    placeholder for  ISO 3166-1 alpha-2 country code that has issued the
    code and ``CODE`` is a placeholder for the actual business identifier code
    without the country code in case it starts with it.

SPLIT FROM (SPLT_FRM)
    In case the ``OA`` was created by a corporate split the identifier code of
    the entity that it was split from is provided (:ref:`org`). 

MERGED WITH (MRGD_WTH)
    In case of closure of the ``OA`` via a merger event the identifier code of
    the entity that the ``OA`` merged with is provided (:ref:`org`).


STATIC_FUND
-----------

Used to submit information data regarding the ``OA``.  The measures of this table can change during
the life cycle of the entity.

DIMENSIONS
~~~~~~~~~~

ID
    Identifier code of the ``OA`` (:ref:`org`).

VALID FROM (VLD_FRM)
    Date from which the measure values are valid.  
    For further details see :doc:`../../../generic`. 

VALID TO (VLD_T)
    Date to which the measure values are valid.  
    For further details see :doc:`../../../generic`. 

MEASURES
~~~~~~~~~~

NAME (NM)
    Official name·

LATIN NAME (NM_LTN)
    Official name using Latin characters.

SHORT NAME (NM_SHRT)
    Short name.

STREET (STRT)
    Street address, street number and area.  Applicable for ``OA`` that do not
    have a management company.

LATIN STREET (STRT_LTN)
    Street address, street number and area using Latin characters.  Applicable
    for ``OA`` that do not have a management company.

CITY (CTY)
    City, village.  Applicable for ``OA`` that do not have a management company.

LATIN CITY (CTY_LTN)
    City, village using Latin characters.  Applicable for ``OA`` that do not
    have a management company.

POSTAL CODE (PSTL_CD)
    Postal code.  Applicable for ``OA`` that do not have a management company.

POSTAL BOX (PSTL_BX)
    Postal box.  Applicable for ``OA`` that do not have a management company.

URL
    Web address (if applicable).

EMAIL
    Email (if applicable).

COUNTRY OF RESIDENCE (CNTRY_RSDNC)
    Country of residence choosing from ``GEN_CNTRY_ENUM``. 

IS LISTED (IS_LSTD)
    Listed flag.

IS INVESTMENT GRADED (IS_INVSTMNT_GRDD)
    Investment graded flag.  Applicable for legal entities ``OA``.

IS INACTIVE (IS_INCTV)
    Inactivity flag.

IS UNDER LIQUIDATION (IS_UNDR_LQDTN)
    Liquidation flag.
    
LEGAL PROCEEDINGS STATUS (LGL_PRCDNG_STTS)
    Status of legal proceedings choosing from ``ORG_LGL_PRCDNG_STTS_ENUM``.

ACCOUNTS CURRENCY (ACCNTS_CRRNCY)
    Financial statements currency choosing from ``GEN_CNTRY_ENUM``.

INSTITUTIONAL SECTOR CONTROL (INSTTTNL_SCTR_CNTRL)
    Institutional sector control choosing from ``ORG_INSTTTNL_SCTR_CNTRL_ENUM``
    as defined in ESA2010 Chapter 2.
    
SIZE (SZ)
    Entity size choosing from ``ORG_SZ_ENUM`` according to ``Annex
    to Commission Recommendation 2033/361/EC``.
        
LEGAL FORM (LGL_FRM)
    Legal form choosing from ``ORG_LGL_FRM_ENUM``.

TYPE OF SUPERVISION (TYP_SPRVSN)
    Type of supervision choosing from ``ORG_SPRVSN_TYP_ENUM``.

.. _fscurrency:

MANAGED BY (MNGD_BY)
    Management company identifier code (if applicable) (:ref:`org`).

REPORTED BY (RPRTD_BY)
    Identifier code of the entity that reports IFDat data (:ref:`org`).

UNDER UMBRELLA BY (UNDR_UMBRLL_BY)
    Identifier code of the umbrella fund that the ``OA`` is contained in (if
    applicable) (:ref:`org`).  

TYPE (TYP)
    Investment fund type choosing from ``FND_TYP_ENUM``. 

INVESTMENT POLICY (INVSTMNT_PLCY)
    Investment policy choosing from ``FND_INVSTMNT_PLCY_ENUM``.

SUBTYPE (SBTYP)
    Investment fund subtype choosing from ``FND_SBTYP_ENUM``.

DISTRIBUTION TYPE (DSTRBTN_TYP)
    Dividend distribution type choosing from ``FND_DSTRBTN_TYP_ENUM``.  

INVESTOR TYPE (INVSTR_TYP)
    Investor type choosing from ``FND_INVSTR_TYP_ENUM``.

GREEN TYPE (GRN_TYP)
    Green type choosing from ``FND_GRN_ENUM`` (if applicable).

STRATEGY (STRTGY)
    Investment strategy choosing from ``FND_STRTGY_ENUM``. 
    
GEOGRAPHICAL FOCUS (GGPHCL_FCS)
    Asset main geographical focus choosing from ``FND_GGRPHCL_FCS_ENUM``.

BOND FUND FOCUS (BND_FCS)
    Bond fund sector focus choosing from ``FND_BND_FCS_ENUM``.  It is
    applicable only for investment funds with a bond policy type.

BOND FUND GRADE (BND_GRD)
    Bond fund asset grade choosing from ``FND_BND_GRD_ENUM``. It is applicable
    only for investment funds with a bond policy type.

REAL ESTATE FUND TYPE (RL_ESTT_TYP)
    Type of real estate fund choosing from ``FND_RL_ESTT_TYP_ENUM``.

IS FUND OF FUND (IS_FOF)
    Fund of fund flag.

IS EXCHANGE TRADED FUND (IS_ETF)
    Exchange traded fund flag as defined in ECB/2014/5. 

IS PRIVATE EQUITY FUND (IS_PEF)
    Private equity fund as defined in ECB/2014/5.

DEBT
----

Used to submit information data regarding debt instruments issued by the
``OA``.  The measures of this table can take at most one value during the
life cycle of the debt instrument.

DIMENSIONS
~~~~~~~~~~

ID
    Debt instrument identifier code (:ref:`dbt`).

MEASURES
~~~~~~~~~~

.. _self_debt_birth:

BIRTHDATE (DT_BRTH)
    Issue date.

.. _self_debt_close:

CLOSEDATE (DT_CLS)
    Maturity or redemption date (if applicable).

ORIGINAL MATURITY (ORGNL_MTRTY)
    Original maturity or redemption date (if applicable).

ISIN ID (ISIN_ID)
    Debt identifier based on the ISIN ISO-6166 standard.

INTERNAL ID (INTRNL_ID)
    Internal identifier formatted as ``{UID}_{CODE}`` where ``CODE`` is a
    placeholder for the code that the ``RA`` has assigned to the debt
    instrument.

.. _sidbtcurrency:

CURRENCY (CRRNCY)
    Currency of transaction choosing from ``GEN_CNTRY_ENUM``.

ISSUE PRICE (ISS_PRC)
    Issue price given as a percentage of its nominal price.

REDEMPTION PRICE (RDMPTN_PRC)
    Redemption price given as a percentage of its nominal price.

MARKET (MRKT)
    Trading market choosing from ``GEN_MRKT_ENUM`` based on the ISO-10383 standard.

ACCRUAL STARTDATE (ACCRL_STRTDT)
    Accrual start date.  In case of a debt instrument without coupons the value of 
    self_debt_birth_ is provided.

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
    
COUPON RATE MULTIPLIER (CPN_MLTPLR)
    Coupon rate multiplier.

COUPON RATE CAP (CPN_CP)
    Maximum coupon rate.

COUPON RATE FLOOR (CPN_FLR)
    Minimum coupon rate.

FIRST COUPON DATE (FRST_CPN_DT)
    Date of first coupon payment.

LAST COUPON DATE (LST_CPN_DT)
    Date of last coupon payment.

UNDERLYING INSTRUMENT (UNDRLYNG)
    Underlying debt instrument that the coupon payment depends on (:ref:`dbt`).

MINIMUM LEVEL OF INVESTMENT (MNMM_INVSTMNT)
    Minimum level of investment given in the currency of the debt instrument.

IS PRIVATE PLACEMENT (PRVT)
    Private placement flag.

RESTRUCTURED TO (RSTRCTRD_T)
    In case of restructure to a new debt instrument the identifier code of the
    new debt instrument is provided and self_debt_close_ is filled with the
    date of restructure (:ref:`dbt`).

RESTRUCTURED FROM (RSTRCTRD_FRM)
    In case that the debt instrument originated from a loan restructure the
    identifier code of the loan is provided (:ref:`lon`).

DEDUPLICATE OF (DDPLCT_OF)
    In case the ``RA`` of the ``OA`` changes it is used to deduplicate internal
    (:ref:`dbt`) ids assigned by the old ``RA`` with those assigned by the new
    ``OA``.

STATIC_DEBT
-----------

Used to submit information data regarding debt instruments issued by the
``OA``.  The measures of this table can change during the
life cycle of the debt instrument.

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

LATIN NAME (NM_LTN)
    Name using Latin characters.

SHORT NAME (NM_SHRT)
    Short name. 

STATUS (STTS)
    Instrument status choosing from ``DBT_STTS_ENUM``.
    
MATURITY DATE (MTRTY_DT)
    Maturity or redemption date (if applicable).  In some rare circumstances this date can change during the life cycle of the instrument and in this case self_debt_close_ is updated.

ISSUED BY (ISSD_BY)
    Issuer identification code (:ref:`org`).

CFI
    Instrument category based on ISO-10962 standard.




SHARE
-----

Used to submit information data regarding equity/investment fund shares issued
by the ``OA``.  The measures of this table can take at most one value during
the life cycle of the debt instrument.


DIMENSIONS
~~~~~~~~~~

ID
    Identifier code of the share/investment fund unit (:ref:`shr`).

MEASURES
~~~~~~~~

BIRTHDATE (DT_BRTH)
    Issue date, activation date, initialization date.

.. _sishareclose:
    
CLOSEDATE (DT_CLS)
    Close date (if applicable).

ISIN ID (ISIN_ID)
    Instrument identifier based on the ISIN ISO-6166 standard.

INTERNAL ID (INTRNL_ID)
    Internal identifier formatted as ``{UID}_{CODE}`` where ``CODE`` is a
    placeholder for the code that the ``RA`` has assigned to the instrument.

.. _sishrcurrency:

CURRENCY (CRRNCY)
    Currency of transaction choosing from ``GEN_CNTRY_ENUM``.

MARKET (MRKT)
    Trading market choosing from ``GEN_MRKT_ENUM`` based on the ISO-10383 standard.

RESTRUCTURED TO (RESTRUCTURED_TO)
    In case of restructure to a new share/investment fund instrument the identifier code of the
    new instrument is provided and sishareclose_ is filled with the
    date of restructure (:ref:`shr`).

DEDUPLICATE OF (DDPLCT_OF)
    In case the ``RA`` of the ``OA`` changes it is used to deduplicate internal
    (:ref:`shr`) ids assigned by the old ``RA`` with those assigned by the new
    ``OA``.
    

STATIC_SHARE
------------

Used to submit information data regarding equity/investment fund shares issued
by the ``OA``.  The measures of this table can change during the
life cycle of the instrument.

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

LATIN NAME (NM_LTN)
    Name using Latin characters. 

SHORT NAME (NM_SHRT)
    Short name.

ISSUED BY (ISSD_BY)
    Issuer identification code (:ref:`org`).

NOMINAL_PRICE (NMNL_PRC)
    Nominal price.

CFI
    Instrument category based on ISO-10962 standard.

REDEMPTION FREQUENCY (RDMPTN_FRQNCY)
    Redemption frequency choosing from ``SHR_FND_RDMPTN_FRQNCY_ENUM``.

MINIMUM AMOUNT (MNMM_AMNT)
    Minimum investment amount (if applicable).


MANAGEMENT
----------

Used to submit information data regarding the management company in case the ``OA`` has a management company.  The measures of this table can take at most one value
during the life cycle of the management company.

DIMENSIONS
~~~~~~~~~~

ID
    Identifier code of the management company (:ref:`org`).

MEASURES
~~~~~~~~

BIRTHDATE (DT_BRTH)
    Birth date.

CLOSEDATE (DT_CLS)
    Close date (if applicable).

COUNTRY OF BIRTH (CNTRY_BRTH)
    Country of incorporation choosing from ``GEN_CNTRY_ENUM``.

ESCB ID (ESCB_ID)
    Identifier code that is assigned by the ``ESCB`` known also as the ``RIAD code``.

LEI ID (LEI_ID)
    Identifier code based on the ISO-17442 standard.

TAX ID (TAX_ID)
    Tax identifier code of the format ``{CC}{CODE}`` where ``CC`` is a
    placeholder for  ISO 3166-1 alpha-2 country code that has issued the
    tax code and ``CODE`` is a placeholder for the actual tax code without the
    country code in case it starts with it.

NBR ID (NBR_ID)
    Business identifier code of the format ``{CC}{CODE}`` where ``CC`` is a
    placeholder for  ISO 3166-1 alpha-2 country code that has issued the
    code and ``CODE`` is a placeholder for the actual business identifier code
    without the country code in case it starts with it.

SPLIT FROM (SPLT_FRM)
    In case the ``RA`` was created by a corporate split the identifier code of
    the entity that it was split from is provided (:ref:`org`). 

MERGED WITH (MRGD_WTH)
    In case of closure of the ``RA`` via a merger event the identifier code of
    the entity that the ``RA`` merged with is provided.

STATIC_MANAGEMNT
----------------

Used to submit information data regarding the management company in case the ``OA`` has a management company.  The measures of this table can change during the life cycle of the management company.

DIMENSIONS
~~~~~~~~~~

ID
    Identifier code of the ``RA`` (:ref:`org`).

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

LATIN NAME (NM_LTN)
    Official name using Latin characters.

SHORT NAME (NM_SHRT)
    Short name.

STREET (STRT)
    Street address, street number and area.

LATIN STREET (STRT_LTN)
    Street address, street number and area in Latin characters.

CITY (CTY)
    City, village.

LATIN CITY (CTY_LTN)
    City, village in Latin characters.

POSTAL CODE (PSTL_CD)
    Postal code.

POSTAL BOX (PSTL_BX)
    Postal box.

URL
    Web address.

EMAIL
    Email address.

COUNTRY OF RESIDENCE (CNTRY_RSDNC)
    Country of residence choosing from ``GEN_CNTRY_ENUM``. 
    
LEGAL PROCEEDINGS STATUS (LGL_PRCDNG_STTS)
    Status of legal proceedings choosing from ``ORG_LGL_PRCDNG_STTS_ENUM``.

RA
--

Used to submit information data regarding the ``RA`` .  In case the ``RA`` is the same as the management company or is the ``OA`` data on this table should not be reported since they are already reported in either the FUND or the MANAGEMENT tables.  The measures of this table can take at most one value
during the life cycle of the reporting agent.


DIMENSIONS
~~~~~~~~~~

ID
    Identifier code of the ``RA`` (:ref:`org`).

MEASURES
~~~~~~~~

BIRTHDATE (DT_BRTH)
    Birth date.

CLOSEDATE (DT_CLS)
    Close date (if applicable).

COUNTRY OF BIRTH (CNTRY_BRTH)
    Country of incorporation choosing from ``GEN_CNTRY_ENUM``.

ESCB ID (ESCB_ID)
    Identifier code that is assigned by the ``ESCB`` known also as the ``RIAD code``.

LEI ID (LEI_ID)
    Identifier code based on the ISO-17442 standard.

TAX ID (TAX_ID)
    Tax identifier code of the format ``{CC}{CODE}`` where ``CC`` is a
    placeholder for  ISO 3166-1 alpha-2 country code that has issued the
    tax code and ``CODE`` is a placeholder for the actual tax code without the
    country code in case it starts with it.

NBR ID (NBR_ID)
    Business identifier code of the format ``{CC}{CODE}`` where ``CC`` is a
    placeholder for  ISO 3166-1 alpha-2 country code that has issued the
    code and ``CODE`` is a placeholder for the actual business identifier code
    without the country code in case it starts with it.

SPLIT FROM (SPLT_FRM)
    In case the ``RA`` was created by a corporate split the identifier code of
    the entity that it was split from is provided (:ref:`org`). 

MERGED WITH (MRGD_WTH)
    In case of closure of the ``RA`` via a merger event the identifier code of
    the entity that the ``RA`` merged with is provided.

STATIC_RA
---------

Used to submit information data regarding the ``RA``.  In case
the ``RA`` is the same as the management company or is the ``OA`` data on this
table should not be reported since they are already reported in either the FUND
or the MANAGEMENT tables.  The measures of this table can change during the
life cycle of the ``RA``.

DIMENSIONS
~~~~~~~~~~

ID
    Identifier code of the ``RA`` (:ref:`org`).

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

LATIN NAME (NM_LTN)
    Official name using Latin characters.

SHORT NAME (NM_SHRT)
    Short name.

STREET (STRT)
    Street address, street number and area.

LATIN STREET (STRT_LTN)
    Street address, street number and area in Latin characters.

CITY (CTY)
    City, village.

LATIN CITY (CTY_LTN)
    City, village in Latin characters.

POSTAL CODE (PSTL_CD)
    Postal code.

POSTAL BOX (PSTL_BX)
    Postal box.

URL
    Web address.

EMAIL
    Email address.

COUNTRY OF RESIDENCE (CNTRY_RSDNC)
    Country of residence choosing from ``GEN_CNTRY_ENUM``. 
    
LEGAL PROCEEDINGS STATUS (LGL_PRCDNG_STTS)
    Status of legal proceedings choosing from ``ORG_LGL_PRCDNG_STTS_ENUM``.



CONTACT
-------

It is used for the submission of information data regarding the contact persons
that submit data on behalf of the ``RA``.

DIMENSIONS
~~~~~~~~~~

ID
    Contact person identifier code (:ref:`psn`).

MEASURES
~~~~~~~~~~

EMAIL
    Email address

FIRST NAME (FRST)
    First name. 

SALUTATION OF FIRST NAME (FRST_SLTTN)
    Salutation of first name. 

LAST NAME (LST)
    Last name.

SALUTATION OF LAST NAME (LST_SLTTN)
    Last name salutation.

GENDER (GNDR)
    Gender choosing from ``GEN_GNDR_ENUM``.

PHONE (PHN)
    Phone.
    

CONTACT_TO_RA
-------------

Used to provide information data regarding the labor relationship between the
contact person and the ``RA``.

DIMENSIONS
~~~~~~~~~~

LID
    Contact person identifier code (:ref:`psn`).

RID
    ``RA`` identifier code (:ref:`org`).

VALID FROM (VLD_FRM)
    Date from which the measure values are valid.  
    For further details see :doc:`../../../generic`. 

VALID TO (VLD_T)
    Date to which the measure values are valid.  
    For further details see :doc:`../../../generic`. 

MEASURES
~~~~~~~~

ASSOCIATED_WITH (ASSCTD_WTH)
    Association flag

IS EMPLOYEE OF (IS_EMPLY_OF)
    Employee flag.

IS CONTRACTOR OF (IS_CNTRCTR_OF)
    Contractor flag.

WORKS FOR (WRKS_FR)
    Department within the ``RA`` with which the contact person works for. 

RESPONSIBLE FOR IFDAT (RSPNSBL_FR_IFDAT)
    Flag if responsible for disseminating ``IFDAT`` data.
