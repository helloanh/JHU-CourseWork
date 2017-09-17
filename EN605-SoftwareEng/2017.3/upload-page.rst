..
  This work is licensed under a Creative Commons 3.0 Unported License.

  http://creativecommons.org/licenses/by/3.0/legalcode

========
Upload Page
========

The upload page for CADET application will allow users to ...


Problem Description
===================


Requirements
------------

1. The user shall be allowed to select and upload a file.

2. The file contents shall be sent via a REST API to the data access layer.

3. The user interface shall transition to the loading page.

Use Cases
---------

File upload
~~~~~~~~~~~

:Primary Actor:
The user - department chairs

:Goals:
Upload a file to check sentiment ratings of students on instructors

:Preconditions:
:Tasks:
The user must select and upload a file, or mulitple files in batch.

:Postconditions:
The application uploads the file then transitions to the results page

:Exceptions:
if the data access layer is unavailable and the rest api call fails, an error
message will be displayed to the user

Proposed Change
===============

Alternatives
------------


Testing
=======


Documentation
=============


Implementation
==============

Work Items
----------

