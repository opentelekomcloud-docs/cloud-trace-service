:original_name: cts_03_0136.html

.. _cts_03_0136:

Permissions Management
======================

This chapter describes how to use IAM for fine-grained permissions control for your CTS resources. With IAM, you can:

-  Create IAM users for employees based on your enterprise's organizational structure. Each IAM user will have their own security credentials for accessing CTS resources.
-  Manage permissions on a principle of least permissions (PoLP) basis.
-  Entrust other accounts or cloud services to perform efficient O&M on your CTS resources.

If your account does not need IAM users, you can skip this section.

Prerequisites
-------------

Learn about the permissions (see :ref:`Permissions Management <cts_01_0006>`) supported by CTS and choose policies or roles according to your requirements.

Process Flow
------------


.. figure:: /_static/images/en-us_image_0000002344556328.png
   :alt: **Figure 1** Process of granting CTS permissions

   **Figure 1** Process of granting CTS permissions

#. .. _cts_03_0136__en-us_topic_0207902851_li10961848173315:

   Create a user group and assign permissions.

   Create a user group on the IAM console, and attach the **CTS Administrator** policy to the group.

#. Create an IAM user.

   Create a user on the IAM console and add the user to the user group created in :ref:`1 <cts_03_0136__en-us_topic_0207902851_li10961848173315>`.

#. Log in and verify permissions.

   Log in to the console as the user you created, and verify that the user has the assigned permissions.
