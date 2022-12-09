:original_name: en-us_topic_0128329663.html

.. _en-us_topic_0128329663:

Key Operations on CDN
=====================

Content Delivery Network (CDN) is an intelligent virtual network layer based on the existing Internet infrastructure. It delivers network content from origin servers to edge node servers distributed across a country, enabling end users to obtain desired content from the proximal node.

With CTS, you can record operations associated with CDN for future query, audit, and backtrack operations.

.. table:: **Table 1** CDN operations that can be recorded by CTS

   +-----------------------------------------------------+---------------+----------------------+
   | Operation                                           | Resource Type | Trace Name           |
   +=====================================================+===============+======================+
   | Creating an acceleration domain name                | CDN           | createDomain         |
   +-----------------------------------------------------+---------------+----------------------+
   | Updating an acceleration domain name                | CDN           | updateDomain         |
   +-----------------------------------------------------+---------------+----------------------+
   | Deleting an acceleration domain name                | CDN           | deleteDomain         |
   +-----------------------------------------------------+---------------+----------------------+
   | Enabling an acceleration domain name                | CDN           | enableDomain         |
   +-----------------------------------------------------+---------------+----------------------+
   | Disabling an acceleration domain name               | CDN           | disableDomain        |
   +-----------------------------------------------------+---------------+----------------------+
   | Configuring a retrieval host                        | CDN           | updateOriginHost     |
   +-----------------------------------------------------+---------------+----------------------+
   | Creating a Referer rule                             | CDN           | createRefer          |
   +-----------------------------------------------------+---------------+----------------------+
   | Configuring an acceleration domain name certificate | CDN           | createCertificate    |
   +-----------------------------------------------------+---------------+----------------------+
   | Creating a cache rule                               | CDN           | createCacheRule      |
   +-----------------------------------------------------+---------------+----------------------+
   | Creating a cache refreshing task                    | CDN           | createRefreshTask    |
   +-----------------------------------------------------+---------------+----------------------+
   | Creating a preheating task                          | CDN           | createPreheatingTask |
   +-----------------------------------------------------+---------------+----------------------+
   | Enabling CDN                                        | CDN           | createBillingMode    |
   +-----------------------------------------------------+---------------+----------------------+
