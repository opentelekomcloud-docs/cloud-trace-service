:original_name: en-us_topic_0100236046.html

.. _en-us_topic_0100236046:

Key Operations on ECS
=====================

An ECS is a computing server that consists of CPUs, memory, images, and EVS disks and allows on-demand allocation and elastic scaling. ECS integrates VPC, virtual firewall, and multi-data-copy capabilities to build an efficient, reliable, and secure computing environment to ensure stable and continuous running of your services.

With CTS, you can record operations associated with ECS for future query, audit, and backtrack operations.

.. table:: **Table 1** ECS operations that can be recorded by CTS

   +-------------------------------------------------+---------------+---------------------+
   | Operation                                       | Resource Type | Trace Name          |
   +=================================================+===============+=====================+
   | Starting an ECS                                 | ecs           | startServer         |
   +-------------------------------------------------+---------------+---------------------+
   | Restarting an ECS                               | ecs           | rebootServer        |
   +-------------------------------------------------+---------------+---------------------+
   | Stopping an ECS                                 | ecs           | stopServer          |
   +-------------------------------------------------+---------------+---------------------+
   | Attaching a disk to an ECS (on the EVS console) | ecs           | attachVolume2       |
   +-------------------------------------------------+---------------+---------------------+
   | Reinstalling the OS                             | ecs           | reinstallOs         |
   +-------------------------------------------------+---------------+---------------------+
   | Changing the OS                                 | ecs           | changeOs            |
   +-------------------------------------------------+---------------+---------------------+
   | Modifying ECS specifications                    | ecs           | resizeServer        |
   +-------------------------------------------------+---------------+---------------------+
   | Adding an automatic recovery tag to a VM        | ecs           | addAutoRecovery     |
   +-------------------------------------------------+---------------+---------------------+
   | Deleting an automatic recovery tag from a VM    | ecs           | deleteAutoRecovery  |
   +-------------------------------------------------+---------------+---------------------+
   | Creating a security group                       | ecs           | createSecurityGroup |
   +-------------------------------------------------+---------------+---------------------+
