# VMware vCloud Director for Service Provider V8.10 Implementation Jumpstart

## Release Notes
http://pubs.vmware.com/Release_Notes/en/vcd/8-10/rel_notes_vcloud_director_8-10.html

## Prerequisite
* http://partnerweb.vmware.com/comp_guide2/sim/interop_matrix.php#interop&224=977
* VMware vCenter 5.5 U3+, 6.0 U1+
* VMware NSX Manager 6.1.5+, 6.2.2+

## Topology
* Recommended at least 2 virtual servers for vCD application and vCD database servers
* vCD application server should have 2 vNICs for HTTP service and remote console proxy (same subnet is OK)

## vCD Application Server Operating Systems
* http://pubs.vmware.com/Release_Notes/en/vcd/8-10/rel_notes_vcloud_director_8-10.html
* CentOS 6, 7 minimal installation
* Red Hat Enterprise Linux 5 U4+, 6 U1+, 7+ minimal installation
* yum install alsa-lib bash chkconfig coreutils indutils glibc grep initscripts krb5-libs libgcc libICE libSM libstdc libX11 libXau libXdmcp libXext libXi libXt libXtst module-init-tools net-tools pciutils procps redhat-lsb sed tar which

## Databases
* http://partnerweb.vmware.com/comp_guide2/sim/interop_matrix.php#db&224=977
* Oracle 11g, 12C
* Microsoft SQL Server 2012. 2014

## Installation
* https://www.vmware.com/support/pubs/vcd_sp_pubs.html

## Comparing with OpenStack
* OpenStack's security group and network virtualization (SDN) done on NSX edge
* OpenStack's stack = vCD's vApp
* vCD's network should predefine network segment as 1 of 3 options belows due to NSX edge design: http://pubs.vmware.com/vcd-810/index.jsp#com.vmware.vcloud.admin.doc_810/GUID-75BEEF03-6176-47A1-9D6E-8C7A305DD649.html
 * External organization virtual datacenter network - direct connection
 * External organization virtual datacenter network - NAT-routed connection
 * Internal organization virtual datacenter network
* vCD may consume external IP addresses than OpenStack because vCD has to define suballocate IP pools on an edge gateway per organization rather than using one IP pools in OpenStack
* OpenStack is easier when connecting internal network to external network due to using only securiy group feature while vCD has to setup SNAT, DNAT policy which is complex to server engineer
* vCD can set VM's administrator password after provisioning using its guest customization feature
