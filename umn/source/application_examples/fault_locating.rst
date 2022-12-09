:original_name: en-us_topic_0043371379.html

.. _en-us_topic_0043371379:

Fault Locating
==============

Scenarios
---------

If a resource or an action encounters an exception, you can query operation records for the resource or action in a specified time period and view the requests and responses to facilitate troubleshooting.

Prerequisites
-------------

You have enabled CTS and the tracker is running properly. For details on how to enable CTS, see :ref:`Enabling CTS <en-us_topic_0030598498>`.

Procedure
---------

To locate an ECS fault which occurred in the morning:

#. Log in to the management console as an administrator.
#. Click |image1| in the upper left corner to select the desired project.
#. Click **Service List** and choose **Management & Deployment** > **Cloud Trace Service**.
#. Choose **Trace List** in the navigation pane on the left.
#. Set filters in sequence: **Trace Source** > **Resource Type** > **Search By**. Then click **Query** to view the result.

   .. note::

      Select **ecs** for **Trace Source**, **ecs** for **Resource Type**, and **Resource ID** for **Search By**. Enter the ID of the faulty virtual machine (VM), and select a time range from 06:00:00 to 12:00:00 on the day when the fault occurred in the upper right corner. Then click **Query**.

#. Check the returned traces, especially the request type and response of each trace. Note any traces whose status is **warning** or **incident**, and any traces whose response indicates a failure.

To locate a fault after an ECS server failed to be created:

#. Log in to the management console as an administrator.
#. Click |image2| in the upper left corner to select the desired project.
#. Click **Service List** and choose **Management & Deployment** > **Cloud Trace Service**.
#. Choose **Trace List** in the navigation pane on the left.
#. Select **esc** for **Trace Source**, **ecs** for **Resource Type**, and **warning** for **Trace Status**. In the returned traces, locate the trace named **createSingleServer**.
#. Check the trace details and locate the fault based on the error code or error message.

.. |image1| image:: /_static/images/en-us_image_0237964513.png
.. |image2| image:: /_static/images/en-us_image_0237950266.png
