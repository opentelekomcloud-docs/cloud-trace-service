:original_name: en-us_topic_0100498013.html

.. _en-us_topic_0100498013:

Key Operations on DWS
=====================

Data Warehouse Service (DWS) is an online data processing database based on the cloud infrastructure and platform and helps you mine and analyze massive data.

With CTS, you can record operations associated with DWS for later query, audit, and backtracking.

.. table:: **Table 1** DWS operations that can be recorded by CTS

   ============================== ============== ====================
   Operation                      Resource Type  Trace Name
   ============================== ============== ====================
   Creating/Restoring a cluster   cluster        createCluster
   Deleting a cluster             cluster        deleteCluster
   Expanding the cluster capacity cluster        growCluster
   Restarting a cluster           cluster        rebootCluster
   Creating a snapshot            backup         createBackup
   Deleting a snapshot            backup         deleteBackup
   Setting security parameters    configurations updateConfigurations
   Creating an MRS data source    dataSource     createExtDataSource
   Deleting an MRS data source    dataSource     deleteExtDataSource
   Updating an MRS data source    dataSource     updateExtDataSource
   ============================== ============== ====================
