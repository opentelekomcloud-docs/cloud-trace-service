:original_name: en-us_topic_0100291686.html

.. _en-us_topic_0100291686:

Key Operations on Anti-DDoS
===========================

Anti-DDoS is a network security service that defends IP addresses against distributed denial of service (DDoS) attacks.

Anti-DDoS monitors traffic directed to specified IP addresses in real time and detects access traffic at network egresses to discover DDoS attacks as soon as possible. It then cleans abnormal traffic according to user-configured defense policies so that services run as normal. It also generates reports to present users with a clear evaluation of network security.

With CTS, you can record operations associated with Anti-DDoS for future query, audit, and backtrack operations.

.. table:: **Table 1** Anti-DDoS operations that can be recorded by CTS

   =================== ============= ==============
   Operation           Resource Type Trace Name
   =================== ============= ==============
   Enabling Anti-DDoS  anti-ddos     openAntiddos
   Disabling Anti-DDoS anti-ddos     deleteAntiddos
   Updating Anti-DDoS  anti-ddos     updateAntiddos
   =================== ============= ==============
