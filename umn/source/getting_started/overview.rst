:original_name: cts_02_0001.html

.. _cts_02_0001:

Overview
========

Scenarios
---------

You need to enable CTS before using it. A management tracker named **system** is automatically created when CTS is enabled. All traces recorded by CTS are associated with the tracker.

Trace files must be stored in Object Storage Service (OBS) buckets or Log Tank Service (LTS) log streams. Ensure that you have enabled OBS and LTS and have full permissions for the OBS bucket and LTS log stream you are going to use. By default, only the owner of OBS buckets can access the buckets and all objects contained in the buckets, but the owner can grant access permissions to other services and users by configuring access policies.

Associated Services
-------------------

-  OBS: used to store trace files.

   .. note::

      You must select a standard OBS bucket because CTS needs to frequently access the OBS bucket that stores traces.

-  LTS: stores logs.
-  SMN: Sends email or SMS message notifications to users when key operations are performed.

Procedure
---------

#. Log in to the management console.
#. Click |image1| in the upper left corner and choose **Management & Deployment** > **Cloud Trace Service**. The CTS console is displayed.
#. Choose **Tracker List** in the navigation pane on the left.
#. Click **Enable CTS**.
#. In the displayed dialog box, click **Enable**. A tracker is automatically created.

You can view the tracker information on the **Tracker List** page.

The tracker records operations on cloud resources performed by the tenant who creates the tracker. For details about the cloud services supported by CTS, see :ref:`Supported Services and Operations <cts_03_0300>`.

.. |image1| image:: /_static/images/en-us_image_0000002378674021.png
