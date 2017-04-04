#Zabbix Templates for VMware ESXi/ESX monitoring 

## Description
Basic VMware Host monitoring templates.
Compatible with Zabbix Server 3.0 and vSphere >4.1

Provides Monitoring of the following parameters:

* Overall Host Status
* Host CPU usage (VMware MHz units)
* Memory Usage
* Network utilization
* Disk IO 
* And some others

_Note: These templates do not provide VMware Guest VM monitoring or discovery._


## Usage
* Be sure your zabbix server is configured for VMware monitoring. See parameters: StartVMwareCollectors, VMwareFrequency, etc.
* Import provided templates.
* Create vCenter SSO zabbix account with access to your vSphere infrastructure. 'Read-only' built-in role is sufficient. 
* Modify 'Template VMware Host Discovery' and 'Template VMware ESX Host' Macros section:
 * Zabbix Account Name within vCenter SSO
 * Password
 * vCenter URL
* Create new host for your vCenter Server and link it with 'Template VMware Host Discovery' template. 
 _Note: the default discovery period is 12 hours, you can lower it by changing interval of 'Template VMware Host Discovery -> Discovery Rules -> Discover ESXi Host'_
* For more info see official documentation: [[1]](https://pubs.vmware.com/vsphere-60/index.jsp#com.vmware.vsphere.security.doc/GUID-18071E9A-EED1-4968-8D51-E0B4F526FDA3.html), [[2]](https://www.zabbix.com/documentation/3.0/manual/vm_monitoring), [[3]](https://www.zabbix.com/documentation/3.0/manual/vm_monitoring/discovery_fields)


Based on official Zabbix VMware Templates from default installation.


## Authors
Dmitry Sarkisov <<ait.meijin@gmail.com>>


## License:
GNU GENERAL PUBLIC LICENSE. 
See 'COPYING'.
