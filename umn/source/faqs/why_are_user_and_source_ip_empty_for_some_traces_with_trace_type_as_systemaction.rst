:original_name: cts_faq_019.html

.. _cts_faq_019:

Why Are **user** and **source_ip** Empty for Some Traces with **trace_type** as **systemAction**?
=================================================================================================

The **trace_type** field indicates the request resource. This field can be **ConsoleAction**, **ApiCall**, and **SystemAction**.

**SystemAction** indicates that the operations are not triggered by users, such as automatic alarms, elastic scaling, scheduled backup tasks, and secondary invocations generated within the system to respond to the user's request. In this case, no user or device that triggers an operation exists. Therefore, **user** and **source_ip** are both empty.
