:original_name: en-us_topic_0100273719.html

.. _en-us_topic_0100273719:

Key Operations on Cloud Eye
===========================

Cloud Eye is an open monitoring platform. It provides monitoring, alarm reporting, and alarm notification for your resources in near-real time.

With CTS, you can record operations associated with Cloud Eye for future query, audit, and backtrack operations.

.. table:: **Table 1** Cloud Eye operations that can be recorded by CTS

   +------------------------------------------------+----------------+-------------------------------------+
   | Operation                                      | Resource Type  | Trace Name                          |
   +================================================+================+=====================================+
   | Creating an alarm rule                         | alarm_rule     | createAlarmRule                     |
   +------------------------------------------------+----------------+-------------------------------------+
   | Creating alarm rules in batches                | alarm_rule     | batchCreateAlarmRule                |
   +------------------------------------------------+----------------+-------------------------------------+
   | Deleting an alarm rule                         | alarm_rule     | deleteAlarmRule                     |
   +------------------------------------------------+----------------+-------------------------------------+
   | Disabling an alarm rule                        | alarm_rule     | disableAlarmRule                    |
   +------------------------------------------------+----------------+-------------------------------------+
   | Enabling an alarm rule                         | alarm_rule     | enableAlarmRule                     |
   +------------------------------------------------+----------------+-------------------------------------+
   | Modifying an alarm rule                        | alarm_rule     | updateAlarmRule                     |
   +------------------------------------------------+----------------+-------------------------------------+
   | Updating the alarm status to alarm             | alarm_rule     | alarmStatusChangeToAlarm            |
   +------------------------------------------------+----------------+-------------------------------------+
   | Updating the alarm status to insufficient data | alarm_rule     | alarmStatusChangeToInsufficientData |
   +------------------------------------------------+----------------+-------------------------------------+
   | Updating the alarm status to normal            | alarm_rule     | alarmStatusChangeToOk               |
   +------------------------------------------------+----------------+-------------------------------------+
   | Creating a custom alarm template               | alarm_template | createAlarmTemplate                 |
   +------------------------------------------------+----------------+-------------------------------------+
   | Deleting a custom alarm template               | alarm_template | deleteAlarmTemplate                 |
   +------------------------------------------------+----------------+-------------------------------------+
   | Modifying a custom alarm template              | alarm_template | updateAlarmTemplate                 |
   +------------------------------------------------+----------------+-------------------------------------+
   | Creating a monitoring panel                    | dashboard      | createDashboard                     |
   +------------------------------------------------+----------------+-------------------------------------+
   | Deleting a monitoring panel                    | dashboard      | deleteDashboard                     |
   +------------------------------------------------+----------------+-------------------------------------+
   | Modifying a monitoring panel                   | dashboard      | updateDashboard                     |
   +------------------------------------------------+----------------+-------------------------------------+
   | Adding monitoring data                         | metric         | addMetricData                       |
   +------------------------------------------------+----------------+-------------------------------------+
   | Exporting monitoring data                      | metric         | downloadMetricsReport               |
   +------------------------------------------------+----------------+-------------------------------------+
