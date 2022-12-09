:original_name: en-us_topic_0168602223.html

.. _en-us_topic_0168602223:

Deleting a Tracker
==================

Function
--------

This API is used to delete a tracker. Deleting a tracker has no impact on the operation records that have been generated. When you enable CTS again, you can still view those records.

URI
---

DELETE /v1.0/{project_id}/tracker?tracker_name={tracker_name}

The URI parameters are described in :ref:`Table1 Parameters in the URI <en-us_topic_0168602223__table4080300>`.

.. _en-us_topic_0168602223__table4080300:

.. table:: **Table 1** Parameters in the URI

   +-----------------+-----------------+-----------------+-------------------------------------------------------------------+
   | Parameter       | Mandatory       | Type            | Description                                                       |
   +=================+=================+=================+===================================================================+
   | project_id      | Yes             | String          | Project ID                                                        |
   +-----------------+-----------------+-----------------+-------------------------------------------------------------------+
   | tracker_name    | No              | String          | Tracker name.                                                     |
   |                 |                 |                 |                                                                   |
   |                 |                 |                 | If this parameter is not specified, all trackers will be deleted. |
   +-----------------+-----------------+-----------------+-------------------------------------------------------------------+

Request
-------

-  Parameter description

   None

-  Example request

   .. code-block:: text

      DELETE /v1.0/{project_id}/tracker?tracker_name=system

Response
--------

-  Parameter description

   None

-  Example response

   None

Returned Value
--------------

-  Normal

   .. table:: **Table 2** Return code for successful requests

      ============== ====================================
      Returned Value Description
      ============== ====================================
      204            The tracker is deleted successfully.
      ============== ====================================

-  Abnormal

   .. table:: **Table 3** Return code for failed requests

      +----------------+------------------------------------------------------------------------------------+
      | Returned Value | Description                                                                        |
      +================+====================================================================================+
      | 400            | The server failed to process the request.                                          |
      +----------------+------------------------------------------------------------------------------------+
      | 404            | The server failed to find the requested resource or deleting some trackers failed. |
      +----------------+------------------------------------------------------------------------------------+
      | 500            | The request failed to be executed or some trackers failed to be deleted.           |
      +----------------+------------------------------------------------------------------------------------+
      | 401            | Your access request is rejected.                                                   |
      +----------------+------------------------------------------------------------------------------------+
      | 403            | You are forbidden to access the requested page.                                    |
      +----------------+------------------------------------------------------------------------------------+
