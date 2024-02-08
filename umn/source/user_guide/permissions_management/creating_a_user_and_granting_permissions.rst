:original_name: cts_031_002.html

.. _cts_031_002:

Creating a User and Granting Permissions
========================================

For fine-grained management of CTS permissions, you can use `Identity and Access Management (IAM) <https://docs.otc.t-systems.com/usermanual/iam/iam_01_0026.html>`__. With IAM, you can:

-  Create IAM users for employees based on your enterprise's organizational structure. Each IAM user will have their own security credentials for accessing CTS resources.
-  Manage permissions on a principle of least permissions (PoLP) basis.
-  Entrust an account or cloud service to perform efficient O&M on your CTS resources.

If your account does not require individual IAM users, skip this section.

Prerequisites
-------------

Learn about the permissions (see `Permissions <https://docs.otc.t-systems.com/permissions/index.html>`__) supported by CTS and choose policies or roles according to your requirements.

Process Flow
------------


.. figure:: /_static/images/en-us_image_0000001525454037.png
   :alt: **Figure 1** Process of granting CTS permissions

   **Figure 1** Process of granting CTS permissions

#. .. _cts_031_002__en-us_topic_0207902851_li10961848173315:

   `Create a user group and assign permissions <https://docs.otc.t-systems.com/usermanual/iam/iam_01_0030.html>`__.

   Create a user group on the IAM console, and attach the **CTS Administrator** policy to the group.

#. `Create a user and add the user to the user group <https://docs.otc.t-systems.com/usermanual/iam/iam_01_0031.html>`__.

   Create a user on the IAM console and add the user to the user group created in :ref:`1 <cts_031_002__en-us_topic_0207902851_li10961848173315>`.

#. `Log in as the created user <https://docs.otc.t-systems.com/usermanual/iam/iam_01_0032.html>`__ and verify permissions.

   Log in to the console by using the created user and verify permissions in the authorized region.
