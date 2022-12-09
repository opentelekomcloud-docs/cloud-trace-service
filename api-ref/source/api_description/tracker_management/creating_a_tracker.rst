:original_name: en-us_topic_0168602251.html

.. _en-us_topic_0168602251:

Creating a Tracker
==================

All API URLs described in this section are case-sensitive.

Function
--------

This API is used to create a tracker.

A tracker will be automatically created when CTS is enabled. All traces recorded by CTS are associated with the tracker. Currently, only one tracker can be created for each tenant in a region.

Traces are retained in the CTS console for seven days. For long-term storage, you can enable Object Storage Service (OBS) and deliver real-time operation records to OBS buckets.

URI
---

POST /v1.0/{project_id}/tracker

The URI parameters are described in :ref:`Table1 Parameters in the URI <en-us_topic_0168602251__table6296289>`.

.. _en-us_topic_0168602251__table6296289:

.. table:: **Table 1** Parameters in the URI

   ========== ========= ====== ===========
   Parameter  Mandatory Type   Description
   ========== ========= ====== ===========
   project_id Yes       String Project ID.
   ========== ========= ====== ===========

Request
-------

-  Parameter description

   .. table:: **Table 2** Parameters in the request

      +------------------+----------------+-------------+-------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter        | Sub-Parameter  | Mandatory   | Type        | Description                                                                                                                                                                       |
      +==================+================+=============+=============+===================================================================================================================================================================================+
      | bucket_name      | N/A            | Yes         | String      | OBS bucket name. The value contains 3 to 63 characters and must start with a digit or lowercase letter. Only lowercase letters, digits, hyphens (-), and periods (.) are allowed. |
      +------------------+----------------+-------------+-------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | file_prefix_name | N/A            | No          | String      | Prefix of trace files that need to be stored in OBS buckets. The value can contain 0 to 64 characters, including letters, digits, hyphens (-), underscores (_), and periods (.).  |
      +------------------+----------------+-------------+-------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | lts              | is_lts_enabled | No          | Boolean     | Whether trace analysis is enabled.                                                                                                                                                |
      |                  |                |             |             |                                                                                                                                                                                   |
      |                  |                |             |             | .. note::                                                                                                                                                                         |
      |                  |                |             |             |                                                                                                                                                                                   |
      |                  |                |             |             |    When you enable trace analysis, a log group named **CTS** and a log stream named **system-trace** are created in LTS.                                                          |
      +------------------+----------------+-------------+-------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

-  Example request

   .. code-block::

      {
          "bucket_name" : "obs-f1da",
          "file_prefix_name" : "yO8Q",
          "lts" : {
              "is_lts_enabled" : true
          }
      }

Response
--------

-  Parameter description

   .. table:: **Table 3** Parameters in the response

      +------------------+----------------+---------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter        | Sub-Parameter  | Type    | Description                                                                                                                                                                       |
      +==================+================+=========+===================================================================================================================================================================================+
      | bucket_name      | N/A            | String  | OBS bucket name. The value contains 3 to 63 characters and must start with a digit or lowercase letter. Only lowercase letters, digits, hyphens (-), and periods (.) are allowed. |
      +------------------+----------------+---------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | file_prefix_name | N/A            | String  | Prefix of trace files that need to be stored in OBS buckets.                                                                                                                      |
      +------------------+----------------+---------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | status           | N/A            | String  | Status of a tracker. The value is **enabled**.                                                                                                                                    |
      +------------------+----------------+---------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | tracker_name     | N/A            | String  | Tracker name. The default value is **system**.                                                                                                                                    |
      +------------------+----------------+---------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | lts              | is_lts_enabled | Boolean | Whether trace analysis is enabled.                                                                                                                                                |
      +------------------+----------------+---------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      |                  | log_group_name | String  | Name of the Log Tank Service (LTS) log group.                                                                                                                                     |
      +------------------+----------------+---------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      |                  | log_topic_name | String  | Name of the LTS log stream.                                                                                                                                                       |
      +------------------+----------------+---------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

-  Example response

   .. code-block::

      {
          "bucket_name" : "obs-f1da",
          "file_prefix_name" : "yO8Q",
          "lts" : {
              "is_lts_enabled" : true,
              "log_group_name" : "CTS",
              "log_topic_name" : "system-trace"
          },
              "bucket_name" : "1214",
              "tracker_name" : "system",
               "file_prefix_name" : "",
               "status" : "enabled",
               "tracker_type" : "system"
      }

Returned Value
--------------

-  Normal

   .. table:: **Table 4** Return code for successful requests

      ============== ==========================
      Returned Value Description
      ============== ==========================
      201            The request is successful.
      ============== ==========================

-  Abnormal

   .. table:: **Table 5** Return code for failed requests

      +----------------+----------------------------------------------------------------------+
      | Returned Value | Description                                                          |
      +================+======================================================================+
      | 400            | The server failed to process the request.                            |
      +----------------+----------------------------------------------------------------------+
      | 403            | The server understood the request but refused to authorize it.       |
      +----------------+----------------------------------------------------------------------+
      | 500            | Failed to complete the request because of an internal service error. |
      +----------------+----------------------------------------------------------------------+
      | 401            | The request is rejected due to authentication failure.               |
      +----------------+----------------------------------------------------------------------+
      | 400            | The requested OBS bucket does not exist.                             |
      +----------------+----------------------------------------------------------------------+
