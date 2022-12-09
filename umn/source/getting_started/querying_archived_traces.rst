:original_name: en-us_topic_0030598636.html

.. _en-us_topic_0030598636:

Querying Archived Traces
========================

Scenarios
---------

CTS periodically compresses recorded traces into trace files and delivers them to OBS buckets. A trace file is a collection of traces. CTS generates trace files based on services and transfer periods. If there are a large number of traces, the system will adjust the number of traces contained in each trace file as needed.

This section describes how to obtain historical operation records from the trace files downloaded from OBS buckets.

Procedure
---------

#. Log in to the management console.

#. Click |image1| in the upper left corner to select the desired project.

#. Click **Service List** and choose **Management & Deployment** > **Cloud Trace Service**.

#. Choose **Tracker List** in the left navigation pane.

#. Click an OBS bucket name in the **OBS Bucket** column. You will be redirected to the bucket's details page on the OBS console.


   .. figure:: /_static/images/en-us_image_0237950267.png
      :alt: **Figure 1** Selecting an OBS bucket

      **Figure 1** Selecting an OBS bucket

#. Select the target trace by choosing in sequence an OBS bucket, the **CloudTraces** directory, a region, a year, a month, a day, a tracker name, and a service directory. Click **Download** in the **Operation** column to download the trace file to the default path. To download the trace file to a customized path, click **More** > **Download As**.

   -  The trace file storage path is as follows:

      *OBS bucket name* > **CloudTraces** **>** *Region* > *Year* > *Month* > *Day* > *Tracker name* > *Service directory*

      An example is *User-defined name* **> CloudTraces > region > 2016 > 5 > 19 > system > ECS**.

   -  The trace file naming format is as follows:

      *Trace file prefix*\ **\_CloudTrace\_**\ *Region/Region-project*\ \_\ *Time when the trace file was uploaded to OBS: Year-Month-Day*\ **T**\ *Hour-Minute-Second*\ **Z**\ \_\ *Character randomly generated*\ **.json.gz**

      Example: *File Prefix*\ **\_CloudTrace_region_2016-05-30T16-20-56Z_21d36ced8c8af71e.json.gz**

   .. note::

      The OBS bucket name and trace file prefix are customized and other parameters are automatically generated.

   For details on key fields in traces, see :ref:`Trace Structure <en-us_topic_0030598500>` and :ref:`Example Traces <en-us_topic_0044019595>`.


   .. figure:: /_static/images/en-us_image_0237950263.png
      :alt: **Figure 2** Viewing a trace file

      **Figure 2** Viewing a trace file

#. Decompress the downloaded package to obtain a JSON file with the same name as the package. Open the JSON file using a text file editor to view traces.

.. |image1| image:: /_static/images/en-us_image_0237950266.png
