:original_name: cts_api_0314.html

.. _cts_api_0314:

Deleting a Key Event Notification
=================================

Function
--------

This API is used to delete a key event notification.

URI
---

DELETE /v3/{project_id}/notifications

.. table:: **Table 1** URI parameter

   +------------+-----------+--------+------------------------------------------------------------------------------------------------------------------------+
   | Parameter  | Mandatory | Type   | Description                                                                                                            |
   +============+===========+========+========================================================================================================================+
   | project_id | Yes       | String | Project ID. For details, see section "Obtaining the Account ID and Project ID" in *Cloud Trace Service API Reference*. |
   +------------+-----------+--------+------------------------------------------------------------------------------------------------------------------------+

.. table:: **Table 2** Query parameter

   +-----------------+-----------+--------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Parameter       | Mandatory | Type   | Description                                                                                                                                            |
   +=================+===========+========+========================================================================================================================================================+
   | notification_id | Yes       | String | Notification ID. To batch delete notifications, enter multiple notification IDs separated by commas (,), for example, **notification_id="xxx1,ccc2"**. |
   +-----------------+-----------+--------+--------------------------------------------------------------------------------------------------------------------------------------------------------+

Request Parameters
------------------

None

Response Parameters
-------------------

**Status code: 400**

.. table:: **Table 3** Response body parameters

   ========== ====== ====================================
   Parameter  Type   Description
   ========== ====== ====================================
   error_code String Error code. Format: **CTS.**\ *XXX*.
   error_msg  String Error description.
   ========== ====== ====================================

Example Request
---------------

None

Example Response
----------------

None

Status Codes
------------

+-------------+--------------------------------------------------------------------------------------------------------+
| Status Code | Description                                                                                            |
+=============+========================================================================================================+
| 204         | The deletion is successful.                                                                            |
+-------------+--------------------------------------------------------------------------------------------------------+
| 400         | The server failed to process the request.                                                              |
+-------------+--------------------------------------------------------------------------------------------------------+
| 401         | The request is rejected due to authentication failure.                                                 |
+-------------+--------------------------------------------------------------------------------------------------------+
| 403         | The server understood the request but refused to authorize it.                                         |
+-------------+--------------------------------------------------------------------------------------------------------+
| 404         | The server failed to find the requested resource or some key event notifications failed to be deleted. |
+-------------+--------------------------------------------------------------------------------------------------------+
| 500         | The request failed to be executed or some trackers failed to be deleted.                               |
+-------------+--------------------------------------------------------------------------------------------------------+
| 503         | The requested service is unavailable. The client should not repeat the request without modifications.  |
+-------------+--------------------------------------------------------------------------------------------------------+

Error Codes
-----------

See :ref:`Error Codes <en-us_topic_0168602259>`.
