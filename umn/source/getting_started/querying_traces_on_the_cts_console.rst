:original_name: en-us_topic_0030598499.html

.. _en-us_topic_0030598499:

Querying Traces on the CTS Console
==================================

Scenarios
---------

When you enable CTS, the system starts recording operations on cloud resources. Operation records of the last seven days are stored on the CTS console.

This section describes how to query or export operation records of the last seven days on the CTS console.

Procedure
---------

#. Log in to the management console.

#. Click |image1| in the upper left corner to select the desired project.

#. Click **Service List** and choose **Management & Deployment** > **Cloud Trace Service**.

#. Choose **Trace List** in the navigation pane on the left.

#. Set filters to search for desired traces. The following filters are available:

   -  **Trace Source**, **Resource Type**, and **Search By**.

      Select the desired content from the drop-down lists one by one.

      When you select **Trace name** for **Search By**, you need to select a trace name.

      When you select **Resource ID** for **Search By**, you need to enter a resource ID.

      When you select **Resource name**, you also need to select or enter a resource name.

      .. note::

         Options are available in the **Search By** drop-down list only when **Trace Source** and **Resource Type** are specified.

   -  **Operator**: Select a user.

   -  **Trace Status**: Select **All trace statuses**, **normal**, **warning**, or **incident**.

   -  In the upper right corner, choose **Last 1 hour**, **Last 1 day**, or **Last 1 week**, or specify a custom time range.

#. On the right of the filter box, click **Export**. CTS exports a CSV file listing query results.

#. Click |image2| on the left of the required trace to expand its details.


   .. figure:: /_static/images/en-us_image_0238416168.png
      :alt: **Figure 1** Expanded trace details

      **Figure 1** Expanded trace details

#. Click **View Trace** in the **Operation** column. In the **View Trace** dialog box, the trace structure details are displayed.


   .. figure:: /_static/images/en-us_image_0237950264.png
      :alt: **Figure 2** Viewing a trace

      **Figure 2** Viewing a trace

   For details on key fields in traces, see :ref:`Trace Structure <en-us_topic_0030598500>` and :ref:`Example Traces <en-us_topic_0044019595>`.

.. |image1| image:: /_static/images/en-us_image_0237950266.png
.. |image2| image:: /_static/images/en-us_image_0237950265.png
