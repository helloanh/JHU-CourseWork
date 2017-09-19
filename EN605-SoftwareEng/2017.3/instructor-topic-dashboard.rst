..
  This work is licensed under a Creative Commons 3.0 Unported License.

  http://creativecommons.org/licenses/by/3.0/legalcode

========
Instructor Topic Dashboard 
========

The instructor-topic dashboard serves as a main view after the user has uploaded comments csv file. It has two pannels for the user: 
one pannel to display the *topic sentiment distribution* and another pannel to display the *instructor sentiment distribution*.  The *topic sentiment distribution* maps out names of instructor to the number of comments. Both pannel displays three level of sentiment: postive, negative, and neutral to either the instructor or the topics.  The data is a processed RESTful datapoint for instructors and courses, from the backend layer. Furthermore, it should have additional options to return to the upload view.


Problem Description
===================

The instructor-topic dashboard aims to deliver processed RESTful endpoints from the data-layer of the CADET team in a user-friendly, graphical interface. It also aims to resolve the following: 

- To display the outputs processed by the data-layer team for topics and instructors sentiments into two pannels.
- To navigate back to the upload page.
- To have the ability to switch between two pannels with ease.
- To create a dashboard that allows room for future expansion for additional features.
- To create a dashboard UI that is compatible with current data visualization libraries from the Django framework. 

Requirements
------------

The functional requirements are the processed calculation in the form of a JSON file from data-layer team. The result should be a dashboard with options to switch between two pannels described above. The quality requirement is to create an intuitive, clean user-interface counts as top priority for quality requirements. Futhermore, the dashboard should accomplish the following tasks: 

- The dashboard must follow the branding guidelines of JHU, available `here <http://brand.jhu.edu/>`_.
- The all two pannels will be displayed and skinned using the built-in `django-admin libraries <http://awesome-django.com/#admin-interface/>`_.
- The dashboard interface must allow the user to switch between the topics pannel, called "Overview", and the instructor pannel, called "Instructor."
- The topics pannel of the dashboard must display the **Topic Sentiment Distribution** heading, with a graph of *Topic ID Number* in the x-axis, along with the *Number of Comments* for the y-axis. The *Topic ID Number* displays three sentiments: positive, negative, and neutral.
- The topics pannel called "Overview" of the dashboard also display the cluster of words mapped to that particular topic id number.  
- The instructor pannel of the dashboard must display the instructor sentiment distribution title along with a graph of instructors names and students students comments. On the instructor x-axis, the names of the instructors should have 3 sentiment ratings: positive, negative, and neutral. On the y-axis, it should display the the number of comments.

Use Case 
------------

Primary Actor: The department chair who wants to view topics by comments or comments by instructor. The department chair wishes to have an overhead view of sentiments groupped by instructors and topics.

Precondition: The department chair must have already uploaded a valid file and it has been processed in the backend team. The user has already finished inputing the topic model options for the number of topics, number of words per topics, number of iterations, and edit the stopwords file.

Postcondition: Graphical represenation of the processed data.

1) The actor has the ability to switch between two pannels on the dashboard.
2) If the actor clicks on the topics pannel, the page should load to display topics and comments grouped for particular topic.  The number of topics to display is determined by the user from the upload view page.
3) If the actor clicks on the instructor pannel, the page should load to display students comments directed at the instructor.

Variations: The department chair's primary objective might not be to view instructors and topics, but to have more granular view--such sorting topics or professors by specific semester.  This is out of the scope of the current iteration of this dashboard.

Variation Handling: Disclaimer or user-friendly text state the purpose of the current functionality of the dashboard. 


Proposed Change
===============

The current dashboard heavily relies the from the `PtQ5 <http://pyqt.sourceforge.net/Docs/PyQt5/>`_. for graphical output with **Numpy** and **MatPlot** python libraries. The web dashboard still would take inputs from *numpy* and *matplotlib* but will add an additional PyQt5 widget named `QWebView <https://pythonspot.com/en/pyqt5-browser/>`_. for the web dashboard functionality. 

There are also drastic UI changes-color, typography, pannel layout--in the display of the web view dashboard. Most will go under the templates section with Django existing libraries, but still will integrate with PyQt5 package.

This feature fits into the larger picture because it takes processed results from the data-layer CADET team and displays the result to the user. 

Alternatives
------------

What other options exist to satisfy the requirements? Why is the proposed
approach better than those options?

Although there are alternatives to PtQt5 library, such as `kivy <https://kivy.org/#home>`_., PtQt5 is already set up in preexisting code.  The Kivy is known more for smaller applications and game development, as mentioned by Medina in `this article <https://medium.com/@tryexceptpass/a-python-ate-my-gui-971f2326ce59>`_. 

There are different libraries such as `Djangosuit <http://djangosuit.com/>`_. to provide out-of-the-box front-end templating functionalities, however, it is not as well documented or has extensive libraries as Awesome-Django.  

Creating a customized UI design with different typography and styling guide is another alternative.  However, this is time-consuming and there is no need to reinvent the wheel when JHU already provide the design guidelines.

Testing
=======

Unit Testing: Use the built-in Django built in **unit test** and `testclient <https://docs.djangoproject.com/en/1.11/topics/testing/tools/>`_. package to test POST and GET requests in a mock browser, particularly on testing requests with for RESTful endpoints on a the dashboard templates.

Intergration Testing: `selenium django <https://django-selenium.readthedocs.io/en/latest/#what-is-it/>`_. library for behavior-driven testing, to emulate a user's experience and interaction with the web site.


Documentation
=============

In-line comments will be provided in the source code for future developing team.  Instructions on setting up and downloading relevant UI Django packages, branding assets, and testing tools will be provided in the repository in the docs directory are also for future front-end side of the engineering team, although any user who wishes to test the system on a live server should be able to follow the set-up guidelines. 


Implementation
==============

Work Items
----------

1. Design bareboned wireframes to test use cases.
2. Design prototypes of screens and upload to InvisionApp for demo with front-end and back-end team.
2. Set up Django UI packages.
3. Integrate packages and template with existing python libraries--numpy and MatPlot.
4. Standardized RESTful endpoints/output JSON file with back-end team. This is our input to parse the two graphical panels on the dashboard view.
5. Develop template dashboard view and helper templates for Overview pannel and Instructor pannel.

References
==========

1. Django Documentation, "Testing Tools," Sept 2017. Online: https://docs.djangoproject.com/en/dev/topics/testing/tools/ 
2. Johns Hopkins University Official Branding Guidelines. April 2016. http://brand.jhu.edu/ 
3. Awesome-Django. http://awesome-django.com/#boilerplate
4. Django Rest Panda. https://github.com/wq/django-rest-pandas/ 
5. PtQ5 QWebView Widget https://pythonspot.com/en/pyqt5-browser/

