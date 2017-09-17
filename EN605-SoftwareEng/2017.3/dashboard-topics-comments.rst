..
  This work is licensed under a Creative Commons 3.0 Unported License.

  http://creativecommons.org/licenses/by/3.0/legalcode

===========
Dashboard - Topics Across Comments
===========

The CADET application is a web-based application which allows a user, 
in this case, the super user department chair, to upload a single or 
multiple files in Excel or or CSV format. The files include students 
comments on a particular course and instructor. This program requires 
an initial upload page with file(s) the user has already uploaded, and
computation from the back-end to use Python npl libraries to process text
into five topics.

Problem Description
===================

The CADET program requires an web application interface to allow better
accesibility for future users.  At its current form, the user would have to 
pull the raw code and compile the program with python in the terminal. 
The current view process comment files and display the results in two view:
the topic dashboard and instructor dashboard. The color scheme and typography 
are bare, monochromatic grey, and not user-friendly nor interactive. 

There needs to be a mechanism to inform the user of how to navigate between 
the two dashboards.  The needs to be a mechanism to give the user more details
on how the file is processed in the backend.

Requirements
------------

- The topics dashboard must indicate to users that they are in the dashboard-topics
section.
- The topics dashboard must have a clean and intuitive interface.
- The topics dashboard must follow the branding guidelines of JHU, 
  available `<http://brand.jhu.edu/>`_here.
- The topics dashboard must display clusters of 5 topics.
- The topics dashboard must display all comments mapped to those 5 topics.
- The topics dashboard must provide the user an obvious, and intuitive way
  to switch to the instructor dashboard view.
- The topics dashboard must provide the user the option to upload another 
  file or a batch of files.
- The topics dashboard  must be presentable on Firefox and Chrome, desktop view.

Use Cases
---------

Use Case A:

Actor: The superuser is the department chair who can upload a single or multiple
file of student comments.

Precondition: The department chair must have at least one valid file for the
program to process.

Postcondition: No post conditions exist.

1) The actor will upload file(s) in the upload panel view from their
   selected browser by going to a provided URL/test server.
2) a) The actor will be prompted to select the format of upload, and will
      select "Upload Text" from the available onscreen options.
   b) At that time, the Main Screen will route the user to the Upload Text
      Feature.

Variations: The actor might input the wrong URL.

Variation Handling: 


Use Case B:

Actor: 

Precondition: 

Postcondition: No post conditions exist.

Variations: 

Variation Handling: 

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

The proposed feature will be implemented over the course of the following
phases:

- Design Phase - Design sprints with wireframe, then demo in InvisionApp.
- Development Phase - The feature will be created.
- Feature Testing Phase - The functionality specific to the feature will be
  tested.
- UI Implementation Phase - The feature will be integrated into the UI project.
- UI Implementation Testing Phase - The UI project will be tested as a whole.
- Project Integration - The UI section will be integrated into the overall
  project.
- Project Testing - The overall project will be functionally tested.

References
==========

None
