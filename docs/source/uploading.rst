Uploading to Database
=====================

The workflow for uploading files submitted between the time intervals described in :doc:`validation <validation>` is the following:

1. A parser is chosen depending on the domain of the incoming data and the data, the source of the data is determined and the incoming data are converted so that they satisfy the :doc:`DBDat <domain/dbdat/index>` **Data Model** and the data are appended in a temporary storage where latest data received take precedence of earlier data received.  The conversion process for each specific **Data Domain** is described in section **Parsing** under the specific **Data Domain** that are described in :doc:`data domains <domain>`.

2. The above incoming data that have been converted to the **DBDat** data model and that are placed in a temporarily storage area are aligned as described in :doc:`alignment <alignment>` and are placed again in the same temporarily storage area.

3. The processed incoming data are then compared to the database data and any new or changed data are loaded into the database.  This process is described in :doc:`database storage <storage>`.

.. toctree::
   :maxdepth: 1 

   alignment 
   storage
