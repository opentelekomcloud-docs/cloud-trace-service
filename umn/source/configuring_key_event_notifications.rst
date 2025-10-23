:original_name: en-us_cts_01_0001.html

.. _en-us_cts_01_0001:

Configuring Key Event Notifications
===================================

Scenarios
---------

You can use this function for:

-  Real-time detection of high-risk operations (such as VM restart and security configuration changes), cost-sensitive operations (such as creating and deleting expensive resources), and service-sensitive operations (such as network configuration changes).
-  Detection of operations such as login of users with admin-level permissions or operations performed by users who do not have the required permissions.
-  Connection with your own audit system: You can synchronize all audit logs to your audit system in real time to analyze the API calling success rate, unauthorized operations, security, and costs.

Usage Description
-----------------

-  SMN sends key event notifications to subscribers. Before setting notifications, you need to know how to create topics and add subscriptions on the SMN console.
-  You can create up to 100 key event notifications on CTS:

   -  Specify key operations, users, and topics to customize notifications.
   -  Complete key event notifications can be sent to notification topics.

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

   Select the operations that will trigger notifications. When a selected operation is performed, an SMN notification is sent immediately.

   -  **Operation Type**: Select **All** or **Custom**.

      -  **All**: This option is suitable if you have connected CTS to your own audit system. When **All** is chosen, you cannot deselect operations because all operations on all cloud services that have connected with CTS will trigger notifications. You are advised to use an SMN topic for which HTTPS is selected.

      -  **Custom**: This option is suitable for enterprises that require detection of high-risk, cost-sensitive, service-sensitive, and unauthorized operations. You can connect CTS to your own audit system for log analysis.

         Customize the operations that will trigger notifications. Up to 1000 operations of 100 services can be added for each notification. For details, see :ref:`Supported Services and Operations <cts_03_0300>`.

   -  **Advanced Filter**: You can set an advanced filter to specify the operations that will trigger notifications. Operations can be filtered by fields **api_version**, **code**, **trace_rating**, **trace_type**, **resource_id**, and **resource_name**. Up to six filter conditions can be set. When you configure multiple conditions, specify whether an operation is considered a match when all conditions are met (AND) or any of the conditions are met (OR).

      .. table:: **Table 1** Advanced filtering parameters

         +-----------------------------------+-----------------------------------------------------------------------------------------------------------------+
         | Parameter                         | Description                                                                                                     |
         +===================================+=================================================================================================================+
         | api_version                       | Version of the API called in a trace.                                                                           |
         |                                   |                                                                                                                 |
         |                                   | Enumerated values:                                                                                              |
         |                                   |                                                                                                                 |
         |                                   | -  v1                                                                                                           |
         |                                   | -  v3                                                                                                           |
         +-----------------------------------+-----------------------------------------------------------------------------------------------------------------+
         | code                              | HTTP status code returned by an API.                                                                            |
         +-----------------------------------+-----------------------------------------------------------------------------------------------------------------+
         | trace_rating                      | Trace status.                                                                                                   |
         |                                   |                                                                                                                 |
         |                                   | Enumerated values:                                                                                              |
         |                                   |                                                                                                                 |
         |                                   | -  normal                                                                                                       |
         |                                   | -  warning                                                                                                      |
         |                                   | -  incident                                                                                                     |
         +-----------------------------------+-----------------------------------------------------------------------------------------------------------------+
         | trace_type                        | Trace type.                                                                                                     |
         |                                   |                                                                                                                 |
         |                                   | Enumerated values:                                                                                              |
         |                                   |                                                                                                                 |
         |                                   | -  ApiCall                                                                                                      |
         |                                   | -  ConsoleAction                                                                                                |
         |                                   | -  SystemAction                                                                                                 |
         +-----------------------------------+-----------------------------------------------------------------------------------------------------------------+
         | resource_id                       | ID of a cloud service resource on which operations are performed. Example: **5a0215bed7a14de38193a******facef** |
         +-----------------------------------+-----------------------------------------------------------------------------------------------------------------+
         | resource_name                     | Resource name recorded in a trace.                                                                              |
         +-----------------------------------+-----------------------------------------------------------------------------------------------------------------+

#. Configure users.

   SMN messages will be sent to subscribers when the specified users perform key operations.

   -  If you select **All users**, SMN will notify subscribers of key operations initiated by all users.
   -  If you select **Specified users**, SMN will notify subscribers of key operations initiated by your specified users.

#. Configure an SMN topic.

   -  When **Yes** is selected for **Send Notification**:

      -  **SMN Topic**: You can select an existing topic or click **SMN** to create one on the SMN console.

   -  If you do not want to send notifications, no further action is required.

#. Click **OK**.

Managing Key Event Notifications
--------------------------------

After you create a key event notification, you can view its name, status, template, and SMN topic in the notification list and delete it as required.

#. Log in to the management console.

#. Click |image2| in the upper left corner and choose **Management & Deployment** > **Cloud Trace Service**. The CTS console is displayed.

#. Choose **Key Event Notifications** in the navigation pane on the left. On the displayed page, perform the following operations as required. For details, see :ref:`Table 2 <en-us_cts_01_0001__en-us_topic_0000001240718676_en-us_topic_0179639609_table1679219139498>`.

   .. _en-us_cts_01_0001__en-us_topic_0000001240718676_en-us_topic_0179639609_table1679219139498:

   .. table:: **Table 2** Related operations

      +--------------------------------------------+--------------------------------------------------------------------------------------------------------------------+
      | Operation                                  | Description                                                                                                        |
      +============================================+====================================================================================================================+
      | Viewing a key event notification           | Click **View** in the **Operation** column to view the operation list and user list details of the notification.   |
      +--------------------------------------------+--------------------------------------------------------------------------------------------------------------------+
      | Enable/Disable a key event notification    | Click **Enable** or **Disable** in the **Operation** column.                                                       |
      |                                            |                                                                                                                    |
      |                                            | .. note::                                                                                                          |
      |                                            |                                                                                                                    |
      |                                            |    CTS can trigger key event notifications only after SMN is configured.                                           |
      +--------------------------------------------+--------------------------------------------------------------------------------------------------------------------+
      | Modifying a key event notification         | Click **More** > **Modify** in the **Operation** column to modify the configuration of the key event notification. |
      +--------------------------------------------+--------------------------------------------------------------------------------------------------------------------+
      | Deleting a key event notification          | Click **More** > **Delete** in the **Operation** column.                                                           |
      +--------------------------------------------+--------------------------------------------------------------------------------------------------------------------+
      | Refreshing the key event notification list | Click |image3| in the upper right corner.                                                                          |
      +--------------------------------------------+--------------------------------------------------------------------------------------------------------------------+

.. |image1| image:: /_static/images/en-us_image_0000002344716056.png
.. |image2| image:: /_static/images/en-us_image_0000002378514073.png
.. |image3| image:: /_static/images/en-us_image_0000002378673993.png
