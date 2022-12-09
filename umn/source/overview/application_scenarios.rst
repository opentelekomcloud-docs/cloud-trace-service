:original_name: en-us_topic_0043877300.html

.. _en-us_topic_0043877300:

Application Scenarios
=====================

CTS is used in the following scenarios:

-  **Compliance audit**

   CTS tracks operations and allows you to query the records. This is essential for organizations, especially financial and payment enterprises, to obtain certifications such as PCI DSS and COSO certificate.

-  **Data Value Mining**

   CTS allows you to mine data in audit logs to provide support for service health analysis, risk analysis, resource tracking, and cost analysis. In addition, you can obtain audit data from CTS and explore data value yourself.

   An audit log contains 19 fields, including time, operator, operation device IP address, operated resource, operation details, and other information. Each audit log is worth mining.

   CTS allows you to synchronize audit logs to your own system for analysis by configuring HTTP or HTTPS notifications. CTS has been interconnected with Cloud Eye and Log Tank Service (LTS) to help you track high-risk operations, analyze unauthorized operations, and check resource usage. The interconnection also provides data for analysis of service health and costs. For details on Cloud Eye, see *Cloud Eye User Guide*.

-  **Key Event Notifications**

   CTS works with FunctionGraph to send notifications to natural persons or service APIs when any key operation is performed. The following are some usage examples:

   -  CTS allows you to configure HTTP or HTTPS notifications targeted at your independent audit systems and synchronize audit logs received by CTS to these audit systems for auditing.
   -  CTS allows you to select a type of log as a trigger (such as file upload) in FunctionGraph to trigger a preset workflow (such as file format conversion). This simplifies service deployment and O&M, avoiding problems and risks.

-  **Fault Locating and Analysis**

   If a fault occurs when you use cloud services, you can use filters to quickly search for unusual operations, and send the related traces to customer service or O&M engineers to handle the issue. This accelerates troubleshooting and reduces manpower requirements.

   You can search by filters such as trace source, resource type, operator, and trace status. Each trace contains the request and response of an operation.
