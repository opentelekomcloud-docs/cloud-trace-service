:original_name: en-us_topic_0100273731.html

.. _en-us_topic_0100273731:

Key Operations on EVS
=====================

An EVS disk is a virtual block storage service that is based on distributed architecture and can elastically scale up and down. EVS disks can be operated online. Using them is similar to using common server hard disks. Compared with common server hard disks, EVS disks have higher data reliability and I/O throughput capabilities. They are also easier to use. EVS disks apply to file systems, databases, or system software or other applications that require block storage devices.

With CTS, you can record operations associated with EVS for future query, audit, and backtrack operations.

.. table:: **Table 1** EVS operations that can be recorded by CTS

   ===================== ============= ============
   Operation             Resource Type Trace Name
   ===================== ============= ============
   Creating an EVS disk  evs           createVolume
   Updating an EVS disk  evs           updateVolume
   Expanding an EVS disk evs           extendVolume
   Deleting an EVS disk  evs           deleteVolume
   ===================== ============= ============
