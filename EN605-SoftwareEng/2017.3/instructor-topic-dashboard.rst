..
  This work is licensed under a Creative Commons 3.0 Unported License.

  http://creativecommons.org/licenses/by/3.0/legalcode

========
Instructor Topic Dashboard 
========

The instructor-topic dashboard serves to deliver two pannels for the user: 
one pannel for comments across number of topics and another pannel to display students comments per instructor.  The data is a processed RESTful datapoint for instructors and courses, from the backend layer.


Problem Description
===================

The instructor-topic dashboard aims to deliver processed RESTful endpoints from the data-layer of the CADET team in a user-friendly, graphical interface. It also aims to resolve the following: 

- To display the outputs process by the data-layer team in meaningful graphs and histograms.
- To navigate back to the upload page.
- To have the ability to switch between two pannels with ease.
- To create a dashboard that allows room for future expansion for additional features.
- To create a dashboard UI that is compatible with current data visualization libraries from the Django framework. 

Requirements
------------

The functional requirements are the processed calculation in the form of a JSON file from data-layer team. The result should be a dashboard with options to switch between two pannels described above. The quality requirement is to create an intuitive, clean user-interface counts as top priority for quality requirements. Futhermore, the dashboard should accomplish the following tasks: 

- The topics pannel of the dashboard must indicate to users that they are in the dashboard-topics section.
- The topics pannel of the dashboard must provide the user an obvious, and intuitive way
  to switch to the instructor dashboard view.
- The topics pannel of the dashboard must follow the branding guidelines of JHU, available `here <http://brand.jhu.edu/>`_.
- The topics pannel of the dashboard must display clusters of the number of topics the user has selected.
- The topics pannel of the dashboard must display all comments mapped to those topics.
- The instructor pannel of the dashboard must display names of instructor and students comments related to that instructor, with sentiment rating.

Use Case A:
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

This section describes how the requirements will be satisfied by the software
system. Considerable detail should be provided -- enough that someone else
could implement this feature.

If this feature is part of a larger effort, include at least one paragraph
describing how this feature fits into the larger system. Be sure to include
the scope of this feature so it is clear where this effort ends. Very large
features may be broken up into multiple pieces and implemented separately,
in which case it is necessary to clearly delineate where each piece ends.

Alternatives
------------

What other options exist to satisfy the requirements? Why is the proposed
approach better than those options?

Testing
=======

Unit Testing: Use the built-in Django 'unittest tool <https://docs.python.org/3/library/unittest.html#module-unittest>'_. and 'testclient tool <https://docs.djangoproject.com/en/dev/topics/testing/tools/>'_. to test POST and GET requests in a mock browser, particularly on testing requests with for RESTful endpoints on a the dashboard templates.

Intergration Testing:

What is the test plan? That is, how will this change be tested? Are there
specific test cases to guard against expected faults?

Provide a detailed rationale if some portions of the proposed change are not
testable or no specific test cases will accompany the implementation.

Documentation
=============

What documentation should accompany this change -- e.g., in-line comments in
the source code or user manuals? Be sure to identify the target audience for
various forms of documentation if it isn't obvious from the context (e.g.,
source code comments are typically intended for developers).

Implementation
==============

Work Items
----------

If this feature will be implemented in phases (and most features should be!),
enumerate the individual pieces that will collectively implement the proposed
change. Work items may be supported by different people, but they also provide a rough timeline for the proposed feature.

References
==========

Please include any relevant references that are related to the problem or the
proposed change. The references should supplement the material already in this specification -- i.e., the specification must make sense even if the references are not available.

.. [Django Testing] Django Documentation, "Testing Tools," Sept 2017. 
	Online: https://docs.djangoproject.com/en/dev/topics/testing/tools/ 

.. [RST] David Goodger, "reStructuredText Markup Specification," May 2016.
   Online: http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html

.. [QuickRST] Quick reStructuredText. Online:
   http://docutils.sourceforge.net/docs/user/rst/quickref.html
