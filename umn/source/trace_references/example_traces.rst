:original_name: en-us_topic_0044019595.html

.. _en-us_topic_0044019595:

Example Traces
==============

This section provides two example traces and describes their key fields to help you better understand traces. You can read other traces in a similar way as shown below.

For details on the fields in a trace, see :ref:`Trace Structure <en-us_topic_0030598500>`.

ECS Server Creation
-------------------

.. code-block::

   {
       "time": "12/01/2016 11:07:28 GMT+08:00",
       "user": {
           "name": "aaa/op_service",
           "id": "f2fe9fac63414a35a7d03108d5f1ea73",
           "domain": {
               "name": "aaa",
               "id": "1f9b9ba51f6b4061bd5c1736b28469f8"
           }
       },
       "request": "{\"server\":{\"name\":\"as-config-15f1_XWO68TFC\",\"imageRef\":\"b2b2c7dc-bbb0-4d6b-81dd-f0904023d54f\",\"flavorRef\":\"m1.tiny\",\"personality\":[],\"vpcid\":\"e4c374b9-3675-482c-9b81-4acd59745c2b\",\"nics\":[{\"subnet_id\":\"fff89132-88d4-4e5b-9e27-d9001167d24f\",\"nictype\":null,\"ip_address\":null,\"binding:profile\":null,\"extra_dhcp_opts\":null}],\"adminPass\":\"********\",\"count\":1,\"metadata\":{\"op_svc_userid\":\"26e96eda18034ae9a44130bacb967b96\"},\"availability_zone\":\"az1.dc1\",\"root_volume\":{\"volumetype\":\"SATA\",\"extendparam\":{\"resourceSpecCode\":\"SATA\"},\"size\":40},\"data_volumes\":[],\"security_groups\":[{\"id\":\"dd597fd7-d119-4994-a22c-891fcfc54be1\"}],\"key_name\":\"KeyPair-3e51\"}}",
       "response": "{\"status\":\"SUCCESS\",\"entities\":{\"server_id\":\"42d39b4a-19b7-4ee2-b01b-a9f1353b4c54\"},\"job_id\":\"4010b39d58b855980158b8574b270018\",\"job_type\":\"createSingleServer\",\"begin_time\":\"2016-12-01T03:04:38.437Z\",\"end_time\":\"2016-12-01T03:07:26.871Z\",\"error_code\":null,\"fail_reason\":null}",
       "service_type": "ECS",
       "resource_type": "ecs",
       "resource_name": "as-config-15f1_XWO68TFC",
       "resource_id": "42d39b4a-19b7-4ee2-b01b-a9f1353b4c54",
       "source_ip": "",
       "trace_name": "createSingleServer",
       "trace_status": "normal",
       "trace_type": "SystemAction",
       "api_version": "1.0",
       "record_time": "12/01/2016 11:07:28 GMT+08:00",
       "trace_id": "4abc3a67-b773-11e6-8412-8f0ed3cc97c6"
   }

Note the following fields:

-  **time** indicates the time when the trace occurred. In this example, the time is 11:07:28 on December 1.
-  **user** indicates the user who performed the operation. In this example, the user (**name** field) is displayed under the enterprise account **aaa** (**domain** field).
-  **request** indicates the request to create an ECS server. It contains basic information about the server, such as its name (**as-config-15f1_XWO68TFC**) and ID (**e4c374b9-3675-482c-9b81-4acd59745c2b**).
-  **response** indicates the response to the ECS creation request. It contains **status** (**SUCCESS** in this example), **error_code** (**null** in this example), and **fail_reason** (**null** in this example).

EVS Disk Creation
-----------------

.. code-block::

   {
       "time": "12/01/2016 11:24:04 GMT+08:00",
       "user": {
           "name": "aaa",
           "id": "26e96eda18034ae9a44130bacb967b96",
           "domain": {
               "name": "aaa",
               "id": "1f9b9ba51f6b4061bd5c1736b28469f8"
                      }
                },
       "request":  "{\"volumes\":[{\"id\":\"49b52508-7cd1-4642-ade5-dfecb853c8a0\"},{\"id\":\"8aa423db-052b-4ecf-a748-53eab02d4cf0\"},{\"id\":\"4b1ee16f-a469-47eb-9433-4fac2a2f959a\"},{\"id\":\"edc7f193-8fd8-44b3-812b-63cb57fd7932\"},{\"id\":\"4094a2c3-9d62-4a24-bb2e-0f417d27834a\"}]}",,
       "response": "{\"job_id\":\"ff808082814cc2ee01828d0a608067c7\",\"job_type\":\"deleteVolume\",\"begin_time\":\"2022-08-11T13:14:03.775Z\",\"end_time\":\"2022-08-11T13:14:07.458Z\",\"status\":\"SUCCESS\",\"error_code\":null,\"fail_reason\":null,\"entities\":{\"volume_type\":\"SAS\",\"volume_id\":\"edc7f193-8fd8-44b3-812b-63cb57fd7932\",\"size\":10,\"name\":\"volume-8631-lxrtest-0002\"}}",
       "service_type": "EVS",
       "resource_type": "evs",
       "resource_name": "volume-39bc",
       "resource_id": "229142c0-2c2e-4f01-a1b4-2dfdf1c678c7",
       "source_ip": "10.146.230.124",
       "trace_name": "deleteVolume",
       "trace_status": "normal",
       "trace_type": "ConsoleAction",
       "api_version": "1.0",
       "record_time": "1660223647458765184",
       "trace_id": "c529254f-bcf5-11e6-a89a-7fc778a6c92c"
   }

Note the following fields:

-  **time** indicates the time when the trace occurred. In this example, the time is 11:24:04 on December 1.
-  **user** indicates the user who performed the operation. In this example, the user (**name** field) is displayed under the enterprise account **aaa** (**domain** field).
-  **request** is optional. It is null in this example.
-  **response** is optional. It is null in this example.
-  **trace_status** indicates the trace status. This field can replace the **response** field to indicate the operation results. In this example, the value is **normal**, indicating that the operation was successful according to :ref:`Trace Structure <en-us_topic_0030598500>`.
