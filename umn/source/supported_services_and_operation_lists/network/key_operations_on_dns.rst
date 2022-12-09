:original_name: en-us_topic_0100273730.html

.. _en-us_topic_0100273730:

Key Operations on DNS
=====================

Domain Name Service (DNS) provides highly available and scalable authoritative DNS services and domain name management services. It translates domain names or application resources into IP addresses required for network connection. By doing so, visitors' access requests are directed to the desired resources.

With CTS, you can record operations associated with DNS for future query, audit, and backtrack operations.

DNS operations that can be recorded by CTS are listed in :ref:`Table 1 <en-us_topic_0100273730__table149110413017>` and :ref:`Table 2 <en-us_topic_0100273730__table155718451405>`.

.. _en-us_topic_0100273730__table149110413017:

.. table:: **Table 1** DNS operations that can be recorded by CTS (global level)

   +-------------------------------------------------+---------------------+---------------------------+
   | Operation                                       | Resource Type       | Trace Name                |
   +=================================================+=====================+===========================+
   | Creating a record set in a public zone          | publicRecordSet     | createPublicRecordSet     |
   +-------------------------------------------------+---------------------+---------------------------+
   | Deleting a record set in a public zone          | publicRecordSet     | deletePublicRecordSet     |
   +-------------------------------------------------+---------------------+---------------------------+
   | Modifying a record set in a public zone         | publicRecordSet     | updatePublicRecordSet     |
   +-------------------------------------------------+---------------------+---------------------------+
   | Creating a public zone                          | publicZone          | createPublicZone          |
   +-------------------------------------------------+---------------------+---------------------------+
   | Modifying a public zone                         | publicZone          | updatePublicZone          |
   +-------------------------------------------------+---------------------+---------------------------+
   | Deleting a public zone                          | publicZone          | deletePublicZone          |
   +-------------------------------------------------+---------------------+---------------------------+
   | Adding tags to a public zone                    | publicZoneTag       | createPublicZoneTag       |
   +-------------------------------------------------+---------------------+---------------------------+
   | Deleting tags of a public zone                  | publicZoneTag       | deletePublicZoneTag       |
   +-------------------------------------------------+---------------------+---------------------------+
   | Adding tags to a record set in a public zone    | publicRecordSetTag  | createPublicRecordSetTag  |
   +-------------------------------------------------+---------------------+---------------------------+
   | Deleting tags of a record set in a public zone  | publicRecordSetTag  | deletePublicRecordSetTag  |
   +-------------------------------------------------+---------------------+---------------------------+
   | Adding tags to a private zone                   | privateZoneTag      | createPrivateZoneTag      |
   +-------------------------------------------------+---------------------+---------------------------+
   | Deleting tags of a private zone                 | privateZoneTag      | deletePrivateZoneTag      |
   +-------------------------------------------------+---------------------+---------------------------+
   | Adding tags to a record set in a private zone   | privateRecordSetTag | createPrivateRecordSetTag |
   +-------------------------------------------------+---------------------+---------------------------+
   | Deleting tags of a record set in a private zone | privateRecordSetTag | deletePrivateRecordSetTag |
   +-------------------------------------------------+---------------------+---------------------------+
   | Adding tags to a PTR record                     | ptrRecordTag        | createPTRRecordSetTag     |
   +-------------------------------------------------+---------------------+---------------------------+
   | Deleting tags of a PTR record                   | ptrRecordTag        | deletePTRRecordTag        |
   +-------------------------------------------------+---------------------+---------------------------+

.. _en-us_topic_0100273730__table155718451405:

.. table:: **Table 2** DNS operations that can be recorded by CTS (region level)

   ============================== ================ ======================
   Operation                      Resource Type    Trace Name
   ============================== ================ ======================
   Creating a private record set  privateRecordSet createPrivateRecordSet
   Deleting a private record set  privateRecordSet deletePrivateRecordSet
   Modifying a private record set privateRecordSet updatePrivateRecordSet
   Creating a private zone        privateZone      createPrivateZone
   Modifying a private zone       privateZone      updatePrivateZone
   Deleting a private zone        privateZone      deletePrivateZone
   Associating a VPC              privateZone      associateRouter
   Disassociating a VPC           privateZone      disassociateRouter
   Configuring a PTR record       ptrRecord        setPTRRecord
   Unsetting a PTR record         ptrRecord        resetPTRRecord
   ============================== ================ ======================
