:original_name: en-us_topic_0100291678.html

.. _en-us_topic_0100291678:

Key Operations on SMN
=====================

Simple Message Notification (SMN) is a type of web service that a user can easily construct and maintain. SMN sends notifications from a cloud.

With CTS, you can record operations associated with SMN for future query, audit, and backtrack operations.

.. note::

   In SMN, deleting a topic will delete all subscription information associated with the topic, and the subscription information deletion operation will not be recorded by CTS.

.. table:: **Table 1** SMN operations that can be recorded by CTS

   +---------------------------------------+------------------+----------------------------+
   | Operation                             | Resource Type    | Trace Name                 |
   +=======================================+==================+============================+
   | Creating a topic                      | topic            | createTopic                |
   +---------------------------------------+------------------+----------------------------+
   | Deleting a topic                      | topic            | deleteTopic                |
   +---------------------------------------+------------------+----------------------------+
   | Updating a topic                      | topic            | updateTopic                |
   +---------------------------------------+------------------+----------------------------+
   | Updating attributes of a topic        | topic            | updateTopicAttribute       |
   +---------------------------------------+------------------+----------------------------+
   | Deleting all topic attributes         | topic            | deleteTopicAttributes      |
   +---------------------------------------+------------------+----------------------------+
   | Deleting a specified topic attribute  | topic            | deleteTopicAttributeByName |
   +---------------------------------------+------------------+----------------------------+
   | Adding a subscription                 | subscription     | subscribe                  |
   +---------------------------------------+------------------+----------------------------+
   | Deleting a subscription               | subscription     | unsubscribe                |
   +---------------------------------------+------------------+----------------------------+
   | Creating a message template           | message_template | createMessageTemplate      |
   +---------------------------------------+------------------+----------------------------+
   | Creating message templates in batches | message_template | batchCreateMessageTemplate |
   +---------------------------------------+------------------+----------------------------+
   | Modifying a message template          | message_template | updateMessageTemplate      |
   +---------------------------------------+------------------+----------------------------+
   | Deleting a message template           | message_template | deleteMessageTemplate      |
   +---------------------------------------+------------------+----------------------------+
