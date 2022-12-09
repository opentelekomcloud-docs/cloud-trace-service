:original_name: en-us_topic_0100273717.html

.. _en-us_topic_0100273717:

Key Operations on OBS
=====================

OBS is a stable, secure, efficient, and easy-to-use cloud storage service. With the Representational State Transfer (REST) application programming interface (API), OBS is able to store any amount and form of unstructured data.

With CTS, you can record operations associated with OBS for future query, audit, and backtrack operations.

.. table:: **Table 1** OBS operations that can be recorded by CTS

   +------------------------------------------------------------+---------------+--------------------------+
   | Operation                                                  | Resource Type | Trace Name               |
   +============================================================+===============+==========================+
   | Deleting a bucket                                          | bucket        | deleteBucket             |
   +------------------------------------------------------------+---------------+--------------------------+
   | Deleting the bucket CORS configuration                     | bucket        | deleteBucketCors         |
   +------------------------------------------------------------+---------------+--------------------------+
   | Deleting the custom domain configuration                   | bucket        | deleteBucketCustomdomain |
   +------------------------------------------------------------+---------------+--------------------------+
   | Deleting the bucket lifecycle configuration                | bucket        | deleteBucketLifecycle    |
   +------------------------------------------------------------+---------------+--------------------------+
   | Deleting the bucket policy configuration                   | bucket        | deleteBucketPolicy       |
   +------------------------------------------------------------+---------------+--------------------------+
   | Deleting the bucket cross-region replication configuration | bucket        | deleteBucketReplication  |
   +------------------------------------------------------------+---------------+--------------------------+
   | Deleting the bucket tagging configuration                  | bucket        | deleteBucketTagging      |
   +------------------------------------------------------------+---------------+--------------------------+
   | Deleting the bucket website configuration                  | bucket        | deleteBucketWebsite      |
   +------------------------------------------------------------+---------------+--------------------------+
   | Deleting bucket data                                       | bucket        | deleteBucketdata         |
   +------------------------------------------------------------+---------------+--------------------------+
   | Creating a bucket                                          | bucket        | createBucket             |
   +------------------------------------------------------------+---------------+--------------------------+
   | Setting the bucket ACL                                     | bucket        | setBucketAcl             |
   +------------------------------------------------------------+---------------+--------------------------+
   | Setting the bucket CORS                                    | bucket        | setBucketCors            |
   +------------------------------------------------------------+---------------+--------------------------+
   | Setting a custom domain name of a bucket                   | bucket        | setBucketCustomdomain    |
   +------------------------------------------------------------+---------------+--------------------------+
   | Setting the bucket lifecycle                               | bucket        | setBucketLifecycle       |
   +------------------------------------------------------------+---------------+--------------------------+
   | Setting the bucket logging                                 | bucket        | setBucketLogging         |
   +------------------------------------------------------------+---------------+--------------------------+
   | Setting the bucket notification                            | bucket        | setBucketNotification    |
   +------------------------------------------------------------+---------------+--------------------------+
   | Setting the bucket policy                                  | bucket        | setBucketPolicy          |
   +------------------------------------------------------------+---------------+--------------------------+
   | Setting the bucket quota                                   | bucket        | setBucketQuota           |
   +------------------------------------------------------------+---------------+--------------------------+
   | Setting a cross-domain replication of a bucket             | bucket        | setBucketReplication     |
   +------------------------------------------------------------+---------------+--------------------------+
   | Setting the bucket storage class                           | bucket        | setBucketStorageclass    |
   +------------------------------------------------------------+---------------+--------------------------+
   | Setting a bucket tag                                       | bucket        | setBucketTagging         |
   +------------------------------------------------------------+---------------+--------------------------+
   | Setting bucket versioning                                  | bucket        | setBucketVersioning      |
   +------------------------------------------------------------+---------------+--------------------------+
   | Setting a static domain name of a bucket                   | bucket        | setBucketWebsite         |
   +------------------------------------------------------------+---------------+--------------------------+
