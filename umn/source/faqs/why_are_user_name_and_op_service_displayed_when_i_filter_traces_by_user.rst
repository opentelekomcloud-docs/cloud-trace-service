:original_name: cts_faq_013.html

.. _cts_faq_013:

Why Are **user_name** and **op_service** Displayed When I Filter Traces by User?
================================================================================

If you submit a request that calls operations requiring high permissions or calling of other services, you may not have the required permissions. In this case, your permissions will be elevated temporarily on condition that security requirements are met. Your permissions will be resumed after the request is processed, but the permissions elevation will be recorded in CTS logs and the operation user is recorded as **user_name** or **op_service**.
