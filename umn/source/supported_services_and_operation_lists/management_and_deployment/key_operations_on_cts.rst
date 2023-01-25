:original_name: en-us_topic_0100273718.html

.. _en-us_topic_0100273718:

Key Operations on CTS
=====================

CTS provides records of operations on cloud service resources. With CTS, you can query, audit, and backtrack these operations.

With CTS, you can record operations associated with CTS itself for future query, audit, and backtrack operations.

.. table:: **Table 1** CTS operations that can be recorded by itself

   +-------------------------------------------------+---------------+--------------------------+
   | Operation                                       | Resource Type | Trace Name               |
   +=================================================+===============+==========================+
   | Creating a tracker                              | tracker       | createTracker            |
   +-------------------------------------------------+---------------+--------------------------+
   | Modifying a tracker                             | tracker       | updateTracker            |
   +-------------------------------------------------+---------------+--------------------------+
   | Disabling a tracker                             | tracker       | updateTracker            |
   +-------------------------------------------------+---------------+--------------------------+
   | Enabling a tracker                              | tracker       | updateTracker            |
   +-------------------------------------------------+---------------+--------------------------+
   | Deleting a tracker                              | tracker       | deleteTracker            |
   +-------------------------------------------------+---------------+--------------------------+
   | Creating a key event notification               | notification  | createNotification       |
   +-------------------------------------------------+---------------+--------------------------+
   | Deleting a key event notification               | notification  | deleteNotification       |
   +-------------------------------------------------+---------------+--------------------------+
   | Modifying a key event notification              | notification  | updateNotification       |
   +-------------------------------------------------+---------------+--------------------------+
   | Changing the status of a key event notification | notification  | updateNotificationStatus |
   +-------------------------------------------------+---------------+--------------------------+
