Validation
==========
All files successfully submitted based on the steps described in :doc:`file submission <submission>` are validated every day at 08:00am, 11:00am and 2:00pm local time and if no critical_errors occur they are loaded into the system database.  For each authorized user that has submitted at least one file on the time intervals formed from the above times a validation report is prepared by the platform for all files that the authorized user has submitted, data of the validation report are loaded into the system validation database and the report is disseminated to the user.

The validation report is formatted as a ``.json`` file and contains the following attributes:

id
    A unique identification of the validation report 

submitter
    Unique identification of the user that submits data on behalf of a RA

submitter_email
    The email of the user that submits data on behalf of a RA (optional)

submitter_unknown
    Whether the user that submits data is not known to the system

data_domain:
    The **Data Domain** that the submitted data is about (optional)

files
    The list of files with the naming convention as described in :doc:`file submission <submission>` that the user submitted and this validation report checks.

critical_errors
    A list of critical errors as described in :doc:`Critical Error <validation/critical>` (optional)

standard_errors
    A list of standard errors as described in :doc:`Critical Error <validation/standard>` (optional)

warnings
    A list of standard errors as described in :doc:`Critical Error <validation/standard>` (optional)
