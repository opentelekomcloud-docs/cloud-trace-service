:original_name: en-us_topic_0030598499.html

.. _en-us_topic_0030598499:

Querying Real-Time Traces
=========================

Scenarios
---------

After CTS is enabled, the tracker starts recording operations on cloud resources. CTS stores operation records for the last seven days.

This section describes how to query operation records of the last seven days on the CTS console.

Procedure
---------

#. Log in to the management console.

#. Click |image1| in the upper left corner and choose **Management & Deployment** > **Cloud Trace Service**. The CTS console is displayed.

#. In the navigation pane on the left, choose **Trace List**.

#. Set filters to search for your desired traces, as shown in :ref:`Figure 1 <en-us_topic_0030598499__en-us_topic_0179639644_f402e07400398464a97ed73852447a5de>`. The following filters are available:

   .. _en-us_topic_0030598499__en-us_topic_0179639644_f402e07400398464a97ed73852447a5de:

   .. figure:: /_static/images/en-us_image_0295789897.png
      :alt: **Figure 1** Filters

      **Figure 1** Filters

   -  **Trace Source**, **Resource Type**, and **Search By**

      Select a filter from the drop-down list.

      If you select **Resource ID** for **Search By**, specify a resource ID.

   -  **Operator**: Select a user.

   -  **Trace Status**: Select **All trace statuses**, **Normal**, **Warning**, or **Incident**.

   -  Time range: You can query traces generated during any time range in the last few days.

#. Click **Export** on the right to export all traces in the query result as a CSV file. The file can contain up to 5000 records.

#. Click |image2| on the left of a trace to expand its details.

   |image3|

#. Click **View Trace** in the **Operation** column. The trace details are displayed.

   |image4|

   |image5|

   For details about key fields in the trace structure, see :ref:`Trace Structure <cts_03_0010>` and :ref:`Example Traces <cts_03_0011>`.

.. |image1| image:: /_static/images/en-us_image_0000001187249376.png
.. |image2| image:: /_static/images/en-us_image_0179639581.jpg
.. |image3| image:: /_static/images/en-us_image_0000001460694917.png
.. |image4| image:: /_static/images/en-us_image_0000001410575694.png
.. |image5| image:: /_static/images/en-us_image_0179639495.png
