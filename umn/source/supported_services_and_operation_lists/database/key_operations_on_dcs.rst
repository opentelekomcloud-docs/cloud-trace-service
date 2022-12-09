:original_name: en-us_topic_0100363624.html

.. _en-us_topic_0100363624:

Key Operations on DCS
=====================

Distributed Cache Service (DCS) is an online distributed database service that is based on the cloud computing platform, available immediately after it is enabled, stable and reliable, scalable online, and easy to manage.

With CTS, you can record operations associated with DCS for future query, audit, and backtrack operations.

.. table:: **Table 1** DCS operations that can be recorded by CTS

   +--------------------------------------------------------+---------------+--------------------------------------+
   | Operation                                              | Resource Type | Trace Name                           |
   +========================================================+===============+======================================+
   | Creating an instance                                   | Redis         | createDCSInstance                    |
   +--------------------------------------------------------+---------------+--------------------------------------+
   | Submitting an instance creation request                | Redis         | submitCreateDCSInstanceRequest       |
   +--------------------------------------------------------+---------------+--------------------------------------+
   | Batch deleting instances                               | Redis         | batchDeleteDCSInstance               |
   +--------------------------------------------------------+---------------+--------------------------------------+
   | Deleting an instance                                   | Redis         | deleteDCSInstance                    |
   +--------------------------------------------------------+---------------+--------------------------------------+
   | Modifying the information about a DCS instance         | Redis         | modifyDCSInstanceInfo                |
   +--------------------------------------------------------+---------------+--------------------------------------+
   | Modifying the configurations of a DCS instance         | Redis         | modifyDCSInstanceConfig              |
   +--------------------------------------------------------+---------------+--------------------------------------+
   | Changing the password of a DCS instance                | Redis         | modifyDCSInstancePassword            |
   +--------------------------------------------------------+---------------+--------------------------------------+
   | Restarting an instance                                 | Redis         | restartDCSInstance                   |
   +--------------------------------------------------------+---------------+--------------------------------------+
   | Submitting an instance restarting request              | Redis         | submitRestartDCSInstanceRequest      |
   +--------------------------------------------------------+---------------+--------------------------------------+
   | Starting an instance                                   | Redis         | startDCSInstance                     |
   +--------------------------------------------------------+---------------+--------------------------------------+
   | Submitting an instance starting request                | Redis         | submitStartDCSInstanceRequest        |
   +--------------------------------------------------------+---------------+--------------------------------------+
   | Clearing instance data                                 | Redis         | flushDCSInstance                     |
   +--------------------------------------------------------+---------------+--------------------------------------+
   | Restarting instances in batches                        | Redis         | batchRestartDCSInstance              |
   +--------------------------------------------------------+---------------+--------------------------------------+
   | Submitting a request to restart instances in batches   | Redis         | submitBatchRestartDCSInstanceRequest |
   +--------------------------------------------------------+---------------+--------------------------------------+
   | Starting instances in batches                          | Redis         | batchStartDCSInstance                |
   +--------------------------------------------------------+---------------+--------------------------------------+
   | Submitting a request to start instances in batches     | Redis         | submitBatchStartDCSInstanceRequest   |
   +--------------------------------------------------------+---------------+--------------------------------------+
   | Restoring instance data                                | Redis         | restoreDCSInstance                   |
   +--------------------------------------------------------+---------------+--------------------------------------+
   | Submitting a request to restore instance data          | Redis         | submitRestoreDCSInstanceRequest      |
   +--------------------------------------------------------+---------------+--------------------------------------+
   | Backing up instance data                               | Redis         | backupDCSInstance                    |
   +--------------------------------------------------------+---------------+--------------------------------------+
   | Submitting a request to back up instance data          | Redis         | submitBackupDCSInstanceRequest       |
   +--------------------------------------------------------+---------------+--------------------------------------+
   | Deleting instance backup files                         | Redis         | deleteInstanceBackupFile             |
   +--------------------------------------------------------+---------------+--------------------------------------+
   | Deleting background tasks                              | Redis         | deleteDCSInstanceJobRecord           |
   +--------------------------------------------------------+---------------+--------------------------------------+
   | Modifying instance specifications                      | Redis         | modifySpecification                  |
   +--------------------------------------------------------+---------------+--------------------------------------+
   | Submitting a request to modify instance specifications | Redis         | submitModifySpecificationRequest     |
   +--------------------------------------------------------+---------------+--------------------------------------+
   | Creating an instance subscription order                | Redis         | createInstanceOrder                  |
   +--------------------------------------------------------+---------------+--------------------------------------+
   | Switching between master and standby nodes             | Redis         | masterStandbySwitchover              |
   +--------------------------------------------------------+---------------+--------------------------------------+
   | Resetting an instance password                         | Redis         | resetDCSInstancePassword             |
   +--------------------------------------------------------+---------------+--------------------------------------+
   | Submitting a request to clear instance data            | Redis         | submitFlushDCSInstanceRequest        |
   +--------------------------------------------------------+---------------+--------------------------------------+
