Overlapping Time Interval Correction, Alignment and Merging
===========================================================

Base Tables
-----------
Base tables are any tables in which the dimensions do not contain any date
dimensions.  They are the tables that generate :doc:`units <identifiers>`.  

Example
~~~~~~~
Suppose a user has submitted two files to be validated together that contain the following data from ORG tables:


Data from first ORG table:

+-------+------------+
| ID    | DT_BRTH    |
+=======+============+
| GRFOO | 1999-01-01 |
+-------+------------+
| GRFAZ | 2010-01-25 |
+-------+------------+

Data from second ORG table which is submitted after the first ORG table:

+-------+------------+------------+
| ID    | DT_BRTH    | CNTRY_BRTH |
+=======+============+============+
| GRFAZ | 2011-01-01 | GR         |
+-------+------------+------------+
| GRFEN | 2022-06-25 |            |
+-------+------------+------------+

Merging the two ORG tables gives:

+-------+------------+------------+
| ID    | DT_BRTH    | CNTRY_BRTH |
+=======+============+============+
| GRFOO | 1999-01-01 |            |
+-------+------------+------------+
| GRFAZ | 2011-01-01 | GR         |
+-------+------------+------------+
| GRFEN | 2022-06-25 |            |
+-------+------------+------------+


Static Tables
-------------
Static tables are any tables in which the dimensions of the table include **VLD_FRM** and **VLD_T**.  

Example
~~~~~~~
Suppose a user has submitted two files to be validated together that contain the following data from STATIC_ORG tables:


Data from first STATIC_ORG table:

+-------+------------+------------+--------+
| ID    | VALID FROM | VALID TO   | SECTOR |
+=======+============+============+========+
| GRFOO | 2000-01-01 | 2010-11-24 | S125   |
+-------+------------+------------+--------+
| GRFOO | 2009-01-25 |            | S126   |
+-------+------------+------------+--------+

And after overlapping time interval correction the first STATIC_ORG table becomes: 

+-------+------------+------------+--------+
| ID    | VALID FROM | VALID TO   | SECTOR |
+=======+============+============+========+
| GRFOO | 2000-01-01 | 2009-01-25 | S125   |
+-------+------------+------------+--------+
| GRFOO | 2009-01-25 |            | S126   |
+-------+------------+------------+--------+

Data from second STATIC_ORG table which is submitted after the first STATIC_ORG 
table:

+-------+------------+------------+--------------+---------+
| ID    | VLD_FRM    | VLD_T      | INSTTNL_SCTR | IS_LSTD |
+=======+============+============+==============+=========+
| GRFOO | 2007-03-30 | 2015-05-05 |    S128      |         |
+-------+------------+------------+--------------+---------+
| GRFOO | 2014-01-15 |            |              |  True   |
+-------+------------+------------+--------------+---------+

And after overlapping time interval correction the first STATIC_ORG table becomes: 

+-------+------------+------------+--------------+---------+
| ID    | VLD_FRM    | VLD_T      | INSTTNL_SCTR | IS_LSTD |
+=======+============+============+==============+=========+
| GRFOO | 2007-03-30 | 2014-01-15 |    S128      |         |
+-------+------------+------------+--------------+---------+
| GRFOO | 2014-01-15 | 2015-05-05 |    S128      |  True   |
+-------+------------+------------+--------------+---------+
| GRFOO | 2015-05-05 |            |              |  True   |
+-------+------------+------------+--------------+---------+

Aligning the two STATIC_ORG tables gives:

+-------+------------+------------+--------------+---------+
| ID    | VLD_FRM    | VLD_T      | INSTTNL_SCTR | IS_LSTD |
+=======+============+============+==============+=========+
| GRFOO | 2000-01-01 | 2007-03-30 |    S125      |         |
+-------+------------+------------+--------------+---------+
| GRFOO | 2007-03-30 | 2014-01-15 |    S128      |         |
+-------+------------+------------+--------------+---------+
| GRFOO | 2014-01-15 | 2015-05-05 |    S128      |  True   |
+-------+------------+------------+--------------+---------+
| GRFOO | 2015-05-05 |            |    S126      |  True   |
+-------+------------+------------+--------------+---------+
