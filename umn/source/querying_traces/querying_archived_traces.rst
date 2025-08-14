:original_name: cts_02_0006.html

.. _cts_02_0006:

Querying Archived Traces
========================

Scenarios
---------

CTS periodically sends trace files to OBS buckets. A trace file is a collection of traces. CTS generates trace files based on services and transfer cycle, and adjusts the number of traces contained in each trace file as needed. CTS can also save audit logs to LTS log streams.

This section describes how to view historical operation records in trace files downloaded from OBS buckets and in LTS log streams.

Prerequisites
-------------

You have configured a tracker in CTS and enabled **Transfer to OBS** or **Transfer to LTS**. For details, see :ref:`Configuring a Tracker <en-us_topic_0071185672>`.

Querying Traces Transferred to OBS
----------------------------------

If you enable **Transfer to OBS** when configuring the tracker, traces will be periodically transferred to a specified OBS bucket as trace files for long-term storage.

#. Log in to the management console.

#. Click |image1| in the upper left corner and choose **Management & Deployment** > **Cloud Trace Service**. The CTS console is displayed.

#. Choose **Tracker List** in the navigation pane on the left.

#. Click a bucket in the **OBS Bucket** column.


   .. figure:: /_static/images/en-us_image_0000002344716048.png
      :alt: **Figure 1** Selecting an OBS bucket

      **Figure 1** Selecting an OBS bucket

#. In the OBS bucket, locate the file storage path to view the desired trace, and click **Download** on the right to download the file to the default download path of the browser. If you need to save it to a custom path, click **More** > **Download As** on the right.

   -  The trace file storage path is as follows:

      **OBS bucket name > CloudTraces > Region > Year > Month > Day > Tracker name > Service directory**

      An example is **User-defined name > CloudTraces > region > 2016 > 5 > 19 > system > ECS**.

   -  The trace file naming format is as follows:

      *Trace file prefix*\ **\_CloudTrace\_**\ *Region/Region-project*\ **\_**\ *Time when the trace file was uploaded to OBS: Year-Month-Day*\ **T**\ *Hour-Minute-Second*\ **Z\_**\ *Random characters*\ **.json.gz**

      An example is **File Prefix**\ **\_CloudTrace_region-project_2016-05-30T16-20-56Z_21d36ced8c8af71e.json.gz**.

   .. note::

      The OBS bucket name and trace file prefix are user-defined, and other parameters are automatically generated.

      Downloading the file will incur request fees and traffic fees.

   For details about key fields in the CTS trace structure, see :ref:`Trace Structure <cts_03_0010>` and :ref:`Example Traces <cts_03_0011>`.


   .. figure:: /_static/images/en-us_image_0000002378673969.png
      :alt: **Figure 2** Viewing trace file content

      **Figure 2** Viewing trace file content

#. Decompress the downloaded package to obtain a JSON file with the same name as the package. Open the JSON file using a text file editor to view traces.


   .. figure:: /_static/images/en-us_image_0000002344556232.png
      :alt: **Figure 3** JSON file

      **Figure 3** JSON file

Querying Traces Transferred to LTS
----------------------------------

If you enable **Transfer to LTS** when configuring a tracker, traces will be transferred to the **CTS/{Tracker Name}** log stream for long-term storage. *{Tracker Name}* indicates the name of the current tracker. For example, the log stream path of the management tracker is **CTS/system-trace**.

#. Log in to the management console.

#. Click |image2| in the upper left corner and choose **Management & Deployment** > **Cloud Trace Service**. The CTS console is displayed.

#. Choose **Tracker List** in the navigation pane on the left.

#. Click an LTS log stream in the **Storage** column.


   .. figure:: /_static/images/en-us_image_0000002344556220.png
      :alt: **Figure 4** Selecting an OBS log stream

      **Figure 4** Selecting an OBS log stream

#. On the **Log Stream** tab page in the **CTS** log group page, select the *{Tracker name}* log stream to view trace logs.

   For details about key fields in the CTS trace structure, see :ref:`Trace Structure <cts_03_0010>` and :ref:`Example Traces <cts_03_0011>`.

#. Click |image3| to download the log file to your local PC.

   .. note::

      Each time you can download up to 5,000 log events. If the number of selected log events exceeds 5000, you cannot download them directly from LTS. Transfer them to OBS and then download them from OBS.

.. |image1| image:: /_static/images/en-us_image_0000002344556228.png
.. |image2| image:: /_static/images/en-us_image_0000002344556236.png
.. |image3| image:: /_static/images/en-us_image_0000002378673981.png
