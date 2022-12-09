:original_name: cts_faq_007.html

.. _cts_faq_007:

What Will Happen If I Have Enabled CTS But Have Not Configured a Correct Policy for the OBS Bucket?
===================================================================================================

CTS will deliver trace files based on the existing OBS bucket policy. If the policy is incorrectly configured, CTS may not deliver trace files to the OBS bucket.

If an OBS bucket has been deleted or encounters an exception, an error message will be displayed on the management console. In this case, you can choose to create an OBS bucket or reconfigure the access permissions of the OBS bucket. For detailed operations, see the "Bucket Management" section in the *Object Storage Service User Guide*.
