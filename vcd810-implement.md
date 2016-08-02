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
