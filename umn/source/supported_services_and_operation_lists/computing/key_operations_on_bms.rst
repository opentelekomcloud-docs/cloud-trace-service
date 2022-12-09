:original_name: en-us_topic_0100236048.html

.. _en-us_topic_0100236048:

Key Operations on BMS
=====================

A Bare Metal Server (BMS) is a physical server dedicated for individual tenants. It provides remarkable compute performance and stability for running key applications. The BMS service can be used in conjunction with other cloud services, such as Virtual Private Cloud (VPC), allowing you to enjoy the stable performance of server hosting and the high scalability of cloud resources together.

With CTS, you can record operations associated with BMS for future query, audit, and backtrack operations.

.. table:: **Table 1** BMS operations that can be recorded by CTS

   ================ ============= ======================
   Operation        Resource Type Trace Name
   ================ ============= ======================
   Creating a BMS   bms           createBareMetalServers
   Deleting a BMS   bms           deleteBareMetalServers
   Starting a BMS   bms           startBareMetalServers
   Stopping a BMS   bms           stopBareMetalServers
   Restarting a BMS bms           rebootBareMetalServers
   ================ ============= ======================
