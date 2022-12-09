:original_name: en-us_topic_0100273725.html

.. _en-us_topic_0100273725:

Key Operations on VPC
=====================

VPC enables you to provision logically isolated, configurable, and manageable virtual networks for ECSs, improving the security of resources in enterprise clouds and simplifying network deployment.

With CTS, you can record operations associated with VPC for future query, audit, and backtrack operations.

.. table:: **Table 1** VPC operations that can be recorded by CTS

   ============================== ============== ===================
   Operation                      Resource Type  Trace Name
   ============================== ============== ===================
   Modifying the bandwidth        bandwidth      modifyBandwidth
   Creating an EIP                eip            createEip
   Releasing an EIP               eip            deleteEip
   Binding an EIP                 eip            bindEip
   Unbinding an EIP               eip            unbindEip
   Assigning a private IP address privateIps     createPrivateIp
   Releasing a private IP address privateIps     deletePrivateIp
   Creating a security group      security_group createSecurityGroup
   Modifying a security group     security_group modifySecurityGroup
   Creating a subnet              subnet         createSubnet
   Deleting a subnet              subnet         deleteSubnet
   Modifying a subnet             subnet         modifySubnet
   Creating a VPC                 vpc            createVpc
   Deleting a VPC                 vpc            deleteVpc
   Modifying a VPC                vpc            modifyVpc
   Creating a VPN                 vpn            createVpn
   Deleting a VPN                 vpn            deleteVpn
   Modifying a VPN                vpn            modifyVpn
   Creating a NAT gateway         natgateway     createNatGateway
   Updating a NAT gateway         natgateway     updateNatGateway
   Deleting a NAT gateway         natgateway     deleteNatGateway
   Creating an SNAT rule          snatrule       createSnatRule
   Deleting an SNAT rule          snatrule       deleteSnatRule
   Creating a DNAT rule           dnatrule       createDnatRule
   Deleting a DNAT rule           dnatrule       deleteDnatRule
   ============================== ============== ===================
