:original_name: en-us_topic_0059288681.html

.. _en-us_topic_0059288681:

Configuring a Tracker
=====================

Scenarios
---------

You can configure parameters in the **Transfer to OBS** area for a created tracker on the **Configure Tracker** page.

If you configure an OBS bucket for a tracker, CTS automatically attaches transferring policies to the OBS bucket so that trace files can be delivered to the OBS bucket for storage. **File Prefix** can be customized to mark trace files to be transferred. The specified prefix will be automatically added in front of the name of a transferred file, helping you quickly find required files.

.. note::

   You must select a standard OBS bucket because CTS needs to frequently access the OBS bucket which traces are transferred to.

After a tracker is configured, new rules take effect immediately.

This section describes how to configure a tracker.

Prerequisites
-------------

You have enabled CTS.

Procedure
---------

#. Log in to the management console.

#. Click |image1| in the upper left corner to select the desired project.

#. Click **Service List** and choose **Management & Deployment** > **Cloud Trace Service**.

#. Click **Tracker** in the left navigation pane.

#. Click **Configure** in the same row as the target tracker in the **Operation** column.

#. Set related parameters on the **Configure Tracker** page.

   -  **Basic Information**

      -  **Tracker Name**: The default value is **system**.
      -  **Trace Analysis**: Enable this function.
      -  **Trace Analysis Path**.

         .. note::

            After trace analysis is enabled, traces will be synchronized to LTS.

   -  **Transfer to OBS**

      .. note::

         CTS allows you to store traces of the last seven days. You can also configure an OBS bucket to deliver traces to it for long-term storage.

      -  **OBS Bucket**: Select an existing OBS bucket.
      -  **File Prefix**: The prefix is used to mark a transferred trace file. The specified prefix will be automatically added in front of the name of a transferred file, helping you quickly find required files.

#. Click **OK**.

   After the tracker is configured, you can view its details on the **Tracker** page.

.. |image1| image:: /_static/images/en-us_image_0237950266.png
