JOURNEY-DOCS
============

:mod:`Journey` is a platform that serves three main purposes:

* Accept data from various domains and sources, validate and store them in main database tables

* Compile stored data based on various standards and feed them to the respective databases.

* Serve as a client interface to disseminate data based on structured requests or structured reports 

Section :doc:`data domains <domain>` describes all domains of data that :mod:`Journey` handles.  As explained within data domains are categorized into structured and unstructured.

Section :doc:`data submission <submission>` describes the main methods of submitting structured domain data.

Section :doc:`data validation <validation>` describes the process of validating incoming data.

Section :doc:`identifiers <identifiers>` describes how to identify each uniquely identifiable kind of unit in :mod:`Journey`. 

Section :doc:`sid` provides the names and the identification codes of the reporting agents.

Section :doc:`whatsnew` provides details of what changes in each released version of :mod:`Journey`.

Section :doc:`dev` provides details of how to contribute to :mod:`Journey`.


.. toctree::
   :maxdepth: 1 

   domain
   submission
   validation
   identifiers
   sid
   whatsnew
   dev

.. toctree::
   :hidden:

   generic
   data_model
   structure
   glossary
   license
