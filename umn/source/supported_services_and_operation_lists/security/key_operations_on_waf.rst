:original_name: en-us_topic_0100291690.html

.. _en-us_topic_0100291690:

Key Operations on WAF
=====================

Web Application Firewall (WAF) is designed to keep web services stable and secure in combination with years of experience in security protection. It examines all HTTP and HTTPS requests to detect and block attacks such as Structure Query Language (SQL) injections, cross-site scripting (XSS), webshell upload, third-party vulnerability exploits, CC attacks, and malicious crawlers.

With CTS, you can record operations associated with WAF for future query, audit, and backtrack operations.

.. table:: **Table 1** WAF operations recorded by CTS

   +---------------------------------------------------+-------------------+-------------------------+
   | Operation                                         | Resource Type     | Trace Name              |
   +===================================================+===================+=========================+
   | Creating a WAF instance                           | instance          | createInstance          |
   +---------------------------------------------------+-------------------+-------------------------+
   | Deleting a WAF instance                           | instance          | deleteInstance          |
   +---------------------------------------------------+-------------------+-------------------------+
   | Modifying a WAF instance                          | instance          | modifyInstance          |
   +---------------------------------------------------+-------------------+-------------------------+
   | Modifying the protection status of a WAF instance | instance          | modifyProtectStatus     |
   +---------------------------------------------------+-------------------+-------------------------+
   | Modifying the connection status of a WAF instance | instance          | modifyAccessStatus      |
   +---------------------------------------------------+-------------------+-------------------------+
   | Creating a policy                                 | policy            | createPolicy            |
   +---------------------------------------------------+-------------------+-------------------------+
   | Applying a policy                                 | policy            | applyToPolicy           |
   +---------------------------------------------------+-------------------+-------------------------+
   | Modifying a policy                                | policy            | modifyPolicy            |
   +---------------------------------------------------+-------------------+-------------------------+
   | Deleting a policy                                 | policy            | deletePolicy            |
   +---------------------------------------------------+-------------------+-------------------------+
   | Modifying alarm notification settings             | alertNoticeConfig | modifyAlertNoticeConfig |
   +---------------------------------------------------+-------------------+-------------------------+
   | Creating a certificate                            | certificate       | createCertificate       |
   +---------------------------------------------------+-------------------+-------------------------+
   | Changing the name of a certificate                | certificate       | modifyCertificate       |
   +---------------------------------------------------+-------------------+-------------------------+
   | Deleting a certificate                            | certificate       | deleteCertificate       |
   +---------------------------------------------------+-------------------+-------------------------+
   | Creating a CC attack protection rule              | policy            | createCc                |
   +---------------------------------------------------+-------------------+-------------------------+
   | Modifying a CC attack protection rule             | policy            | modifyCc                |
   +---------------------------------------------------+-------------------+-------------------------+
   | Deleting a CC attack protection rule              | policy            | deleteCc                |
   +---------------------------------------------------+-------------------+-------------------------+
   | Creating a precise protection rule                | policy            | createCustom            |
   +---------------------------------------------------+-------------------+-------------------------+
   | Modifying a precise protection rule               | policy            | modifyCustom            |
   +---------------------------------------------------+-------------------+-------------------------+
   | Deleting a precise protection rule                | policy            | deleteCustom            |
   +---------------------------------------------------+-------------------+-------------------------+
   | Adding a blacklist or whitelist rule              | policy            | createWhiteblackip      |
   +---------------------------------------------------+-------------------+-------------------------+
   | Modifying a blacklist or whitelist rule           | policy            | modifyWhiteblackip      |
   +---------------------------------------------------+-------------------+-------------------------+
   | Deleting a blacklist or whitelist rule            | policy            | deleteWhiteblackip      |
   +---------------------------------------------------+-------------------+-------------------------+
   | Adding a web tamper protection rule               | policy            | createAntitamper        |
   +---------------------------------------------------+-------------------+-------------------------+
   | Updating a web tamper protection rule             | policy            | refreshAntitamper       |
   +---------------------------------------------------+-------------------+-------------------------+
   | Deleting a web tamper protection rule             | policy            | deleteAntitamper        |
   +---------------------------------------------------+-------------------+-------------------------+
   | Adding a false alarm masking rule                 | policy            | createIgnore            |
   +---------------------------------------------------+-------------------+-------------------------+
   | Deleting a false alarm masking rule               | policy            | deleteIgnore            |
   +---------------------------------------------------+-------------------+-------------------------+
   | Creating a data masking rule                      | policy            | createPrivacy           |
   +---------------------------------------------------+-------------------+-------------------------+
   | Modifying a data masking rule                     | policy            | modifyPrivacy           |
   +---------------------------------------------------+-------------------+-------------------------+
   | Deleting a data masking rule                      | policy            | deletePrivacy           |
   +---------------------------------------------------+-------------------+-------------------------+
