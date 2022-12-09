:original_name: en-us_cts_03_0011.html

.. _en-us_cts_03_0011:

Key Operations on GaussDB(for MySQL)
====================================

GaussDB(for MySQL) is a MySQL-compatible, enterprise-class distributed database service.

With CTS, you can record operations associated with GaussDB(for MySQL) for future query, audit, and backtracking.

.. table:: **Table 1** GaussDB(for MySQL) operations recorded by CTS

   +----------------------------------------------+----------------+-----------------------+
   | Operation                                    | Resource Type  | Trace Name            |
   +==============================================+================+=======================+
   | Creating a DB instance                       | instance       | createInstance        |
   +----------------------------------------------+----------------+-----------------------+
   | Creating a read replica                      | instance       | addNodes              |
   +----------------------------------------------+----------------+-----------------------+
   | Deleting a read replica                      | instance       | deleteNode            |
   +----------------------------------------------+----------------+-----------------------+
   | Rebooting a DB instance                      | instance       | restartInstance       |
   +----------------------------------------------+----------------+-----------------------+
   | Changing a database port                     | instance       | changeInstancePort    |
   +----------------------------------------------+----------------+-----------------------+
   | Changing a security group                    | instance       | modifySecurityGroup   |
   +----------------------------------------------+----------------+-----------------------+
   | Promoting a read replica to the primary node | instance       | instanceSwitchOver    |
   +----------------------------------------------+----------------+-----------------------+
   | Binding or unbinding an EIP                  | instance       | setOrResetPublicIP    |
   +----------------------------------------------+----------------+-----------------------+
   | Deleting a DB instance                       | instance       | deleteInstance        |
   +----------------------------------------------+----------------+-----------------------+
   | Renaming a DB instance                       | instance       | renameInstance        |
   +----------------------------------------------+----------------+-----------------------+
   | Changing a failover priority                 | instance       | modifyPriority        |
   +----------------------------------------------+----------------+-----------------------+
   | Modifying specifications                     | instance       | instanceAction        |
   +----------------------------------------------+----------------+-----------------------+
   | Resetting a password                         | instance       | resetPassword         |
   +----------------------------------------------+----------------+-----------------------+
   | Restoring data to a new DB instance          | instance       | restoreInstance       |
   +----------------------------------------------+----------------+-----------------------+
   | Creating a backup                            | backup         | createManualSnapshot  |
   +----------------------------------------------+----------------+-----------------------+
   | Deleting a backup                            | backup         | deleteManualSnapshot  |
   +----------------------------------------------+----------------+-----------------------+
   | Creating a parameter template                | parameterGroup | createParameterGroup  |
   +----------------------------------------------+----------------+-----------------------+
   | Modifying parameters in a parameter template | parameterGroup | updateParameterGroup  |
   +----------------------------------------------+----------------+-----------------------+
   | Deleting a parameter template                | parameterGroup | deleteParameterGroup  |
   +----------------------------------------------+----------------+-----------------------+
   | Replicating a parameter template             | parameterGroup | copyParameterGroup    |
   +----------------------------------------------+----------------+-----------------------+
   | Resetting a parameter template               | parameterGroup | resetParameterGroup   |
   +----------------------------------------------+----------------+-----------------------+
   | Comparing parameter templates                | parameterGroup | compareParameterGroup |
   +----------------------------------------------+----------------+-----------------------+
   | Applying a parameter template                | parameterGroup | applyParameterGroup   |
   +----------------------------------------------+----------------+-----------------------+
