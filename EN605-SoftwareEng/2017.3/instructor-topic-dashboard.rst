..
  This work is licensed under a Creative Commons 3.0 Unported License.

  http://creativecommons.org/licenses/by/3.0/legalcode

========
Instructor Topic Dashboard 
========

The instructor-topic dashboard serves to deliver two pannels for the user: 
one pannel for comments across number of topics, and another pannel to display students comments on the instructors.  


Problem Description
===================

The instructor-topic dashboard aims to deliver processed RESTful endpoints from the data-layer of the CADET team in a user-friendly, graphical interface. It also aims to resolve the following: 

- To display the outputs process by the data-layer team in meaningful graphs and histograms.
- To navigate back to the upload page.
- To have the ability to switch between two pannels with ease.

Requirements
------------

The functional requirements are the processed calculation in the form of a JSON file from data-layer team. The result should be a dashboard with options to switch between two pannels described above. The quality requirement is to create an intuitive, clean user-interface counts as top priority for quality requirements. Futhermore, the dashboard should accomplish the following tasks: 

- The topics dashboard must indicate to users that they are in the dashboard-topics section.
- The topics dashboard must follow the branding guidelines of JHU, available `<http://brand.jhu.edu/>`here.
- The topics dashboard must display clusters of 5 topics.
- The topics dashboard must display all comments mapped to those 5 topics.
- The topics dashboard must provide the user an obvious, and intuitive way
  to switch to the instructor dashboard view.
- The topics dashboard must provide the user the option to upload another 
  file or a batch of files.
- The topics dashboard  must be presentable on Firefox and Chrome, desktop view.


Use Cases
---------

A *use case*, at a high level, is a story about an observable interaction (a
"thread of usage") between the system and the environment. Each story is
described from the point of view of an actor that interacts with the system
in some way.

Each feature must include at least one use case that answers the following
questions:
* Who is the primary actor and the secondary actor(s)?
* What are the actors' goals?
* What preconditions exist before the story begins and postconditions after the
  story ends?
* What main tasks or functions are performed by the actor(s)?
* What variations in the actors' interactions are possible (e.g., exceptions)?

Use Case A:

Actor: The superuser is the department chair who wants to view topics by comments or comments by instructor.

Precondition: The department chair must have already uploaded a valid file and it has been processed in the backend team. The user has already finished inputing the topic model options for the number of topics, number of words per topics, number of iterations, and edit the stopwords file.

Postcondition: The processed data is delivered.

1) The actor has the ability to switch between two pannels on the dashboard.
2) If the actor clicks on the topics pannel, the page should load to display topics and comments groupped until that particular topic.  The number of topics to display is 
3) If the actor clicks on the instructor pannel, 


Variations: 

Variation Handling: 


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
change. Work items may be supported by different people, but they also provide
a rough timeline for the proposed feature.

References
==========

Please include any relevant references that are related to the problem or the
proposed change. The references should supplement the material already in this
specification -- i.e., the specification must make sense even if the references
are not available.

.. [RST] David Goodger, "reStructuredText Markup Specification," May 2016.
   Online: http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html

.. [QuickRST] Quick reStructuredText. Online:
   http://docutils.sourceforge.net/docs/user/rst/quickref.html
