:original_name: en-us_topic_0100236047.html

.. _en-us_topic_0100236047:

Key Operations on IMS
=====================

IMS provides easy-to-use and self-service image management. You can use a public or private image to create an ECS. You can also create a private image using an existing ECS or an external image file.

With CTS, you can record operations associated with IMS for future query, audit, and backtrack operations.

.. table:: **Table 1** IMS operations that can be recorded by CTS

   =========================== ============= ============
   Operation                   Resource Type Trace Name
   =========================== ============= ============
   Creating an image           ims           createImage
   Updating an image           ims           updateImage
   Deleting images in batches  ims           deleteImage
   Copying an image            ims           copyImage
   Exporting an image          ims           exportImage
   Adding a member             ims           addMember
   Updating members in batches ims           updateMember
   Deleting members in batches ims           deleteMember
   =========================== ============= ============
