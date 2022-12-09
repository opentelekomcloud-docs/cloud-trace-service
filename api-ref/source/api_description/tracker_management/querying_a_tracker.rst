:original_name: en-us_topic_0168602253.html

.. _en-us_topic_0168602253:

Querying a Tracker
==================

Function
--------

This API is used to query the details of a tracker. The details include the name of the tracker, name of the OBS bucket for storing traces, and prefix of the trace files stored in the OBS bucket.

URI
---

GET /v1.0/{project_id}/tracker?tracker_name={tracker_name}

The URI parameters are described in :ref:`Table1 Parameters in the URI <en-us_topic_0168602253__table9404449>`.

.. _en-us_topic_0168602253__table9404449:

.. table:: **Table 1** Parameters in the URI

   +-----------------+-----------------+-----------------+-----------------------------------------------------------------------------------------+
   | Parameter       | Mandatory       | Type            | Description                                                                             |
   +=================+=================+=================+=========================================================================================+
   | project_id      | Yes             | String          | Project ID                                                                              |
   +-----------------+-----------------+-----------------+-----------------------------------------------------------------------------------------+
   | tracker_name    | No              | String          | Tracker name.                                                                           |
   |                 |                 |                 |                                                                                         |
   |                 |                 |                 | If this parameter is not specified, all trackers will be queried.                       |
   |                 |                 |                 |                                                                                         |
   |                 |                 |                 | Currently, only one tracker is allowed for each tenant. The tracker name is **system**. |
   +-----------------+-----------------+-----------------+-----------------------------------------------------------------------------------------+

.. note::

   It is expected that CTS can support multiple trackers in the future. In this case, if you send a request where the parameter **tracker_name** is not specified (**GET /v1.0/{project_id}/tracker**), the response will be in array format. Otherwise, the response will be in object format.

Request
-------

-  Parameter description

   None

-  Example request

   .. code-block:: text

      GET /v1.0/{project_id}/tracker?tracker_name=system

Response
--------

-  Parameter description

   .. table:: **Table 2**

      +------------------+----------------+---------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter        | Sub-Parameter  | Type    | Description                                                                                                                                                                                                                                                                   |
      +==================+================+=========+===============================================================================================================================================================================================================================================================================+
      | tracker_name     | ``-``          | String  | Tracker name. It is set as **system** by default.                                                                                                                                                                                                                             |
      +------------------+----------------+---------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | bucket_name      | ``-``          | String  | OBS bucket name. It starts with a number or lowercase letter and contains 3 to 63 characters, including lowercase letters, numbers, hyphens (-), and periods (.)                                                                                                              |
      +------------------+----------------+---------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | file_prefix_name | ``-``          | String  | Prefix of trace files that need to be stored in OBS buckets                                                                                                                                                                                                                   |
      +------------------+----------------+---------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | status           | ``-``          | String  | Status of a tracker. The value can be **enabled** or **disabled**.                                                                                                                                                                                                            |
      +------------------+----------------+---------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | detail           | ``-``          | String  | This parameter is returned only when the tracker status is abnormal. It specifies the cause of the exception. The value will be **checkBucketExistFailed**, which indicates the failure to check the bucket, or **noBucket**, which indicates that the bucket does not exist. |
      +------------------+----------------+---------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | lts              | is_lts_enabled | Boolean | Whether trace analysis is enabled                                                                                                                                                                                                                                             |
      +------------------+----------------+---------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      |                  | log_group_name | String  | Name of the LTS log group                                                                                                                                                                                                                                                     |
      +------------------+----------------+---------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      |                  | log_topic_name | String  | Name of the LTS log stream                                                                                                                                                                                                                                                    |
      +------------------+----------------+---------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

-  Example response

   .. code-block::

      {
          "bucket_name" : "my_created_bucket",
          "tracker_name" : "system",
          "detail" : "noBucket",
          "file_prefix_name" : "some_folder",
          "status" : "disabled",
          "lts" : {
              "is_lts_enabled" : true,
              "log_group_name" : "CTS",
              "log_topic_name" : "tracker"
          },
              "bucket_name" : "1214",
              "tracker_name" : "system",

      }

Returned Value
--------------

-  Normal

   .. table:: **Table 3** Return code for successful requests

      +----------------+-------------------------------------------------------------+
      | Returned Value | Description                                                 |
      +================+=============================================================+
      | 200            | The request is successful and the query result is returned. |
      +----------------+-------------------------------------------------------------+

-  Abnormal

   .. table:: **Table 4** Return code for failed requests

      +----------------+----------------------------------------------------------------------+
      | Returned Value | Description                                                          |
      +================+======================================================================+
      | 400            | The server failed to process the request.                            |
      +----------------+----------------------------------------------------------------------+
      | 500            | Failed to complete the request because of an internal service error. |
      +----------------+----------------------------------------------------------------------+
      | 401            | Your access request is rejected.                                     |
      +----------------+----------------------------------------------------------------------+
      | 403            | You are forbidden to access the requested page.                      |
      +----------------+----------------------------------------------------------------------+
