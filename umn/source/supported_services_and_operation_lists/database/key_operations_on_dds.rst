:original_name: en-us_topic_0100363627.html

.. _en-us_topic_0100363627:

Key Operations on DDS
=====================

Document Database Service (DDS) is compatible with the MongoDB protocol and is secure, highly available, reliable, scalable, and easy to use. It provides DB instance creation, scaling, redundancy, backup, restoration, monitoring, and alarm reporting functions with just a few clicks on the DDS console.

With CTS, you can record operations associated with DDS for future query, audit, and backtrack operations.

.. table:: **Table 1** DDS operations recorded by CTS

   +--------------------------------------+----------------+--------------------------+
   | Operation                            | Resource Type  | Trace Name               |
   +======================================+================+==========================+
   | Restoring data to a new DB instance  | instance       | ddsRestoreToNewInstance  |
   +--------------------------------------+----------------+--------------------------+
   | Creating a DB instance               | instance       | ddsCreateInstance        |
   +--------------------------------------+----------------+--------------------------+
   | Deleting a DB instance               | instance       | ddsDeleteInstance        |
   +--------------------------------------+----------------+--------------------------+
   | Restarting a DB instance             | instance       | ddsRestartInstance       |
   +--------------------------------------+----------------+--------------------------+
   | Scaling up a DB instance             | instance       | ddsGrowInstance          |
   +--------------------------------------+----------------+--------------------------+
   | Scaling up storage space             | instance       | ddsExtendInstanceVolume  |
   +--------------------------------------+----------------+--------------------------+
   | Resetting the database password      | instance       | ddsResetPassword         |
   +--------------------------------------+----------------+--------------------------+
   | Renaming a DB instance               | instance       | ddsRenameInstance        |
   +--------------------------------------+----------------+--------------------------+
   | Modifying a DB instance port         | instance       | ddsModifyInstancePort    |
   +--------------------------------------+----------------+--------------------------+
   | Creating a backup                    | backup         | ddsCreateBackup          |
   +--------------------------------------+----------------+--------------------------+
   | Deleting a backup                    | backup         | ddsDeleteBackup          |
   +--------------------------------------+----------------+--------------------------+
   | Setting a backup policy              | backup         | ddsSetBackupPolicy       |
   +--------------------------------------+----------------+--------------------------+
   | Applying a parameter group           | parameterGroup | ddsApplyConfigurations   |
   +--------------------------------------+----------------+--------------------------+
   | Replicating a parameter group        | parameterGroup | ddsCopyConfigurations    |
   +--------------------------------------+----------------+--------------------------+
   | Resetting a parameter group          | parameterGroup | ddsResetConfigurations   |
   +--------------------------------------+----------------+--------------------------+
   | Creating a parameter group           | parameterGroup | ddsCreateConfigurations  |
   +--------------------------------------+----------------+--------------------------+
   | Deleting a parameter group           | parameterGroup | ddsDeleteConfigurations  |
   +--------------------------------------+----------------+--------------------------+
   | Updating a parameter group           | parameterGroup | ddsUpdateConfigurations  |
   +--------------------------------------+----------------+--------------------------+
   | Binding an EIP                       | instance       | ddsBindEIP               |
   +--------------------------------------+----------------+--------------------------+
   | Unbinding an EIP                     | instance       | ddsUnbindEIP             |
   +--------------------------------------+----------------+--------------------------+
   | Rolling back upon scaling-up failure | instance       | ddsDeleteExtendedDdsNode |
   +--------------------------------------+----------------+--------------------------+
   | Changing DB instance classes         | instance       | ddsResizeInstance        |
   +--------------------------------------+----------------+--------------------------+
