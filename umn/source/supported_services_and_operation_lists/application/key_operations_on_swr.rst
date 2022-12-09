:original_name: cts_0827.html

.. _cts_0827:

Key Operations on SWR
=====================

Software Repository for Container (SWR) provides easy, secure, and reliable management of container images throughout their lifecycles, facilitating quick deployment of containerized services.

With CTS, you can record operations associated with SWR for future query, audit, and backtrack operations.

.. table:: **Table 1** SWR operations that can be recorded by CTS

   +-----------------------------------------------+--------------------+--------------------------+
   | Operation                                     | Resource Type      | Trace Name               |
   +===============================================+====================+==========================+
   | Creating an image repository                  | imagerepository    | createImageRepository    |
   +-----------------------------------------------+--------------------+--------------------------+
   | Modifying an image repository                 | imagerepository    | updateImageRepository    |
   +-----------------------------------------------+--------------------+--------------------------+
   | Deleting an image repository                  | imagerepository    | deleteImageRepository    |
   +-----------------------------------------------+--------------------+--------------------------+
   | Uploading an image package                    | image              | uploadImagePackage       |
   +-----------------------------------------------+--------------------+--------------------------+
   | Deleting an image tag                         | imagetag           | deleteImageTag           |
   +-----------------------------------------------+--------------------+--------------------------+
   | Granting permissions for an image repository  | userrepositoryauth | createUserRepositoryAuth |
   +-----------------------------------------------+--------------------+--------------------------+
   | Modifying permissions for an image repository | userrepositoryauth | updateUserRepositoryAuth |
   +-----------------------------------------------+--------------------+--------------------------+
   | Deleting permissions for an image repository  | userrepositoryauth | deleteUserRepositoryAuth |
   +-----------------------------------------------+--------------------+--------------------------+
   | Creating an organization                      | usernamespace      | createUserNamespace      |
   +-----------------------------------------------+--------------------+--------------------------+
   | Deleting an organization                      | usernamespace      | deleteUserNamesapce      |
   +-----------------------------------------------+--------------------+--------------------------+
   | Granting permissions for an organization      | usernamespaceauth  | createUserNamespaceAuth  |
   +-----------------------------------------------+--------------------+--------------------------+
   | Modifying permissions for an organization     | usernamespaceauth  | updateUserNamespaceAuth  |
   +-----------------------------------------------+--------------------+--------------------------+
   | Deleting permissions for an organization      | usernamespaceauth  | deleteUserNamespaceAuth  |
   +-----------------------------------------------+--------------------+--------------------------+
   | Generating login command                      | dockerlogincmd     | createDockerConfig       |
   +-----------------------------------------------+--------------------+--------------------------+
