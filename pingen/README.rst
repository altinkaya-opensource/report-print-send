======================
pingen.com integration
======================

.. 
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
   !! This file is generated by oca-gen-addon-readme !!
   !! changes will be overwritten.                   !!
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
   !! source digest: sha256:f5ab7a7ea6b3293a9889594432660443e1b976f3319c7f64a08851363358a360
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

.. |badge1| image:: https://img.shields.io/badge/maturity-Beta-yellow.png
    :target: https://odoo-community.org/page/development-status
    :alt: Beta
.. |badge2| image:: https://img.shields.io/badge/licence-AGPL--3-blue.png
    :target: http://www.gnu.org/licenses/agpl-3.0-standalone.html
    :alt: License: AGPL-3
.. |badge3| image:: https://img.shields.io/badge/github-OCA%2Freport--print--send-lightgray.png?logo=github
    :target: https://github.com/OCA/report-print-send/tree/16.0/pingen
    :alt: OCA/report-print-send
.. |badge4| image:: https://img.shields.io/badge/weblate-Translate%20me-F47D42.png
    :target: https://translation.odoo-community.org/projects/report-print-send-16-0/report-print-send-16-0-pingen
    :alt: Translate me on Weblate
.. |badge5| image:: https://img.shields.io/badge/runboat-Try%20me-875A7B.png
    :target: https://runboat.odoo-community.org/builds?repo=OCA/report-print-send&target_branch=16.0
    :alt: Try me on Runboat

|badge1| |badge2| |badge3| |badge4| |badge5|

Pingen.com is a paid online service.
It sends uploaded documents by letter post.

One can decide, per document / attachment, if it should be pushed
to pingen.com. The documents are pushed asynchronously.

The informations of the documents from pingen.com are updated through webhook calls.

**Table of contents**

.. contents::
   :local:

Configuration
=============

The authentication token, client ID, organization ID and webhook secret is configured
on the company's view. You can also tick a checkbox if the staging environment
(https://stage-api.pingen.com) should be used.

Webhooks should be configured on pingen account. Organization ID and webhook secret must match.

Usage
=====

On the attachment view, a new pingen.com section has been added.
You can tick a box to push the document to pingen.com.

There is 3 additional options:

 * Send: the document will not be only uploaded, but will be also be sent
 * Speed: priority or economy
 * Type of print: color or black and white

Once the configuration is done and the attachment saved, a Pingen Document
is created. You can directly access to the latter on the Link on the right on
the attachment view.

You can find them in `Pingen Documents` App or in the more convenient `Documents` menu if you have installed the
`document` module.

Errors
======

Sometimes, pingen.com will refuse to send a document because it does not meet
its requirements. In such case, the document's state becomes "Pingen Error"
and you will need to manually handle the case, either from the pingen.com
backend, or by changing the document on Odoo and resolving the error on the
Pingen Document.

When a connection error occurs, the action will be retried on the next
scheduler run.


Dependencies
============

 * Require the Python library `requests_oauthlib <https://github.com/requests/requests-oauthlib>`_
 * The address must be in a format accepted by pingen.com: the last line
   is the country in English or German.

Bug Tracker
===========

Bugs are tracked on `GitHub Issues <https://github.com/OCA/report-print-send/issues>`_.
In case of trouble, please check there if your issue has already been reported.
If you spotted it first, help us to smash it by providing a detailed and welcomed
`feedback <https://github.com/OCA/report-print-send/issues/new?body=module:%20pingen%0Aversion:%2016.0%0A%0A**Steps%20to%20reproduce**%0A-%20...%0A%0A**Current%20behavior**%0A%0A**Expected%20behavior**>`_.

Do not contact contributors directly about support or help with technical issues.

Credits
=======

Authors
~~~~~~~

* Camptocamp

Contributors
~~~~~~~~~~~~

* Guewen Baconnier <guewen.baconnier@camptocamp.com>
* Anar Baghirli <a.baghirli@mobilunity.com>
* Akim Juillerat <akim.juillerat@camptocamp.com>
* Anna Janiszewska <anna.janiszewska@camptocamp.com>

Maintainers
~~~~~~~~~~~

This module is maintained by the OCA.

.. image:: https://odoo-community.org/logo.png
   :alt: Odoo Community Association
   :target: https://odoo-community.org

OCA, or the Odoo Community Association, is a nonprofit organization whose
mission is to support the collaborative development of Odoo features and
promote its widespread use.

.. |maintainer-ajaniszewska-dev| image:: https://github.com/ajaniszewska-dev.png?size=40px
    :target: https://github.com/ajaniszewska-dev
    :alt: ajaniszewska-dev
.. |maintainer-grindtildeath| image:: https://github.com/grindtildeath.png?size=40px
    :target: https://github.com/grindtildeath
    :alt: grindtildeath

Current `maintainers <https://odoo-community.org/page/maintainer-role>`__:

|maintainer-ajaniszewska-dev| |maintainer-grindtildeath| 

This module is part of the `OCA/report-print-send <https://github.com/OCA/report-print-send/tree/16.0/pingen>`_ project on GitHub.

You are welcome to contribute. To learn how please visit https://odoo-community.org/page/Contribute.
