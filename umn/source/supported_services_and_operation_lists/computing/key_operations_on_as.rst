:original_name: en-us_topic_0100236049.html

.. _en-us_topic_0100236049:

Key Operations on AS
====================

Auto Scaling (AS) is a service that automatically adjusts computing resources based on your requirements and configured AS policies to ensure proper service running.

With CTS, you can record operations associated with AS for future query, audit, and backtrack operations.

.. table:: **Table 1** AS operations that can be recorded by CTS

   +-------------------------------------------+-----------------------+---------------------------------+
   | Operation                                 | Resource Type         | Trace Name                      |
   +===========================================+=======================+=================================+
   | Creating an AS group                      | scaling_group         | createScalingGroup              |
   +-------------------------------------------+-----------------------+---------------------------------+
   | Modifying an AS group                     | scaling_group         | modifyScalingGroup              |
   +-------------------------------------------+-----------------------+---------------------------------+
   | Deleting an AS group                      | scaling_group         | deleteScalingGroup              |
   +-------------------------------------------+-----------------------+---------------------------------+
   | Enabling an AS group                      | scaling_group         | enableScalingGroup              |
   +-------------------------------------------+-----------------------+---------------------------------+
   | Disabling an AS group                     | scaling_group         | disableScalingGroup             |
   +-------------------------------------------+-----------------------+---------------------------------+
   | Creating an AS configuration              | scaling_configuration | createScalingConfiguration      |
   +-------------------------------------------+-----------------------+---------------------------------+
   | Deleting an AS configuration              | scaling_configuration | deleteScalingConfiguration      |
   +-------------------------------------------+-----------------------+---------------------------------+
   | Batch deleting AS configurations          | scaling_configuration | batchDeleteScalingConfiguration |
   +-------------------------------------------+-----------------------+---------------------------------+
   | Creating an AS policy                     | scaling_policy        | createScalingPolicy             |
   +-------------------------------------------+-----------------------+---------------------------------+
   | Modifying an AS policy                    | scaling_policy        | modifyScalingPolicy             |
   +-------------------------------------------+-----------------------+---------------------------------+
   | Deleting an AS policy                     | scaling_policy        | deleteScalingPolicy             |
   +-------------------------------------------+-----------------------+---------------------------------+
   | Enabling an AS policy                     | scaling_policy        | enableScalingPolicy             |
   +-------------------------------------------+-----------------------+---------------------------------+
   | Disabling an AS policy                    | scaling_policy        | disableScalingPolicy            |
   +-------------------------------------------+-----------------------+---------------------------------+
   | Executing an AS policy                    | scaling_policy        | executeScalingPolicy            |
   +-------------------------------------------+-----------------------+---------------------------------+
   | Removing an instance                      | scaling_instance      | removeInstance                  |
   +-------------------------------------------+-----------------------+---------------------------------+
   | Batch removing instances from an AS group | scaling_instance      | batchRemoveInstances            |
   +-------------------------------------------+-----------------------+---------------------------------+
   | Batch adding instances to an AS group     | scaling_instance      | batchAddInstances               |
   +-------------------------------------------+-----------------------+---------------------------------+
   | Batch enabling instance protection        | scaling_instance      | batchProtectInstances           |
   +-------------------------------------------+-----------------------+---------------------------------+
   | Batch disabling instance protection       | scaling_instance      | batchUnprotectInstances         |
   +-------------------------------------------+-----------------------+---------------------------------+
