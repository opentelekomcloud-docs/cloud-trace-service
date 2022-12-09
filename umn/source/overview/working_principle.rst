:original_name: en-us_topic_0043877299.html

.. _en-us_topic_0043877299:

Working Principle
=================

CTS directly connects to other cloud services, records operations on the cloud resources and the results, and stores these records in the form of trace files to OBS buckets in real time.

Before enabling CTS, you need to create an OBS bucket. When CTS is enabled, a tracker is created automatically. The tracker will generate trace files and send them to your specified OBS bucket.

The following operations can be performed on trace files:

-  Trace file creation and storage

   -  When operations, such as addition, deletion, and modification, are performed on the services connected with CTS, the services will record the operations in specified formats and send the records to CTS. Such services include Elastic Cloud Server (ECS), Elastic Volume Service (EVS), and Image Management Service (IMS).
   -  CTS keeps the operation records for seven days, and periodically delivers the records to your specified OBS buckets for long-term storage.

-  Trace file query

   -  You can query operation records in the last seven days on the **Trace List** page by time and other filters.
   -  To check operation records older than seven days, download trace files from OBS buckets.
   -  You can enable, disable, delete, or modify a tracker on the **Tracker** page on the CTS console.

   Let's use image creation as an example to show how CTS works. If you create an image in IMS, IMS will report a trace that records the operation to CTS. You can then view the trace on the CTS console. For long-term storage, CTS will transfer the trace to an OBS bucket.


   .. figure:: /_static/images/en-us_image_0000001381965089.jpg
      :alt: **Figure 1** CTS working principle

      **Figure 1** CTS working principle
