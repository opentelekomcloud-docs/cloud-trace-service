:original_name: en-us_topic_0100363626.html

.. _en-us_topic_0100363626:

Key Operations on DRS
=====================

Data Replication Service (DRS) is an easy-to-use, stable, and efficient cloud service used for database migration and synchronization. DRS makes data flow between databases simple, greatly reducing data transfer costs. DRS enables you to quickly transfer data between databases in different scenarios.

With CTS, you can record operations associated with DRS for future query, audit, and backtrack operations.

.. table:: **Table 1** DRS operations that can be recorded by CTS

   =============== ============= ==========
   Operation       Resource Type Trace Name
   =============== ============= ==========
   Creating a task job           createJob
   Editing a task  job           modifyJob
   Deleting a task job           deleteJob
   Cloning a task  job           cloneJob
   Starting a task job           startJob
   Retrying a task job           retryJob
   =============== ============= ==========
