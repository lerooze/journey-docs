Data Categories
===============

+-------------------------------------------+-------------------------+------------------------+-----------------------+
| Data Category                             | Data Model              | Excel Template         | JSON Schema           |
+===========================================+=========================+========================+=======================+
| :doc:`SELF_INFO <categories/self_info>`   | `SELF_INFO_DATAMODEL`_  | `SELF_INFO_TEMPLATE`_  | `SELF_INFO_SCHEMA`_   |
+-------------------------------------------+-------------------------+------------------------+-----------------------+
| :doc:`SELF_KEY <categories/self_key>`     | `SELF_KEY_DATAMODEL`_   | `SELF_KEY_TEMPLATE`_   | `SELF_INFO_TEMPLATE`_ |
+-------------------------------------------+-------------------------+------------------------+-----------------------+
| :doc:`OTHER_INFO <categories/other_info>` | `OTHER_INFO_DATAMODEL`_ | `OTHER_INFO_TEMPLATE`_ | `OTHER_INFO_SCHEMA`_  |
+-------------------------------------------+-------------------------+------------------------+-----------------------+
| :doc:`OTHER_KEY <categories/other_key>`   | `OTHER_KEY_DATAMODEL`_  | `OTHER_KEY_TEMPLATE`_  | `OTHER_KEY_SCHEMA`_   |
+-------------------------------------------+-------------------------+------------------------+-----------------------+
| :doc:`BSI <categories/bsi>`               | `BSI_DATAMODEL`_        | `BSI_TEMPLATE`_        | `BSI_SCHEMA`_         |
+-------------------------------------------+-------------------------+------------------------+-----------------------+
|  :doc:`INCOME <categories/income>`        | `INCOME_DATAMODEL`_     | `INCOME_TEMPLATE`_     | `INCOME_SCHEMA`_      |
+-------------------------------------------+-------------------------+------------------------+-----------------------+

For each of the six data categories of ``IFDat`` the table above gives the following:

Data Category
    Name and link to the section that describes the following for each table of the data category:

    * Table dimensions

    * Table measures

    * The attributes for each measure in case of deviations with what is discussed in  
      :doc:`../../generic` regarding attributes.
    
    In the title of each dimension, measure and attribute the name is provided
    and in parenthesis the code name if it is different from the name.

Data Model
    Link to download the corresponding ``Data Model``.
    
    
Excel Template
    Link to download the excel template for data submission in in excel format.

JSON Schema
    Link to download the corresponding ``json`` schema that data submitted
    using ``json`` format must follow. 

.. _SELF_INFO_DATAMODEL: https://github.com/lerooze/journey-docs/blob/main/domain_files/ifdat/model/SELF_INFO_DATAMODEL.xlsx

.. _SELF_INFO_TEMPLATE: https://github.com/lerooze/journey-docs/blob/main/domain_files/ifdat/template/SELF_INFO_TEMPLATE.xlsx

.. _SELF_INFO_SCHEMA: https://github.com/lerooze/journey-docs/blob/main/domain_files/ifdat/schema/SELF_INFO_SCHEMA.json

.. _SELF_KEY_DATAMODEL: https://github.com/lerooze/journey-docs/blob/main/domain_files/ifdat/model/SELF_KEY_DATAMODEL.xlsx

.. _SELF_KEY_TEMPLATE: https://github.com/lerooze/journey-docs/blob/main/domain_files/ifdat/template/SELF_KEY_TEMPLATE.xlsx

.. _SELF_KEY_SCHEMA: https://github.com/lerooze/journey-docs/blob/main/domain_files/ifdat/schema/SELF_KEY_SCHEMA.json

.. _OTHER_INFO_DATAMODEL: https://github.com/lerooze/journey-docs/blob/main/domain_files/ifdat/model/OTHER_INFO_DATAMODEL.xlsx

.. _OTHER_INFO_TEMPLATE: https://github.com/lerooze/journey-docs/blob/main/domain_files/ifdat/template/OTHER_INFO_TEMPLATE.xlsx

.. _OTHER_INFO_SCHEMA: https://github.com/lerooze/journey-docs/blob/main/domain_files/ifdat/schema/OTHER_INFO_SCHEMA.json

.. _OTHER_KEY_DATAMODEL: https://github.com/lerooze/journey-docs/blob/main/domain_files/ifdat/model/OTHER_KEY_DATAMODEL.xlsx

.. _OTHER_KEY_TEMPLATE: https://github.com/lerooze/journey-docs/blob/main/domain_files/ifdat/template/OTHER_KEY_TEMPLATE.xlsx

.. _OTHER_KEY_SCHEMA: https://github.com/lerooze/journey-docs/blob/main/domain_files/ifdat/schema/OTHER_KEY_SCHEMA.json

.. _BSI_DATAMODEL: https://github.com/lerooze/journey-docs/blob/main/domain_files/ifdat/model/BSI_DATAMODEL.xlsx

.. _BSI_TEMPLATE: https://github.com/lerooze/journey-docs/blob/main/domain_files/ifdat/template/BSI_TEMPLATE.xlsx

.. _BSI_SCHEMA: https://github.com/lerooze/journey-docs/blob/main/domain_files/ifdat/schema/BSI_SCHEMA.json

.. _INCOME_DATAMODEL: https://github.com/lerooze/journey-docs/blob/main/domain_files/ifdat/model/INCOME_DATAMODEL.xlsx

.. _INCOME_TEMPLATE: https://github.com/lerooze/journey-docs/blob/main/domain_files/ifdat/template/INCOME_TEMPLATE.xlsx

.. _INCOME_SCHEMA: https://github.com/lerooze/journey-docs/blob/main/domain_files/ifdat/schema/INCOME_SCHEMA.json

.. toctree::
   :hidden:

   categories/self_info
   categories/self_key
   categories/other_info
   categories/other_key
   categories/bsi
   categories/income
