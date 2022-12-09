:original_name: en-us_topic_0168602243.html

.. _en-us_topic_0168602243:

Querying a Specified API Version
================================

Function
--------

This API is used to query a specified API version of CTS.

URI
---

GET/{api_version}

The URI parameters are described in :ref:`Table 1 <en-us_topic_0168602243__t2f4b2999b4784e78845eefcc5eefac90>`.

.. _en-us_topic_0168602243__t2f4b2999b4784e78845eefcc5eefac90:

.. table:: **Table 1** Parameters in the URI

   =========== ========= ===========
   Parameter   Mandatory Description
   =========== ========= ===========
   api_version Yes       API version
   =========== ========= ===========

Request
-------

None

Response
--------

-  Parameter description

   .. table:: **Table 2** Parameters in the response

      +-----------------+-----------------+-----------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter       | Mandatory       | Type            | Description                                                                                                                                                                                   |
      +=================+=================+=================+===============================================================================================================================================================================================+
      | version         | Yes             | Array           | Information of the API version.                                                                                                                                                               |
      +-----------------+-----------------+-----------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | id              | Yes             | String          | Version ID (version number), for example, v1.                                                                                                                                                 |
      +-----------------+-----------------+-----------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | links           | Yes             | String          | API URL                                                                                                                                                                                       |
      +-----------------+-----------------+-----------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | href            | Yes             | String          | Reference address of the current API version                                                                                                                                                  |
      +-----------------+-----------------+-----------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | rel             | Yes             | String          | Relationship between the current API version and the referenced address                                                                                                                       |
      +-----------------+-----------------+-----------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | version         | Yes             | String          | If microversions are supported by the APIs of the given version, the maximum microversion supported will be displayed. If microversions are not supported, this parameter will be left blank. |
      +-----------------+-----------------+-----------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | status          | Yes             | String          | Version status. The value will be one of the following:                                                                                                                                       |
      |                 |                 |                 |                                                                                                                                                                                               |
      |                 |                 |                 | **CURRENT**: The version is the primary version.                                                                                                                                              |
      |                 |                 |                 |                                                                                                                                                                                               |
      |                 |                 |                 | **SUPPORTED**: The version is an old version, but it is still supported.                                                                                                                      |
      |                 |                 |                 |                                                                                                                                                                                               |
      |                 |                 |                 | **DEPRECATED**: The version is a deprecated version, which may be deleted later.                                                                                                              |
      +-----------------+-----------------+-----------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | updated         | Yes             | String          | Version release time, which is the Coordinated Universal time (UTC). For example, the release time of v1 is **2014-06-28T12:20:21Z**.                                                         |
      +-----------------+-----------------+-----------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | min_version     | No              | String          | If microversions are supported by the APIs of the given version, the minimum microversion supported will be displayed. If microversions are not supported, this parameter will be left blank. |
      +-----------------+-----------------+-----------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

-  Example response

   .. code-block::

      {
        "version":
          {
            "id": "v1.0",
            "links": [
              {
                "href": "https://x.x.x.x/v1.0/",
                "rel": "self"
              }
            ],
            "min_version": "",
            "status": "CURRENT",
            "updated": "2018-09-30T00:00:00Z",
            "version": ""
          }
        ]
      }

Returned Value
--------------

-  Normal

   200

-  Abnormal

   .. table:: **Table 3** Return code for failed requests

      +---------------------------+----------------------------------------------------------------------+
      | Returned Value            | Description                                                          |
      +===========================+======================================================================+
      | 400 Bad Request           | Request error.                                                       |
      +---------------------------+----------------------------------------------------------------------+
      | 401 Unauthorized          | The authentication information is not provided or is incorrect.      |
      +---------------------------+----------------------------------------------------------------------+
      | 403 Forbidden             | The request was forbidden.                                           |
      +---------------------------+----------------------------------------------------------------------+
      | 404 Not Found             | The server failed to find the requested resource.                    |
      +---------------------------+----------------------------------------------------------------------+
      | 408 Request Timeout       | The request timed out.                                               |
      +---------------------------+----------------------------------------------------------------------+
      | 429 Too Many Requests     | The number of requests exceeded the upper limit.                     |
      +---------------------------+----------------------------------------------------------------------+
      | 500 Internal Server Error | Failed to complete the request because of an internal service error. |
      +---------------------------+----------------------------------------------------------------------+
      | 503 Service Unavailable   | The service is currently unavailable.                                |
      +---------------------------+----------------------------------------------------------------------+
