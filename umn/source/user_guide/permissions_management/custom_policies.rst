:original_name: cts_031_003.html

.. _cts_031_003:

Custom Policies
===============

Custom policies can be created to supplement the system-defined policies of CTS. For the actions supported for custom policies, see "Permissions Policies and Supported Actions" in the *API Reference*.

You can create custom policies in either of the following ways:

-  Visual editor: Select cloud services, actions, resources, and request conditions. You do not need to have knowledge of the policy syntax.
-  JSON: Edit policies from scratch or based on an existing policy in JSON format.

For details about how to create custom policies, see `Creating a Custom Policy <https://docs.otc.t-systems.com/usermanual/iam/en-us_topic_0274187246.html>`__. The following section contains examples of common CTS custom policies.

Example Custom Policies
-----------------------

-  Example 1: Authorize a user to view the event list.

   .. code-block::

      {
          "Version": "1.1",
          "Statement": [
              {
                  "Effect": "Allow",
                  "Action": [
                      "cts:trace:list"
                  ]
              }
          ]
      }

-  Example 2: Deny modification and delete the tracker.

   A policy with only "Deny" permissions must be used in conjunction with other policies. If the permissions assigned to a user contain both "Allow" and "Deny", the "Deny" permissions take precedence over the "Allow" permissions.

   The following method can be used if you need to assign permissions of the **CTS FullAccess** policy to a user but also forbid the user from modifying or deleting trackers. Create a custom policy to disallow tracker deletion or modifying and assign both policies to the group the user belongs to. Then the user can perform all operations on CTS except deleting or modifying trackers. The following is an example of a deny policy:

   .. code-block::

      {
          "Version": "1.1",
          "Statement": [
              {
                  "Effect": "Deny",
                  "Action": [
                      "cts:tracker:delete",
                      "cts:tracker:update"
                  ]
              }
          ]
      }

-  Example 3: Define actions for multiple services in a policy

   A custom policy can contain the actions of multiple services that are of the same type: global or project-level. The following is a policy with multiple statements:

   .. code-block::

      {{
          "Version": "1.1",
          "Statement": [
              {
                  "Effect": "Allow",
                  "Action": [
                      "cts:tracker:list",
                      "cts:trace:list",
                      "lts:groups:get",
                      "lts:logs:list",
                      "lts:logstreams:list"
                  ]
              }
          ]
      }
