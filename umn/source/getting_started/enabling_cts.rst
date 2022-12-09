:original_name: en-us_topic_0030598498.html

.. _en-us_topic_0030598498:

Enabling CTS
============

Scenarios
---------

You need to enable CTS before using it. A tracker is automatically created when CTS is enabled. All traces recorded by CTS are associated with the tracker. Currently, only one tracker is available in a project for a tenant.

Trace files must be stored in OBS buckets. Therefore, before enabling CTS, you must enable OBS and have full permissions of the OBS bucket you are going to use. By default, only the owner who has enabled OBS can access OBS buckets and all objects contained, but the owner can grant permissions to other services and users by configuring an access policy.

A tracker created in a multi-project scenario can only track resources under the current project. If tracking cloud resources under another project is required, you need to create a tracker under the project.

This section describes how to enable CTS.

Prerequisites
-------------

You have created an OBS bucket and have the required permissions.

Procedure
---------

#. Log in to the management console.

#. Click |image1| in the upper left corner to select the desired project.

#. Click **Service List** and choose **Management & Deployment** > **Cloud Trace Service**.

#. Click **Tracker** in the left navigation pane.

#. Click **Enable CTS**.

#. Click **Configure** in the **Operation** column to set **OBS Bucket** and **File Prefix**. :ref:`Table 1 <en-us_topic_0030598498__table1478957894650>` lists the parameters.

   .. _en-us_topic_0030598498__table1478957894650:

   .. table:: **Table 1** Parameter description

      +-------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+---------------+
      | Parameter   | Description                                                                                                                                                                                                                                                                                                                                  | Example Value |
      +=============+==============================================================================================================================================================================================================================================================================================================================================+===============+
      | OBS Bucket  | Name of the OBS bucket in which trace files are to be stored.                                                                                                                                                                                                                                                                                | bucket-001    |
      +-------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+---------------+
      | File Prefix | Used for identifying the trace files stored in the OBS bucket. This parameter is optional. The value can contain 0 to 64 characters. Only letters, numbers, hyphens (-), underscores (_), and periods (.) are supported. If a tracker is created, a value will be generated automatically in the same way as you specify the value manually. | None          |
      +-------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+---------------+

#. Click **OK**.

After CTS is enabled, you can view details of the created tracker on the **Tracker** page.

.. |image1| image:: /_static/images/en-us_image_0237950266.png
