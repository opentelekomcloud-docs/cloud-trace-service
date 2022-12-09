:original_name: en-us_cts_01_0001.html

.. _en-us_cts_01_0001:

Configuring Key Event Notifications
===================================

Scenarios
---------

You can configure key event notifications on CTS so that Simple Message Notification (SMN) can send messages to notify you of key operations. This function is triggered by CTS, but notifications are sent by SMN. This function is used in the following scenarios:

-  Real-time detection and confirmation of high-risk operations (such as VM restart and security configuration changes), cost-sensitive operations (such as creating and deleting expensive resources), and service-sensitive operations (such as network configuration changes)
-  Detection and confirmation of unauthorized operations and operations such as logging in with high permissions
-  Interconnecting with your own audit system: All audit logs are synchronized to your audit system in real time for analysis of API calling success rate, unauthorized operations, security, and costs.

Note
----

-  Key event notifications are sent to subscribers by SMN. Therefore, before using CTS, you need to know how to create topics and add subscriptions on the SMN console.
-  Currently, you can create 100 key event notifications in CTS and specify key operations, users, and topics for each notification.
-  You can configure a maximum of 50 users in 10 user groups in key event notifications. For each notification, you can select multiple users in a same user group.
-  You can select a maximum of 1000 key operations of 100 cloud services for each notification.
-  Key event notification is an upgraded version of the original notification function. It is more powerful and provides more configuration items.

Procedure
---------

#. Log in to the management console.

#. Click |image1| in the upper left corner to select the desired project.

#. Click **Service List** and choose **Management & Deployment > Cloud Trace Service**.

#. In the navigation pane on the left, choose **Key Event Notifications**.

#. Click **Create Key Event Notification** in the upper right corner of the page. On the displayed page, specify required parameters.

#. Enter a key event notification name in the **Basic Information** area.

   **Notification Name**: Identifies key event notifications. This parameter is mandatory. The value contains a maximum of 64 characters, and only letters, numbers, and underscores (_) are allowed.

#. Configure key operations.

   Select **Typical**, **All**, or **Custom** based on your actual requirements:

   -  **Typical**: This option is suitable for enterprise routine auditing. Notifications will be sent when your specified operations occur, such as creating or deleting core resources of ECS, Virtual Private Cloud (VPC), EVS, or Key Management Service (KMS), and logging in as an Identity and Access Management (IAM) user.
   -  **All**: This option is suitable if you have connected CTS to your own audit systems. When **All** is chosen, you cannot deselect operations because all operations on all cloud services that have connected with CTS will trigger notifications. You are advised to use an SMN topic for which HTTPS is selected.
   -  **Custom**: This option is suitable for enterprises that require detection of high-risk, cost-sensitive, service-sensitive, and unauthorized operations. You can connect CTS with your own audit systems for log analysis. Select the operations that will trigger notifications. Up to 1000 operations of 100 services can be added for each notification. For details, see :ref:`Supported Services and Operation Lists <en-us_topic_0100236045>`.

#. Configure users.

   Specify users. SMN messages will be sent to subscribers when specified users perform key operations.

   -  If you select **All users**, SMN will notify subscribers of key operations initiated by all users.
   -  If you select **Specified users** and specify users, SMN will notify subscribers of key operations initiated by these users. You can configure a maximum of 50 users in 10 user groups. For each notification, you can select multiple users in a same user group.

#. Configure an SMN topic.

   -  If you select **Yes** for **Send Notification**, you can select an existing topic or click **Topic** to create one on the SMN console.
   -  If you select **No** for **Send Notification**, no further action is required.

#. Click **Create Now**. The **Key Event Notifications** page is displayed, showing all created key event notifications.

.. |image1| image:: /_static/images/en-us_image_0237964518.png
