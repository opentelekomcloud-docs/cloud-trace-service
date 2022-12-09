:original_name: en-us_topic_0100291677.html

.. _en-us_topic_0100291677:

Key Operations on TMS
=====================

Tag Management Service (TMS) is a visualized service for fast, unified tag management that enables you to control your resource permissions and billing more efficiently. It allows you to tag and categorize cloud services across regions, and it can be accessed through the TMS console or using APIs.

With CTS, you can record operations associated with TMS for future query, audit, and backtrack operations.

.. table:: **Table 1** TMS operations that can be recorded by CTS

   ========================== ============= ==================
   Operation                  Resource Type Trace Name
   ========================== ============= ==================
   Adding a predefined tag    predefineTag  addPredefineTag
   Deleting a predefined tag  predefineTag  deletePredefineTag
   Modifying a predefined tag predefineTag  modifyPredefineTag
   Creating a resource tag    application   createResourceTag
   Deleting a resource tag    application   deleteResourceTag
   ========================== ============= ==================
