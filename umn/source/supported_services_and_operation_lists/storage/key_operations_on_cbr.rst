:original_name: en-us_topic_0000001317721642.html

.. _en-us_topic_0000001317721642:

Key Operations on CBR
=====================

Cloud Backup and Recovery (CBR) backup for Elastic Volume Service (EVS), Elastic Cloud Server (ECS), and Bare Metal Server (BMS), ensuring data security and correctness as well as service security.

With CTS, you can record operations associated with CBR for later query, audit, and backtracking.

.. table:: **Table 1** CBR operations that can be recorded by CTS

   ============================== ============= =================
   Operation                      Resource Type Trace Name
   ============================== ============= =================
   Creating a policy              policy        createPolicy
   Updating a policy              policy        updatePolicy
   Deleting a policy              policy        deletePolicy
   Setting a vault policy         vault         associatePolicy
   Removing a policy from a vault vault         dissociatePolicy
   Creating a vault               vault         createVault
   Modifying a vault              vault         updateVault
   Deleting a vault               vault         deleteVault
   Removing resources             vault         removeResources
   Adding resources               vault         addResources
   Performing a backup            vault         createVaultBackup
   Creating a backup              backup        createBackup
   Deleting a backup              backup        deleteBackup
   Restoring a backup             backup        restoreBackup
   ============================== ============= =================
