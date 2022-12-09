:original_name: en-us_topic_0030594187.html

.. _en-us_topic_0030594187:

CTS
===

Log audit is core to information security audit. It is an essential part of security risk control for information systems in enterprises and public sectors. As more information systems are migrating to the cloud, standards on information security have been released around the globe, such as ISO/IEC 27000, GB/T 20945-2013, ITIL, and NIST SP 800.

Cloud Trace Service (CTS) is a log audit service for cloud security. It allows you to collect, store, and query resource operation records. You can use these records to perform security analysis, track resource changes, audit compliance, and locate faults.

CTS provides the following functions:

-  Operation recording: CTS records action taken on the console, API calls, and system-triggered actions.
-  Trace query: You can query traces of the last seven days on the CTS console by multiple filters, such as trace source, resource type, operator, and trace status.
-  Trace transfer: traces can be transferred to Object Storage Service (OBS) buckets periodically. During transfer, traces are compressed into trace files by service.
