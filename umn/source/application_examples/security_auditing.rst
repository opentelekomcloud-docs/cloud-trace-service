:original_name: en-us_topic_0043371377.html

.. _en-us_topic_0043371377:

Security Auditing
=================

Scenarios
---------

You can query operation records matching specified conditions and check whether operations have been performed by authorized users for security analysis.

Prerequisites
-------------

You have enabled CTS and the tracker is running properly. For details on how to enable CTS, see :ref:`Enabling CTS <en-us_topic_0030598498>`.

Procedure
---------

The following shows how you can review records of EVS disk creation and deletion over the last two weeks.

#. Log in to the management console as an administrator.

#. Click |image1| in the upper left corner to select the desired project.

#. Click **Service List** and choose **Management & Deployment** > **Cloud Trace Service**.

#. Choose **Trace List** in the navigation pane on the left.

#. .. _en-us_topic_0043371377__li857921015615:

   Set filters in sequence: **Trace Source** > **Resource Type** > **Search By** > **Operator** > **Trace Status**. Then click **Query** to view the result.

   .. note::

      Select **evs** for **Trace Source**, **evs** for **Resource Type**, **Trace name** for **Search By**, and select **createVolume** or **deleteVolume**. Then, click **Query** to search for all EVS creation or deletion operations of the last seven days.

#. Choose **Tracker** in the left navigation pane to obtain an OBS bucket name.

#. Download traces older than seven days or all traces by following the instructions in :ref:`Querying Archived Traces <en-us_topic_0030598636>`.

#. .. _en-us_topic_0043371377__li38255771182015:

   In the downloaded file, locate required operation records by searching for keywords **createVolume** and **deleteVolume**.

#. Check the traces obtained in steps :ref:`5 <en-us_topic_0043371377__li857921015615>` and :ref:`8 <en-us_topic_0043371377__li38255771182015>` to see whether there are any unauthorized operations or operations that do not conform to security rules.

.. |image1| image:: /_static/images/en-us_image_0168422564.png
