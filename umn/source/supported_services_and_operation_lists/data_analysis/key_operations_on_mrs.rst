:original_name: en-us_topic_0100363631.html

.. _en-us_topic_0100363631:

Key Operations on MRS
=====================

MapReduce Service (MRS) is a data processing and analysis service that is based on a cloud computing platform. It is stable, reliable, scalable, and easy to manage.

With CTS, you can record operations associated with MRS for future query, audit, and backtrack operations.

.. table:: **Table 1** MRS operations that can be recorded by CTS

   =================== ============= ===============
   Operation           Resource Type Trace Name
   =================== ============= ===============
   Creating a cluster  cluster_mrs   createCluster
   Deleting a cluster  cluster_mrs   deleteCluster
   Expanding a cluster cluster_mrs   scaleOutCluster
   Shrinking a cluster cluster_mrs   scaleInCluster
   =================== ============= ===============
