:original_name: en-us_topic_0101676084.html

.. _en-us_topic_0101676084:

Key Operations on CSS
=====================

Cloud Search Service (CSS) is a fully hosted distributed search engine service based on the cloud infrastructure and platform. It provides structured and unstructured text search, statistics, and report capabilities.

With CTS, you can record operations associated with CSS for later query, audit, and backtracking.

.. table:: **Table 1** CSS operations that can be recorded by CTS

   +--------------------------------------------------------+---------------+--------------------------+
   | Operation                                              | Resource Type | Trace Name               |
   +========================================================+===============+==========================+
   | Creating a cluster                                     | Cluster       | createCluster            |
   +--------------------------------------------------------+---------------+--------------------------+
   | Deleting a cluster                                     | Cluster       | deleteCluster            |
   +--------------------------------------------------------+---------------+--------------------------+
   | Expanding the cluster capacity                         | Cluster       | growCluster              |
   +--------------------------------------------------------+---------------+--------------------------+
   | Restarting a cluster                                   | Cluster       | rebootCluster            |
   +--------------------------------------------------------+---------------+--------------------------+
   | Performing basic configurations for a cluster snapshot | cluster       | updateSnapshotPolicy     |
   +--------------------------------------------------------+---------------+--------------------------+
   | Setting the automatic snapshot creation policy         | cluster       | updateAutoSnapshotPolicy |
   +--------------------------------------------------------+---------------+--------------------------+
   | Creating a snapshot                                    | snapshot      | createSnapshot           |
   +--------------------------------------------------------+---------------+--------------------------+
   | Restarting a snapshot                                  | snapshot      | restoreSnapshot          |
   +--------------------------------------------------------+---------------+--------------------------+
   | Deleting a snapshot                                    | snapshot      | deleteSnapshot           |
   +--------------------------------------------------------+---------------+--------------------------+
