# Oracle Cloud Infrastructure Ansible Collection

Oracle Cloud Infrastructure Ansible Collection provides an easy way to provision and manage resources in Oracle Cloud using Ansible.

> **This collection replaces the [legacy modules](https://github.com/oracle/oci-ansible-modules). Refer to the [Migration Guide](https://github.com/oracle/oci-ansible-collections/blob/master/MigrationGuide.md) for best migration practices.**

Ansible [released Collections](https://www.ansible.com/blog/getting-started-with-ansible-collections) as part of the Ansible 2.9 release. Ansible recommends Collections as the recommended method of packaging and releasing modules. 
With the creation of Oracle Cloud Ansible Collection, we are providing two user benefits:
 * **Faster Availability** - Oracle Cloud Ansible Modules will now be available to users at a faster pace on Ansible Galaxy. 
 * **Wider Coverage** - This summer, we aim to provide support for all the Oracle Cloud resources    
    
### Expected Change

Please expect a few [breaking changes](https://github.com/oracle/oci-ansible-collections/blob/master/MigrationGuide.md) as we transition from legacy modules to the new collection modules.
Also, the new modules are renamed to use the service name as a prefix.
We recommend you to refer to the [Migration Guide](https://github.com/oracle/oci-ansible-collections/blob/master/MigrationGuide.md) as you plan to migrate.

As we gradually make progress to provide full coverage of Oracle Cloud resources, you might not find all the familiar modules (that we support in the legacy modules) in the new collection.
In that case, you may choose to use the legacy modules as a workaround for the time being.

We have also added a new [User Guide](https://github.com/oracle/oci-ansible-collections/blob/master/UserGuide.md) to highlight new features and best practices for using the new modules.

### Currently Supported Services 
- Block Volume
- Compute/Compute Management
- Database
- Networking
- Container Engine for Kubernetes Service (OKE)
- Identity and Access Management (IAM)
- Load Balancing
- Object Storage
- File Storage
- Audit
- Autoscaling
- Budget/Account management
- Health Checks
- Vault Secret and Key Management (KMS)
- Domain Name System (DNS)
- Email
- Marketplace
- Monitoring
- Notifications
- Streaming
- Functions
- OS Management
- Resource Manager
- Announcement
- Integration
- NoSQL
- Events
- Service Limits
- API Gateway
- Content and Experience
- Analytics
- Web Application Acceleration and Security Services
- Limits
- Data Science
- Data Safe
- Data Catalog
- Data Flow
- Search
- Digital Assistant Instance
- MySQL
- Big Data
- Usage
- VMWare
- Data Integration

## Installation

#### 1) Installing the Collection with yum

You can use yum to install the Oracle Cloud Infrastructure Ansible Module Collection RPM.

The RPM installs the OCI Ansible module collection and its required dependencies: the OCI SDK for Python and Ansible.

The following example shows how to use yum to install the Ansible Module Collection RPM:
  ``` bash
$ yum -y install oraclelinux-developer-release-el7 && sudo yum install oci-ansible-collection
  ```
Note:
This installation uses Python version 3.6.

To test the installation of the RPM and configuration of the SDK, you can run a sample playbook. For example:
  ``` bash
$ ansible-playbook-3 /usr/share/doc/oci-ansible-collection-<version>/samples/object_storage/get_namespace/sample.yaml
  ```

#### 2) Installing collections from Ansible Galaxy

You can install it from [Ansible Galaxy](https://galaxy.ansible.com/oracle) using the command:
  ``` bash
  $ ansible-galaxy collection install oracle.oci
  ```
Notes:
* Collections is supported in Ansible 2.9+.
* For more information about collections, please check [Ansible Collections](https://docs.ansible.com/ansible/latest/user_guide/collections_using.html)
* To update the modules to latest version, use the install --force flag.

#### Install OCI Python SDK

The Oracle Cloud Ansible modules are built using the [Oracle Cloud Infrastructure Python SDK](https://docs.us-phoenix-1.oraclecloud.com/Content/API/SDKDocs/pythonsdk.htm).

[Install OCI Python SDK](https://oracle-cloud-infrastructure-python-sdk.readthedocs.io/en/latest/installation.html#downloading-and-installing-the-sdk):

  ``` bash
  $ yum -y install oraclelinux-developer-release-el7 && yum -y install python-oci-sdk
  or
  $ pip install oci
  ```
The modules honor the [SDK configuration](https://docs.us-phoenix-1.oraclecloud.com/Content/ToolsConfig.htm) when available.

#### For more info about installation and troubleshooting check the [Installation Guide](https://github.com/oracle/oci-ansible-collections/blob/master/InstallationGuide.md).

## Samples

The project includes a catalog of Oracle Cloud Infrastructure Ansible module samples that illustrate using the modules 
to carry out common infrastructure provisioning and configuration tasks. The samples are organized in groups associated 
with Oracle Cloud Infrastructure services under [the samples directory on GitHub](https://github.com/oracle/oci-ansible-collections/tree/master/samples).
Begin by reviewing the Readme.md file that you will find in each sample's root directory.

## Documentation
Module documentation is found [here](https://github.com/oracle/oci-ansible-collection/tree/master/docs). The HTML version is available on [readthedocs.io](https://oci-ansible-collection.readthedocs.io/en/latest/).

To view the module documentation, use this command:
  ``` bash
ansible-doc oracle.oci.[module_name]
  ```
General documentation for legacy and new modules can be found [here](https://docs.cloud.oracle.com/iaas/Content/API/SDKDocs/ansible.htm).


## Help

See the ["Questions or Feedback"](https://docs.cloud.oracle.com/en-us/iaas/Content/API/SDKDocs/ansible.htm#questions) section.

## Changes

See [CHANGELOG](https://github.com/oracle/oci-ansible-collections/blob/master/CHANGELOG.md).

## Contributing

This is an open source project. See [CONTRIBUTING](https://github.com/oracle/oci-ansible-collections/blob/master/CONTRIBUTING.md) for details.

Oracle gratefully acknowledges the contributions to `oci-ansible-collections` that have been made by the community.

## Known Issues

You can find information on any known issues on [GitHub issues](https://github.com/oracle/oci-ansible-collections/issues) page.

## License

Copyright (c) 2020, Oracle and/or its affiliates.

This software is made available to you under the terms of the GPL 3.0 license or the Apache 2.0 license.

See [LICENSE.txt](https://github.com/oracle/oci-ansible-collections/blob/master/LICENSE.txt) for more details.
