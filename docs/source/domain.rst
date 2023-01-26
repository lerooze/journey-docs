DATA DOMAINS
============

The data domains that :mod:`Journey` can handle are of two types:

Structured
    Refers to received data that have a structure defined within :mod:`Journey` as described in section :doc:`data model <data_model>`. 

Unstructured
    Refers to received or obtained data that have a structure defined outside of :mod:`Journey` or do not have a defined structure.
    
Structured Data Domains
-----------------------
    
* `DBDat` handles data that are directly related to the :mod:`Journey` database
  tables.  All other domain data whether structured or not are parsed and
  converted into **DBDat** domain data and then stored to the database.  For
  details see section :doc:`domain/dbdat/index`.

* `IFDat` defines a structure that the RAs of Investment Funds use to submit
  Investment Fund domain data.handles data coming from Investment Fund units.
  For details see section :doc:`domain/ifdat/index`.

Unstructured Data Domains
-------------------------
* TODO


.. toctree::
   :maxdepth: 1 

   domain/dbdat/index 
   domain/ifdat/index 
