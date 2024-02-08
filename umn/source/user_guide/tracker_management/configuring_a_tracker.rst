:original_name: cts_03_0002.html

.. _cts_03_0002:

Configuring a Tracker
=====================

Scenario
--------

You can configure the file prefix of trackers on the CTS console no matter whether the trackers are enabled or not. For enabled trackers, you can also configure OBS buckets for trace transfer and LTS dumps.

-  You can select an existing OBS bucket for trace transfer. CTS will automatically attach a required policy to the OBS bucket.
-  If you modify the trace file prefix of a tracker, the OBS bucket policy will not be affected.

.. note::

   There are three storage classes of OBS buckets, Standard, Infrequent Access, and Archive. You must use Standard OBS buckets for trace transfer because CTS needs to frequently access the OBS buckets.

The configuration will take effect immediately after it is complete.

Prerequisites
-------------

You have enabled CTS.

Procedure
---------

#. Log in to the management console.

#. Click |image1| in the upper left corner and choose **Management & Deployment** > **Cloud Trace Service**. The CTS console is displayed.

#. Choose **Tracker List** in the navigation pane on the left.

#. On the right of the tracker information, click **Configure**.

#. Configure a transfer.

   .. table:: **Table 1** Parameters for configuring a transfer

      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                                                                                                                                                                                           |
      +===================================+=======================================================================================================================================================================================================================================================================================================+
      | Transfer to OBS                   | If you select **Yes**, select an existing OBS bucket and set **File Prefix**.                                                                                                                                                                                                                         |
      |                                   |                                                                                                                                                                                                                                                                                                       |
      |                                   | When **Transfer to OBS** is disabled, no operation is required.                                                                                                                                                                                                                                       |
      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | OBS Bucket                        | **New**: If this function is enabled, an OBS bucket will be created automatically with the name you enter.                                                                                                                                                                                            |
      |                                   |                                                                                                                                                                                                                                                                                                       |
      |                                   | Select **Existing**: Select an existing OBS bucket.                                                                                                                                                                                                                                                   |
      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Select Bucket                     | When you select **New**, enter an OBS bucket name. The OBS bucket name cannot be empty. It can contain 3 to 63 characters, including only lowercase letters, digits, hyphens (-), and periods (.). It cannot contain two consecutive periods (..). For example, **my..bucket** is not allowed.        |
      |                                   |                                                                                                                                                                                                                                                                                                       |
      |                                   | When you select **Existing**, select an existing OBS bucket.                                                                                                                                                                                                                                          |
      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Retention Period                  | The duration for storing traces in the OBS bucket. This configuration will apply to the selected bucket and all files in it. Different compliance standards require different trace retention periods. You are advised to set the retention period to at least 180 days.                              |
      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | File Prefix                       | A prefix is used to mark a transferred trace file. Your specified prefix will be automatically added to the beginning of the name of a transferred file, helping you quickly filter files. Enter 0 to 64 characters. Only letters, digits, hyphens (-), underscores (_), and periods (.) are allowed. |
      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Transfer to LTS                   | When **Transfer to LTS** is enabled, traces are transferred to the log stream.                                                                                                                                                                                                                        |
      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Log group name                    | When **Transfer to LTS** is enabled, the default log group name is **CTS**. When **Transfer to LTS** is disabled, no operation is required.                                                                                                                                                           |
      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

#. Click **OK** to complete the configuration.

   You can then view the tracker details on the **Tracker List** page.

   .. note::

      Traces recorded by CTS are delivered periodically to the OBS bucket for storage. If you configure an OBS bucket for a tracker, traces generated during the current cycle (usually several minutes) will be delivered to the configured OBS bucket. For example, if the current cycle is from 12:00:00 to 12:05:00 and you configure an OBS bucket for a tracker at 12:02:00, traces received from 12:00:00 to 12:02:00 will also be delivered to the configured OBS bucket for storage at 12:05:00.

.. |image1| image:: /_static/images/en-us_image_0000001187949118.png
