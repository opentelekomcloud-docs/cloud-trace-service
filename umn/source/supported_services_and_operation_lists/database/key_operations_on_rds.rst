:original_name: en-us_topic_0100363625.html

.. _en-us_topic_0100363625:

Key Operations on RDS
=====================

Relational Database Service (RDS) is a cloud-based web service that is reliable, scalable, easy to manage, and immediately ready for use.

With CTS, you can record operations associated with RDS for future query, audit, and backtrack operations.

.. table:: **Table 1** RDS operations recorded by CTS

   +----------------------------------------------------------------------------------+----------------+--------------------------+
   | Operation                                                                        | Resource Type  | Trace Name               |
   +==================================================================================+================+==========================+
   | Creating a DB instance or a read replica, or restoring data to a new DB instance | instance       | createInstance           |
   +----------------------------------------------------------------------------------+----------------+--------------------------+
   | Scaling up storage space and changing instance class                             | instance       | instanceAction           |
   +----------------------------------------------------------------------------------+----------------+--------------------------+
   | Rebooting a DB instance                                                          | instance       | instanceRestart          |
   +----------------------------------------------------------------------------------+----------------+--------------------------+
   | Restoring data to the original DB instance                                       | instance       | instanceRestore          |
   +----------------------------------------------------------------------------------+----------------+--------------------------+
   | Renaming a DB instance                                                           | instance       | instanceRename           |
   +----------------------------------------------------------------------------------+----------------+--------------------------+
   | Resetting a password                                                             | instance       | resetPassword            |
   +----------------------------------------------------------------------------------+----------------+--------------------------+
   | Setting database version parameters                                              | instance       | setDBParameters          |
   +----------------------------------------------------------------------------------+----------------+--------------------------+
   | Resetting database version parameters                                            | instance       | resetDBParameters        |
   +----------------------------------------------------------------------------------+----------------+--------------------------+
   | Enabling, modifying, or disabling a backup policy                                | instance       | setBackupPolicy          |
   +----------------------------------------------------------------------------------+----------------+--------------------------+
   | Changing a database port                                                         | instance       | changeInstancePort       |
   +----------------------------------------------------------------------------------+----------------+--------------------------+
   | Binding or unbinding an EIP                                                      | instance       | setOrResetPublicIP       |
   +----------------------------------------------------------------------------------+----------------+--------------------------+
   | Modifying a security group                                                       | instance       | modifySecurityGroup      |
   +----------------------------------------------------------------------------------+----------------+--------------------------+
   | Deleting a DB instance                                                           | instance       | deleteInstance           |
   +----------------------------------------------------------------------------------+----------------+--------------------------+
   | Performing a primary/standby switchover                                          | instance       | instanceFailOver         |
   +----------------------------------------------------------------------------------+----------------+--------------------------+
   | Changing the replication mode                                                    | instance       | instanceFailOverMode     |
   +----------------------------------------------------------------------------------+----------------+--------------------------+
   | Changing a failover priority                                                     | instance       | instanceFailOverStrategy |
   +----------------------------------------------------------------------------------+----------------+--------------------------+
   | Changing a DB instance type from single to primary/standby                       | instance       | modifySingleToHaInstance |
   +----------------------------------------------------------------------------------+----------------+--------------------------+
   | Downloading a backup (using OBS)                                                 | backup         | downLoadSnapshot         |
   +----------------------------------------------------------------------------------+----------------+--------------------------+
   | Downloading a backup (using a browser)                                           | backup         | backupsDownLoad          |
   +----------------------------------------------------------------------------------+----------------+--------------------------+
   | Deleting a backup                                                                | backup         | deleteManualSnapshot     |
   +----------------------------------------------------------------------------------+----------------+--------------------------+
   | Downloading a merged backup                                                      | backup         | packBackupsDownLoad      |
   +----------------------------------------------------------------------------------+----------------+--------------------------+
   | Creating a parameter template                                                    | parameterGroup | createParameterGroup     |
   +----------------------------------------------------------------------------------+----------------+--------------------------+
   | Modifying parameters in a parameter template                                     | parameterGroup | updateParameterGroup     |
   +----------------------------------------------------------------------------------+----------------+--------------------------+
   | Deleting a parameter template                                                    | parameterGroup | deleteParameterGroup     |
   +----------------------------------------------------------------------------------+----------------+--------------------------+
   | Replicating a parameter template                                                 | parameterGroup | copyParameterGroup       |
   +----------------------------------------------------------------------------------+----------------+--------------------------+
   | Resetting a parameter template                                                   | parameterGroup | resetParameterGroup      |
   +----------------------------------------------------------------------------------+----------------+--------------------------+
   | Applying a parameter template                                                    | parameterGroup | applyParameterGroup      |
   +----------------------------------------------------------------------------------+----------------+--------------------------+
   | Saving parameters in a parameter template                                        | parameterGroup | saveParameterGroup       |
   +----------------------------------------------------------------------------------+----------------+--------------------------+
