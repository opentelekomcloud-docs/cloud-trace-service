:original_name: en-us_cts_01_0002.html

.. _en-us_cts_01_0002:

Key Operations on SDRS
======================

Storage Disaster Recovery Service (SDRS) provides disaster recovery (DR) services for many cloud services, such as Elastic Cloud Server (ECS), Elastic Volume Service (EVS), and Dedicated Distributed Storage Service (DSS). SDRS uses multiple technologies, such as storage replication, data redundancy, and cache acceleration, to provide high data reliability and service continuity for users.

With CTS, you can record operations associated with SDRS for later query, audit, and backtracking.

.. table:: **Table 1** SDRS operations that can be recorded by CTS

   +--------------------------------------------------------------------------------------------------------+-----------------------+--------------------------+
   | Operation                                                                                              | Resource Type         | Trace Name               |
   +========================================================================================================+=======================+==========================+
   | Creating a protection group                                                                            | protectionGroup       | createProtectionGroup    |
   +--------------------------------------------------------------------------------------------------------+-----------------------+--------------------------+
   | Deleting a protection group                                                                            | protectionGroup       | deleteProtectionGroup    |
   +--------------------------------------------------------------------------------------------------------+-----------------------+--------------------------+
   | Updating a protection group                                                                            | protectionGroup       | updateProtectionGroup    |
   +--------------------------------------------------------------------------------------------------------+-----------------------+--------------------------+
   | Enabling protection for a protection group (when the protection group is in the **available** state)   | protectionGroup       | startProtectionGroup     |
   +--------------------------------------------------------------------------------------------------------+-----------------------+--------------------------+
   | Enabling protection for a protection group (when the protection group is in the **failed-over** state) | protectionGroup       | reprotectProtectionGroup |
   +--------------------------------------------------------------------------------------------------------+-----------------------+--------------------------+
   | Disabling protection for a protection group                                                            | protectionGroup       | stopProtectionGroup      |
   +--------------------------------------------------------------------------------------------------------+-----------------------+--------------------------+
   | Performing a failover for a protection group                                                           | protectionGroup       | failoverProtectionGroup  |
   +--------------------------------------------------------------------------------------------------------+-----------------------+--------------------------+
   | Performing a planned failover                                                                          | protectionGroup       | reverseProtectionGroup   |
   +--------------------------------------------------------------------------------------------------------+-----------------------+--------------------------+
   | An action performed when a job is not submitted by a protection group                                  | protectionGroup       | protectionGroupAction    |
   +--------------------------------------------------------------------------------------------------------+-----------------------+--------------------------+
   | Creating a protected instance                                                                          | protectedInstance     | createProtectedInstance  |
   +--------------------------------------------------------------------------------------------------------+-----------------------+--------------------------+
   | Deleting a protected instance                                                                          | protectedInstance     | deleteProtectedInstance  |
   +--------------------------------------------------------------------------------------------------------+-----------------------+--------------------------+
   | Updating a protected instance                                                                          | protectedInstance     | updateProtectedInstance  |
   +--------------------------------------------------------------------------------------------------------+-----------------------+--------------------------+
   | Attaching a replication pair to a protected instance                                                   | protectedInstance     | attachReplicationPair    |
   +--------------------------------------------------------------------------------------------------------+-----------------------+--------------------------+
   | Detaching a replication pair from a protected instance                                                 | protectedInstance     | detachReplicationPair    |
   +--------------------------------------------------------------------------------------------------------+-----------------------+--------------------------+
   | Adding a NIC to a protected instance                                                                   | protectedInstance     | addNic                   |
   +--------------------------------------------------------------------------------------------------------+-----------------------+--------------------------+
   | Deleting a NIC from a protected instance                                                               | protectedInstance     | deleteNic                |
   +--------------------------------------------------------------------------------------------------------+-----------------------+--------------------------+
   | Modifying the specifications of a protected instance                                                   | protectedInstance     | resizeProtectedInstance  |
   +--------------------------------------------------------------------------------------------------------+-----------------------+--------------------------+
   | Creating a replication pair                                                                            | replicationPair       | createReplicationPair    |
   +--------------------------------------------------------------------------------------------------------+-----------------------+--------------------------+
   | Deleting a replication pair                                                                            | replicationPair       | deleteReplicationPair    |
   +--------------------------------------------------------------------------------------------------------+-----------------------+--------------------------+
   | Updating a replication pair                                                                            | replicationPair       | updateReplicationPair    |
   +--------------------------------------------------------------------------------------------------------+-----------------------+--------------------------+
   | Expanding the capacity of a replication pair                                                           | replicationPair       | expandReplicationPair    |
   +--------------------------------------------------------------------------------------------------------+-----------------------+--------------------------+
   | Creating a DR drill                                                                                    | disasterRecoveryDrill | createDrDrill            |
   +--------------------------------------------------------------------------------------------------------+-----------------------+--------------------------+
   | Deleting a DR drill                                                                                    | disasterRecoveryDrill | deleteDrDrill            |
   +--------------------------------------------------------------------------------------------------------+-----------------------+--------------------------+
   | Updating a DR drill                                                                                    | disasterRecoveryDrill | updateDrDrill            |
   +--------------------------------------------------------------------------------------------------------+-----------------------+--------------------------+
