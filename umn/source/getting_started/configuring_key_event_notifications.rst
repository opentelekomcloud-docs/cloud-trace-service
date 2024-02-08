:original_name: cts_01_00011.html

.. _cts_01_00011:

Configuring Key Event Notifications
===================================

Scenarios
---------

You can use this function for:

-  Real-time detection of high-risk operations (such as VM restart and security configuration changes), cost-sensitive operations (such as creating and deleting expensive resources), and service-sensitive operations (such as network configuration changes).
-  Detection of operations such as login of users with admin-level permissions or operations performed by users who do not have the required permissions.
-  Connection with your own audit system: You can synchronize all audit logs to your audit system in real time to analyze the API calling success rate, unauthorized operations, security, and costs.

Prerequisites
-------------

-  SMN sends key event notifications to subscribers. Before setting notifications, you need to know how to create topics and add subscriptions on the SMN console.
-  You can create up to 100 key event notifications on CTS:

   -  Specify key operations, users, and topics to customize notifications.
   -  Complete key event notifications can be sent to notification topics.
   -  Typical key event notifications can be sent to specified users and notification topics.

-  If CTS and Cloud Eye use the same message topic, they can receive messages from the same terminal but with different content.
-  You can configure one key event notification for operations initiated by a maximum of 50 users in 10 user groups. For each key event notification, you can add users from different user groups, but cannot select multiple user groups at once.

Creating a Key Event Notification
---------------------------------

#. Log in to the management console.

#. Click |image1| in the upper left corner and choose **Management & Deployment** > **Cloud Trace Service**. The CTS console is displayed.

#. In the navigation pane on the left, choose **Key Event Notifications**.

   The **Key Event Notifications** page is displayed.

#. Click **Create Key Event Notification**. On the displayed page, specify required parameters.

#. Enter a key event notification name.

   **Notification Name**: Identifies key event notifications. This parameter is mandatory. The name can contain up to 64 characters. Only letters, digits, and underscores (_) are allowed.

#. Configure key operations.

   -  **Operation Type**: Select **All** or **Custom**.

      -  **All**: This option is suitable if you have connected CTS to your own audit system.When **All** is chosen, you cannot deselect operations because all operations on all cloud services that have connected with CTS will trigger notifications.You are advised to use an SMN topic for which HTTPS is selected.

      -  **Custom**: This option is suitable for enterprises that require detection of high-risk, cost-sensitive, service-sensitive, and unauthorized operations. You can connect CTS to your own audit system for log analysis.

         Select the operations that will trigger notifications. Up to 1000 operations of 100 services can be added for each notification. For details, see :ref:`Supported Services and Operations <cts_03_0300>`.

#. Configure users.

   SMN messages will be sent to subscribers when the specified users perform key operations.

   -  If you select **All users**, SMN will notify subscribers of key operations initiated by all users.
   -  If you select **Specified users**, SMN will notify subscribers of key operations initiated by your specified users.

#. Configure an SMN topic.

   -  If you select **Yes** for **Send Notification**, you can select an existing topic or click **Topic** to create one on the SMN console.
   -  If you do not want to send notifications, no further action is required.

#. Click **OK**.

View Key Event Notification
---------------------------

#. Log in to the management console.
#. Click |image2| in the upper left corner and choose **Management & Deployment** > **Cloud Trace Service**. The CTS console is displayed.
#. In the navigation pane on the left, choose **Key Event Notifications**. The **Key Event Notifications** page is displayed.
#. Click **View** in the **Operation** column. The **View Key Event Notifications** page is displayed.

Enable Key Event Notification
-----------------------------

#. Log in to the management console.
#. Click |image3| in the upper left corner and choose **Management & Deployment** > **Cloud Trace Service**. The CTS console is displayed.
#. In the navigation pane on the left, choose **Key Event Notifications**. The **Key Event Notifications** page is displayed.
#. Click **Start** in the **Operation** column. The **Enabling Key Event Notifications** page is displayed.

   .. note::

      CTS can trigger key event notifications only after SMN is configured.

#. Click **Yes** to enable the key event notification function.

Modifying a Key Event Notification
----------------------------------

#. Log in to the management console.
#. Click |image4| in the upper left corner and choose **Management & Deployment** > **Cloud Trace Service**. The CTS console is displayed.
#. In the navigation pane on the left, choose **Key Event Notifications**. The **Key Event Notifications** page is displayed.
#. Click **More** > **Modify** in the **Operation** column. The **Key Event Notifications** page is displayed.
#. Then, click **OK**.

Deleting a Key Event Notification
---------------------------------

#. Log in to the management console.
#. Click |image5| in the upper left corner and choose **Management & Deployment** > **Cloud Trace Service**. The CTS console is displayed.
#. In the navigation pane on the left, choose **Key Event Notifications**. The **Key Event Notifications** page is displayed.
#. Choose **More** > **Delete** in the **Operation** column. The **Delete Key Event Notifications** page is displayed.
#. Click **Yes** to delete the key event notification function.

.. |image1| image:: /_static/images/en-us_image_0000001186930850.png
.. |image2| image:: /_static/images/en-us_image_0000001417288029.png
.. |image3| image:: /_static/images/en-us_image_0000001366607830.png
.. |image4| image:: /_static/images/en-us_image_0000001366287882.png
.. |image5| image:: /_static/images/en-us_image_0000001417089185.png
