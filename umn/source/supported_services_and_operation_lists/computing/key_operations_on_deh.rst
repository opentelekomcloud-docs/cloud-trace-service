:original_name: en-us_topic_0100363619.html

.. _en-us_topic_0100363619:

Key Operations on DeH
=====================

Dedicated Host (DeH) is a service that provides dedicated physical hosts. You can create ECSs on a DeH to enhance isolation, security, and performance of your ECSs. When you migrate services to a DeH, you can continue to use your server software licenses used before the migration. That is, you can use the Bring Your Own License (BYOL) feature on the DeH to reduce costs and independently manage your ECSs.

With CTS, you can record operations associated with DeH for future query, audit, and backtrack operations.

.. table:: **Table 1** DeH operations that can be recorded by CTS

   ============== ============== =====================
   Operation      Resource Type  Trace Name
   ============== ============== =====================
   Creating a DeH dedicatedHosts createDedicatedHosts
   Updating a DeH dedicatedHosts updateDedicatedHosts
   Deleting a DeH dedicatedHosts releaseDedicatedHosts
   ============== ============== =====================
