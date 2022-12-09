:original_name: en-us_topic_0043371378.html

.. _en-us_topic_0043371378:

Resource Tracking
=================

Scenarios
---------

You can view operation records of a cloud resource throughout its lifecycle.

Prerequisites
-------------

You have enabled CTS and the tracker is running properly. For details on how to enable CTS, see :ref:`Enabling CTS <en-us_topic_0030598498>`.

Procedure
---------

The following takes the records of all operations on an ECS as an example.

#. Log in to the management console as an administrator.

#. Click |image1| in the upper left corner to select the desired project.

#. Click **Service List** and choose **Management & Deployment** > **Cloud Trace Service**.

#. Choose **Trace List** in the navigation pane on the left.

#. .. _en-us_topic_0043371378__li36410601182:

   Set filters in sequence: **Trace Source** > **Resource Type** > **Search By**. Then click **Query** to view the result.

   .. note::

      Select **ecs** for **Trace Source**, **ecs** for **Resource Type**, **Resource ID** for **Search By**, and enter the ID of the VM. Click **Query** to obtain the traces generated in the last seven days.

#. Choose **Tracker** in the left navigation pane to obtain an OBS bucket name.

#. .. _en-us_topic_0043371378__li14173783182013:

   Download traces older than seven days or all traces by following the instructions in :ref:`Querying Archived Traces <en-us_topic_0030598636>`.

#. Check all the traces obtained in steps :ref:`5 <en-us_topic_0043371378__li36410601182>` and :ref:`7 <en-us_topic_0043371378__li14173783182013>`.

.. |image1| image:: /_static/images/en-us_image_0168422564.png
