{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

#{{site.data.keyword.Bluemix_notm}} Local
{: #local}
*Last updated: 29 October 2015*

{{site.data.keyword.Bluemix}} Local brings the power and agility of the {{site.data.keyword.Bluemix_notm}} cloud-based platform to your data center. With {{site.data.keyword.Bluemix_notm}} Local, you can protect your most sensitive workloads behind your company firewall, while staying securely connected and in sync with {{site.data.keyword.Bluemix_notm}} Public. 
{:shortdesc}

IBM® uses cloud operations as a service to monitor and maintain your environment, so that you can focus on building apps and services that run on top of the environment. IBM also handles platform updates, so that you can focus on the business.

{{site.data.keyword.Bluemix_notm}} Local includes a private, syndicated catalog that displays the local services that are available exclusively to you. It also includes additional services that are syndicated from and available for you to use from {{site.data.keyword.Bluemix_notm}} Public.

{{site.data.keyword.Bluemix_notm}} Local sits on a virtual machine that is behind your company firewall, so that you have the highest performing and most secure cloud infrastructure available to you. IBM installs, remotely monitors, and manages {{site.data.keyword.Bluemix_notm}} Local in your data center through IBM's relay technology.

Relay is a delivery capability included with {{site.data.keyword.Bluemix_notm}} Local that enables IBM to automatically and consistently deliver updates to all local deployments, so that you always have an up-to-date, stable, and secure system. Relay achieves secure connectivity through an open, outbound SSL, VPN tunnel that originates from the inception virtual machine using certificates that are specific to each {{site.data.keyword.Bluemix_notm}} Local instance. The traffic on this tunnel is Urban Code Deployer automation for serving and maintaining the platform, compute resources, and services for your instance.

![{{site.data.keyword.Bluemix_notm}} Local overview](images/bluemixlocalarchitecture.png "Bluemix Local overview")

*Figure 1. {{site.data.keyword.Bluemix_notm}} Local detailed overview*

{{site.data.keyword.Bluemix_notm}} Local environments have the same security standards as the public {{site.data.keyword.Bluemix_notm}} in terms of operational security. You provide the hardware and infrastructure, which gives you control over infrastructure and physical security. Developer access to the local {{site.data.keyword.Bluemix_notm}} is controlled by your LDAP policies, which can be configured by the {{site.data.keyword.Bluemix_notm}} team when they set up your environment. Within the local environment, using the Admin Console, you can manage user roles and permissions.

{{site.data.keyword.Bluemix_notm}} Local comes with all included {{site.data.keyword.Bluemix_notm}} runtimes and 64 GB of compute memory.

In addition, there is a set of services available for {{site.data.keyword.Bluemix_notm}} Local.

| **Type** | **Name** | **Description** |    
|----------|----------|-----------------|
|Included | {{site.data.keyword.Bluemix_notm}} Runtimes | Use runtimes to get your app up and running quickly, with no need to set up and manage VMs and operating systems. All {{site.data.keyword.Bluemix_notm}} runtimes are available for you to use in your {{site.data.keyword.Bluemix_notm}} Local instance.|
|Included | {{site.data.keyword.autoscaling}}| Dynamically increase or decrease the compute capacity of your application based on policies. With this service, you have unlimited use in your {{site.data.keyword.Bluemix}} Local environment.|
|Optional |{{site.data.keyword.datacshort}}| This service provides an in-memory data grid that supports distributed caching scenarios for your apps. Includes 50 GB of in-memory cache. |
|Optional | {{site.data.keyword.APIM}} | Use the {{site.data.keyword.APIMfull}} service to compose, manage, and socialize APIs. You can import APIs with resources by using a proxy URL or by assembling data from HTTP data sources. The benefit of using the {{site.data.keyword.APIM}} service is that you can manage how your APIs are used. |

*Table 1. Local Services*

##Setting up your {{site.data.keyword.Bluemix_notm}} Local instance
{: #setuplocal}

{{site.data.keyword.Bluemix_notm}} Local is designed to provide a private version of the {{site.data.keyword.Bluemix_notm}} Public offering that is hosted on your own hardware, managed by you. You can use {{site.data.keyword.Bluemix_notm}} services and runtimes to support your computing needs in a secure, customer-hosted and managed cloud environment.

IBM provides you access to {{site.data.keyword.Bluemix_notm}} Local by using a password-secured login. You can access the services, runtimes, and associated resources, and deploy and remove {{site.data.keyword.Bluemix_notm}} apps. Review the following steps for working with your IBM representative to set up your local instance of {{site.data.keyword.Bluemix_notm}}.

To set up your private version of {{site.data.keyword.Bluemix_notm}}:

<ol>
<li>Review the <a href="index.html#localinfra">{{site.data.keyword.Bluemix_notm}} Local infrastructure requirements</a> for setting up your local instance.</li>
<li>Contact your IBM designated account representative or contact <a href="https://console.ng.bluemix.net/?direct=classic/#/contactUs/cloudOEPaneId=contactUs" target="_blank">{{site.data.keyword.Bluemix_notm}}</a> to get started.</li>
<li>Establish your {{site.data.keyword.Bluemix_notm}} Local agreement with IBM that includes milestone dates for delivery.
<ol type="a">
	<li>Work with IBM on your fee for your {{site.data.keyword.Bluemix_notm}} Local instance. The monthly recurring fee is based on the local services that you want to use, plus a subscription to all {{site.data.keyword.Bluemix_notm}} public services. You then receive an invoice for anything that you use beyond that subscription agreement.</li>
	<li>Identify the deadlines for each phase of setting up your {{site.data.keyword.Bluemix_notm}} Local instance.</li>
	</ol>
	</li>
<li>After your platform and account are created, you identify the people in your organization for the roles that are needed to get your local instance up and running.<br />
<br />
<dl>
<dt>**Procurement focal**</dt>
<dd>Works with IBM representatives on establishing your {{site.data.keyword.Bluemix_notm}} Local environment, including identifying the right people in your organization to work on any aspect of the project. This role oversees pattern selection, commercial arrangements, and arrangement of access to customer resources. The procurement focal is the overall contact for setting up the local instance.</dd>
<dt>**Compliance officer**</dt>
<dd>Works with IBM representatives to select a topology and deployment option that meets your security requirements. This role works with the IBM compliance consultants to determine which deployment patterns acheive the compliance goals and objectives.</dd>
<dt>**Network Specialist**</dt>
<dd>Works with IBM representatives on the network plans for the {{site.data.keyword.Bluemix_notm}} deployment. This role provides the requirements to the IBM representatives and works with the representatives on an implementation plan. At the end of the installation and verification phase, this role will "sign-off" that the network configuration is in compliance with corporate standards.</dd>
<dt>**DevOps focal**</dt>
<dd>Works with IBM representatives to plan and apply the maintenance updates that are needed for the {{site.data.keyword.Bluemix_notm}} platform, services, and runtimes. This role also works with the IBM representatives on the configuration of your {{site.data.keyword.Bluemix_notm}} Local instance.</dd>
</dl>
</li>
<li>You provide the hardware, and IBM helps you define and establish network connectivity between your corporate network and your {{site.data.keyword.Bluemix_notm}} Local instance. For more information about infrastructure requirements, see <a href="index.html#localinfra">{{site.data.keyword.Bluemix_notm}} Local infrastructure requirements</a>.
<ol type="a">
	<li>IBM configures network access and LDAP based on what you provided. Administrative access is given to the contacts that you designate. You must also designate a contact for support and billing.</li>
	<li>IBM sets up a syndicated catalog in your local environment to show your local services and many of the public {{site.data.keyword.Bluemix_notm}} services.</li>
	<li>You validate network and firewall configuration and the LDAP endpoint and access.</li>
	</ol>
</li>
</ol>

<!--audience="blue" staging only -->
##Roles and responsibilities
{: #rolesresponsibilities}

From choosing between {{site.data.keyword.Bluemix}} Public, Local, or Dedicated, to deploying and maintaining your environment, IBM is here to help. IBM has representatives to help you through each stage. 
{:shortdesc}

If you set up a Local or Dedicated {{site.data.keyword.Bluemix_notm}} account, you identify the people in your organization for the roles that are needed to get your instance up and running. Review the following customer roles and responsibilities that you assign:

<dl>
<dt>**Procurement focal**</dt>
<dd>Works with the IBM representative on establishing your {{site.data.keyword.Bluemix_notm}} Local environment, including identifying the right people in your organization to work on any aspect of the project. This role oversees pattern selection, commercial arrangements, and arrangement of access to customer resources. The procurement focal is the overall contact for setting up the local instance.</dd>
<dt>**Compliance officer**</dt>
<dd>Works with the IBM representative to select a topology and deployment option that meets your security requirements. This role works with the IBM compliance consultant to determine which deployment patterns achieve the compliance goals and objectives.</dd>
<dt>**Network specialist**</dt>
<dd>Works with the IBM representative on the network plans for the {{site.data.keyword.Bluemix_notm}} deployment. This role provides the requirements to the IBM representative and works together on an implementation plan. At the end of the installation and verification phase, this role will "sign-off" that the network configuration is in compliance with corporate standards.</dd>
<dt>**DevOps focal**</dt>
<dd>Works with the IBM representative to plan and apply the maintenance updates that are needed for the {{site.data.keyword.Bluemix_notm}} platform, services, and runtimes. This role also works with the IBM representative on the configuration of your {{site.data.keyword.Bluemix_notm}} Local instance.</dd>
<dt>**IaaS specialist**</dt>
<dd>TBD and differs for Local and Dedicated</dd>
</dl>

Your customer representatives work with a dedicated Client Success Manager (CSM) and other IBM specialists that work together to ensure that you always have the support that you need. Through setting up your environment to continued maintenance, a variety of tasks must be completed. The following table outlines the required tasks and the owner for completing the task.

*Table 1. Tasks and responsibilities*

| **Task** | **Task details** | **Responsible party** |    
|----------|------------------|-----------------------|
|Set compliance and standards | Identify government, industry, and proprietary corporate standards that are required for the environment. | Customer |
|Create security and compliance integration plan | Create security and integration plan including costs, scheduling, and resources that are required to achieve security compliance. | IBM |
|Compliance plan approval | Approve the compliance plan. | Customer |
|Create sizing for environment |  	Create environment sizing based on predefined choices that take into consideration the high availability and disaster recovery goals, as well as initial DEA and service provisioning that is necessary to support the apps created with the platform. | IBM and customer share responsibility |
|Select architecture | Selection of architecture based on predefined choices that take into account high availability and disaster recovery requirements. | IBM |
|Define disaster recovery goals | Define the disaster recovery requirements for the environment. | Customer |
|Create disaster recovery plan | Consult and define the disaster recovery plan. | IBM and customer share responsibility |
|Create back up and recovery plan | Create back up and recovery plan that defines the frequency and the requirements for on-and-off site distribution of the back up. | IBM |
|Identify tools for event detection and problem determination | Identify IBM and third-party tools used for event detection and problem determination. | IBM |
|Define escalation plan | Define the escalation plan to triage and resolve events detected from the monitoring components. | IBM |
|Sign infrastructure, platform, and support agreements | Sign the subscription agreement including the financial terms and conditions for the environment. Sign network and security monitoring agreement. Sign support subscription. | Customer |
|Procurement of environment | Procurement of Core and Services VLAN to host {{site.data.keyword.Bluemix_notm}}, bare metal services to host Data Power, and SoftLayer Firewall (for Dedicated only). Provide infrastructure to allow for VPN tunnel. | Customer |
|Install and configure monitoring and management components | Install, configure, and verify the monitoring components as defined in the escalation and problem determination plan. | IBM |
|Install and configure application components |  	Install, configure, and verify DEAs and Service providers. | IBM |
|Install fabric components | Install, configure, and verify fabric components such as Bosh Director, Cloud Controller, Health Manager, Messaging, and Routers. | IBM |
|Establish initial network configuration | Establish initial network configuration including firewalls, DataPower, Fortigate, and DNS. | IBM |
|Install and configure security components | Install and configure security components that are tied into the monitoring and escalation plan including Qradar, Credential Vault, Intrusion Prevention System (IPS), IBM Endpoint Manager (IEM), and Privilege Identity Manager. | IBM |
|Install and configure custom components |  	Install and configure custom components that reside outside the scope of the {{site.data.keyword.Bluemix_notm}} product and services. | Customer |
|Install VPN solution | Install bi-directional VPN solution. | IBM |
|Connect {{site.data.keyword.Bluemix_notm}} pipeline | Connect {{site.data.keyword.Bluemix_notm}} CI/CD pipeline with IBM repositories. | IBM |
|Customize external solution components | F5 Big IP and Global and Local Load Balancers | Customer |
|Configure login server | Configure the login server for use with the corporate LDAP. | IBM |
|Track status for security, compliance, and audit controls  | Track status up to the point where all tools and processes are in place to achieve identified compliance. | Customer |
|Review physical infrastructure | Review of physical premises that host the solution components for threats and review of security controls to protect the data center. | Customer |
|Inspect monitoring software | Inspection of monitoring and management components as defined in the escalation and problem determination plan. | Customer |
|Inspect OS | Inspect that the operating system image meets compliance standards. | Customer |
|Review weekly capacity reports | Review the weekly capacity reports and take corrective action, if needed. | Customer |
|Create month-to-month projection | Collect information and create a month-to-month projection of capacity and consumption. | IBM and customer share responsibility |
|Review projections | Review the capacity projections as it relates to external events that might impact capacity. | Customer |
|Document require maintenance | Create documentation for the required maintenance of IBM solution components. | IBM |
|Perform network and IP scans | Perform daily and monthly network and IP scans. | IBM and customer share responsibility |
|Provide access to audit logs | Provide access to all security and administrative audit logs.   | IBM and customer share responsibility |
|Conduct testing | Conduct periodic Key Control over Operations (KCO) testing and third-party penetration testing. | IBM and customer share responsibility |
|Status reporting, audit coordination, and compliance meetings  | Complete status reporting, external audit coordination, and representation at compliance review status meetings. | IBM |
|Employment verification | Complete quarterly employment verification. | IBM |
|Business need verification | Complete quarterly "continued business need" verification. | IBM |
|Resolution of security vulnerabilities | Resolve reported security vulnerabilities in the platform. | IBM |
<!--audience="blue" staging only -->
	
##{{site.data.keyword.Bluemix_notm}} Local infrastructure requirements
{: #localinfra}

For {{site.data.keyword.Bluemix_notm}} Local, you own the physical security and the infrastructure for hosting the local instance. IBM sets the following requirements for setting up {{site.data.keyword.Bluemix_notm}} Local.
###Hardware
While there are requirements for the type and size of available hardware, you can choose any combination to meet the set resource total requirements.
<dl>
<dt>**VMware ESXi hardware**</dt>
<dd>
ESXi is a virtualization layer that runs on physical servers and that abstracts processor, memory, storage, and resources into multiple virtual machines. Choose any combination that meets the following resource totals, on the condition that minimum physical core count per ESXi is eight. The following specifications are for the {{site.data.keyword.Bluemix_notm}} core runtime only.
<ul>
<li>48 Physical cores at 2.0 of more GHz each</li>
<li>756 GB of physical RAM</li>
</li>Total datastore size of 7.5 TB 
<ul>
<li>7 TB datastore to hold {{site.data.keyword.Bluemix_notm}}</li>
<li>500 GB datastore to hold the inception virtual machine</li>
</ul>
</ul>
<p><strong>Note:</strong> If you use multiple datastores, use the same prefix for each.</p>
</dd>
<dt>**High availability**</dt>
<dd>
To support a single node failure, you must have n+1 ESXi. For example, if two ESXis are used, meaning 16x cores each, then a third is needed.
<p><strong>Note:</strong> The customer VMware administrator can decide to enforce strict high availability failover in the cluster to guarantee resources.</p>
</dd>
<dt>**Network**</dt>
<dd>
Recommended requirements include a customer accessible port group with 10 customer network IP addresses that have outbound internet access. Then, define a second private VLAN between only the ESXis being used for {{site.data.keyword.Bluemix_notm}} Local. This VLAN is shown as a port group in VMware. {{site.data.keyword.Bluemix_notm}} Local uses it for the private subnet, which is more secure and can help avoid routing issues.
</dd>
</dl>

###vCenter server configuration
Review the following version, datacenter, resource pool, and datastore requirements.
<dl>
<dt>**Supported VMware versions**</dt>
<dd>vCenter and ESXi 5.1 and 5.5</dd>
<dt>**Datacenter**</dt>
<dd>Create a datacenter, if one does not exist.</dd>
<dt>**Datacenter folder**</dt>
<dd>Create a VM folder with the same name as the cluster, if you do not plan to grant Administrator access that is propagated from the datacenter.</dd>
<dt>**Cluster**</dt>
<dd>Create a cluster specifically for {{site.data.keyword.Bluemix_notm}} Local use. An example for the cluster name is `bluemix`.</dd>
<dt>**Resource pool**</dt>
<dd>Create a resource pool under the {{site.data.keyword.Bluemix_notm}} Local cluster. An example for resource pool name is `local`.</dd>
</dt>**Datastores**</dt>
<dd>Requires 7.5 TB for the initial deployment of {{site.data.keyword.Bluemix_notm}}.<br />
<br />
**Note**: When you use more than one datastore, ensure that each one begins with the same prefix. Examples of multiple datastore names with the same prefix are `bluemix_datastore_01` and `bluemix_datastore_02`.</dd>
</dl>

###Network Bandwidth
Recommended throughput is 5 Mbps up and 5 Mbps down, and you can expect a monthly data usage of 10 GB. IBM establishes agreed upon windows when large bundles of data are delivered, which can be as large as 3 GB.
###VMware permissions
Set the following roles and permissions. Propagation is set for each permission. If the permission is propagated, the permission gets passed down through the object hierarchy. However, permissions for a child object always override permissions that are propagated from a parent object.
<dl>
<dt>**v Center Server**</dt>
<dd>Set the role as read-only and not propagated.<br />
<br />
**Note**: This role is needed to retrieve task status for specific disk operations.</dd>
<dt>**Datacenter**</dt>
<dd>Create the role "{{site.data.keyword.Bluemix_notm}}" and grant permissions for **Datastore** including **Low level file operations** and **Update virtual machine files**.<br />
<br />
**Note**: This role is needed to support file posts to the datastores.</dd>
<dt>**Cluster**</dt>
<dd>Set the role as administrator and propagated.</dd>
<dt>**Datastores**</dt>
<dd>Set the role administrator and propagated for each {{site.data.keyword.Bluemix_notm}} datastore.</dd>
<dt>**Network**</dt>
<dd>Set public and private port groups with the administrator role, not propagated.</dd>
</dl>

###Droplet Execution Agent (DEA) pool
Each DEA is configured with:
- 16 - 32 GB of RAM
- 2x - 4x vCPU
- 150 - 300 GB of storage

For example, if the ESXi host size is 256 GB of memory with 16x cores, then eight DEAs are added. If the ESXi host size is 64 GB of memory with 8x cores, then two ESXis and four DEAs are required to be added. An additional 1.5 TB of storage is required for every four DEAs. This example is based on a DEA configured with 32 GB of RAM, 4x vCPU, and 300 GB of storage.

##Maintaining your local instance
{: #maintainlocal}

IBM maintains and installs updates and fixes as IBM deems appropriate to the Bluemix Local platform, runtimes, and services. Services might not be available during maintenance windows.

**Important**: IBM reserves the right to interrupt services to apply emergency maintenance as needed. IBM might change scheduled maintenance hours, but notifies you of any such changes, as well as any emergency maintenance information.

The following types of maintenance are required for {{site.data.keyword.Bluemix_notm}} Local:
<dl>
<dt>**Standard Maintenance Windows**</dt>
<dd>The services utilize pre-defined, standard maintenance windows, which might cause the services to be unavailable. IBM does not require customer approval to perform maintenance, but attempts to minimize impact to your services.<br />
<br />
IBM sends broadcast messages of the changes that are planned for each maintenance window, through email, phone, or other methods.<br />
<br />
**Important**: Some service might not be available to you during the maintenance period.</dd>

<dt>**Monthly Change Window**</dt>
<dd>The monthly maintenance window is applied based on coordination between you and IBM within a 21-day window. You can provide IBM with specific dates or times within the 21-day window that might not work for you. IBM attempts to schedule updates around those times. Based on the requests, IBM communicates the scheduled maintenance window to you. Monthly change windows are not expected to impact the running Bluemix Local environment.<br />
<br />
**Note**: If you do not request a specific time for the update, the maintenance is automatically applied at the end of the window.<br />
<br />
Go to **ADMINISTRATION > SYSTEM INFORMATION** to view pending updates, set unavailable dates, and approve updates. For more information about notifications and scheduling pending updates, see <a href="../admin/index.html#oc_system">Viewing system information</a>.</dd>

<dt>**Other**</dt>
<dd>IBM intends to confine all maintenance that might affect your services, in particular the availability of your Bluemix Local environment, runtimes, and services, to the standard and monthly windows. Other change windows might be used on an exception basis for management of the environment. IBM makes reasonable efforts to minimize the impact to you during such change windows and notifies you in advance.</dd>
</dl>

To set up maintenance of your local instance, work with your IBM designated account representative to identify an agreed upon window for the standard maintenance.

##Restoring your local instance
{: #restorelocal}

{{site.data.keyword.Bluemix_notm}} Local settings and configurations are backed up regularly to prepare for any unplanned outages in the environment.

As part of the backup of your data, IBM completes the following tasks:

<ul>
<li>Encrypts all backup copies and manages encryption keys</li>
<li>Monitors and manages backup activity</li>
<li>Provides the encrypted backup files</li>
<li>Restores the requested data</li>
<li>Manages scheduling conflicts between backup and fix management operations</li>
</ul>

Because protection of private data is critical, IBM needs your collaboration when dealing with backup file management, so that the files are not moved outside of your data centers. Specifically, IBM asks that you complete the following tasks:

<ul>
<li>Move a copy of your encrypted backup data off-site, just as you would for any other backup data that you manage.</li>
<li>Provide the backup files for the IBM operator in case of any need to restore.</li>
</ul>
   
# rellinks
## general 
* [Discover: {{site.data.keyword.Bluemix_notm}} Local](http://www.ibm.com/cloud-computing/bluemix/hybrid/local/)
