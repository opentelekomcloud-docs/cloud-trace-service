:original_name: en-us_topic_0100273727.html

.. _en-us_topic_0100273727:

Key Operations on ELB
=====================

Elastic Load Balancing (ELB) is a service that automatically distributes access traffic to multiple ECSs to balance their service load. ELB enables you to achieve higher levels of fault tolerance in your applications and expand application service capabilities.

With a web-based console, you can create load balancers, configure the ports required for listening, and add backend ECSs for load balancers. ELB helps eliminate single points of failure (SPOFs), improving availability of the whole system.

With CTS, you can record operations associated with ELB for future query, audit, and backtrack operations.

.. table:: **Table 1** ELB operations that can be recorded by CTS

   =============================== ============= ===================
   Operation                       Resource Type Trace Name
   =============================== ============= ===================
   Creating a certificate          certificate   createCertificate
   Updating a certificate          certificate   updateCertificate
   Deleting a certificate          certificate   deleteCertificate
   Creating a health check         healthmonitor createHealthMonitor
   Updating a health check         healthmonitor updateHealthMonitor
   Deleting a health check         healthmonitor deleteHealthMonitor
   Creating a forwarding policy    l7policy      createL7policy
   Updating a forwarding policy    l7policy      updateL7policy
   Deleting a forwarding policy    l7policy      deleteL7policy
   Creating a forwarding rule      l7rule        createl7rule
   Updating a forwarding rule      l7rule        updateL7rule
   Deleting a forwarding rule      l7rule        deleteL7rule
   Creating a listener             listener      createListener
   Updating a listener             listener      updateListener
   Deleting a listener             listener      deleteListener
   Creating a load balancer        loadbalancer  createLoadbalancer
   Updating a load balancer        loadbalancer  updateLoadbalancer
   Deleting a load balancer        loadbalancer  deleteLoadbalancer
   Adding a backend ECS            member        createMember
   Updating a backend ECS          member        updateMember
   Removing a backend ECS          member        batchUpdateMember
   Creating a backend server group pool          createPool
   Updating a backend server group pool          updatPool
   Deleting a backend server group pool          deletePool
   =============================== ============= ===================
