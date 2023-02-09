Uploading to Database
=====================

The automatic generic steps :mod:`Journey` performs to upload incoming files submitted between the fixed time intervals described in :doc:`validation <validation>` are the following:

* A temporary data-storage place is created to hold the processed incoming data. 

* A parser is chosen based on the data domain. 

* The incoming data are converted to the :mod:`Journey` database structured data.  The structure of the database tables follows the structure of the data domain :doc:`DBDat <domain/dbdat/index>`.  The conversion steps are described in the parser section of each :doc:`data domains <domain>`.A parser is chosen depending on the domain of the incoming data and the data, the source of the data is determined and the incoming data are converted so that they satisfy the :doc:`DBDat <domain/dbdat/index>` **Data Model** and the data are appended in a temporary storage where latest data received take precedence of earlier data received.  The conversion process for each specific **Data Domain** is described in section **Parsing** under the specific **Data Domain** that are described in :doc:`data domains <domain>`.

* A parser is chosen depending on the domain of the incoming data and the data, the source of the data is determined and the incoming data are converted so that they satisfy the :doc:`DBDat <domain/dbdat/index>` **Data Model** and the data are appended in a temporary storage where latest data received take precedence of earlier data received.  The conversion process for each specific **Data Domain** is described in section **Parsing** under the specific **Data Domain** that are described in :doc:`data domains <domain>`.


2. The above incoming data that have been converted to the **DBDat** data model and that are placed in a temporarily storage area are aligned as described in :doc:`alignment <alignment>` and are placed again in the same temporarily storage area.

3. The processed incoming data are then compared to the database data and any new or changed data are loaded into the database.  This process is described in :doc:`database storage <storage>`.

.. toctree::
   :maxdepth: 1 

   alignment 
   storage
