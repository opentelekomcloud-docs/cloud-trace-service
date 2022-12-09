:original_name: en-us_topic_0168602227.html

.. _en-us_topic_0168602227:

Modifying a Tracker
===================

Function
--------

CTS allows you to modify configuration parameters of a created tracker, including parameters related to **Transfer to OBS** and **Trace Analysis**. You can also change tracker status by clicking **Enable** or **Disable** in the **Operation** column. Modifying tracker parameters does not affect the existing operation records. After the modification is complete, the system will immediately start recording operations based on the new rule.

URI
---

PUT /v1.0/{project_id}/tracker/{tracker_name}

The URI parameters are described in :ref:`Table1 Parameters in the URI <en-us_topic_0168602227__table25483595>`.

.. _en-us_topic_0168602227__table25483595:

.. table:: **Table 1** Parameters in the URI

   +--------------+-----------+--------+-------------------------------------------------------------------------------------------------------+
   | Parameter    | Mandatory | Type   | Description                                                                                           |
   +==============+===========+========+=======================================================================================================+
   | project_id   | Yes       | String | Project ID                                                                                            |
   +--------------+-----------+--------+-------------------------------------------------------------------------------------------------------+
   | tracker_name | Yes       | String | Tracker name. Currently, only one tracker is allowed for each tenant. The tracker name is **system**. |
   +--------------+-----------+--------+-------------------------------------------------------------------------------------------------------+

Request
-------

-  Parameter description

   .. table:: **Table 2** Parameters in the request

      +------------------+----------------+-------------+-------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter        | Sub-Parameter  | Mandatory   | Type        | Description                                                                                                                                                                   |
      +==================+================+=============+=============+===============================================================================================================================================================================+
      | bucket_name      | N/A            | Yes         | String      | OBS bucket name. It starts with a number or lowercase letter and contains 3 to 63 characters, including lowercase letters, numbers, hyphens (-), and periods (.)              |
      +------------------+----------------+-------------+-------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | file_prefix_name | N/A            | No          | String      | Prefix of trace files that need to be stored in OBS buckets. The value contains 0 to 64 characters, including letters, numbers, hyphens (-), underscores (_), and periods (.) |
      +------------------+----------------+-------------+-------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | status           | N/A            | No          | String      | Status of a tracker. The value can be **enabled** or **disabled**. If you change the value to **disabled**, the tracker stops recording traces.                               |
      +------------------+----------------+-------------+-------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | lts              | is_lts_enabled | Yes         | Boolean     | Whether trace analysis is enabled.                                                                                                                                            |
      |                  |                |             |             |                                                                                                                                                                               |
      |                  |                |             |             | .. note::                                                                                                                                                                     |
      |                  |                |             |             |                                                                                                                                                                               |
      |                  |                |             |             |    When you enable trace analysis, a log group named **CTS** and a log stream named **system-trace** are created in LTS.                                                      |
      +------------------+----------------+-------------+-------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

-  Example request

   .. code-block:: text

      PUT /v1.0/{project_id}/tracker/system
      {
          "bucket_name" : "my_created_bucket",
          "file_prefix_name" : "some_folder",
          "lts" : {
              "is_lts_enabled" : true,
          },
          "status" : "disabled"
      }

Response
--------

-  Parameter description

   .. table:: **Table 3** Parameters in the response

      +------------------+----------------+---------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter        | Sub-Parameter  | Type    | Description                                                                                                                                                      |
      +==================+================+=========+==================================================================================================================================================================+
      | tracker_name     | N/A            | String  | Tracker name. It is set as **system** by default.                                                                                                                |
      +------------------+----------------+---------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | bucket_name      | N/A            | String  | OBS bucket name. It starts with a number or lowercase letter and contains 3 to 63 characters, including lowercase letters, numbers, hyphens (-), and periods (.) |
      +------------------+----------------+---------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | file_prefix_name | N/A            | String  | Prefix of trace files that need to be stored in OBS buckets.                                                                                                     |
      +------------------+----------------+---------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | status           | N/A            | String  | Status of a tracker. The value can be **enabled** or **disabled**.                                                                                               |
      +------------------+----------------+---------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | lts              | is_lts_enabled | Boolean | Whether trace analysis is enabled.                                                                                                                               |
      +------------------+----------------+---------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      |                  | log_group_name | String  | Name of the LTS log group.                                                                                                                                       |
      +------------------+----------------+---------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      |                  | log_topic_name | String  | Name of the LTS log stream.                                                                                                                                      |
      +------------------+----------------+---------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+

-  Example response

.. code-block::

   {
       "bucket_name" : "my_created_bucket",
       "tracker_name" : "system",
       "file_prefix_name" : "some_folder",
       "lts" : {
           "is_lts_enabled" : true,
           "log_group_name" : "CTS",
           "log_topic_name" : "system-trace"
       },
       "status" : "disabled"
           "bucket_name" : "1214",
           "tracker_name" : "system",
   }

Returned Value
--------------

-  Normal

   .. table:: **Table 4** Return code for successful requests

      ============== ======================================
      Returned Value Description
      ============== ======================================
      200            The request is successfully processed.
      ============== ======================================

-  Abnormal

   .. table:: **Table 5** Return code for failed requests

      +----------------+----------------------------------------------------------------------+
      | Returned Value | Description                                                          |
      +================+======================================================================+
      | 400            | The server failed to process the request.                            |
      +----------------+----------------------------------------------------------------------+
      | 404            | The server failed to find the requested resource.                    |
      +----------------+----------------------------------------------------------------------+
      | 500            | Failed to complete the request because of an internal service error. |
      +----------------+----------------------------------------------------------------------+
      | 401            | Your access request is rejected.                                     |
      +----------------+----------------------------------------------------------------------+
      | 403            | You are forbidden to access the requested page.                      |
      +----------------+----------------------------------------------------------------------+
