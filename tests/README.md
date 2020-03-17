## Testing Signin Canada 
### Introduction 
Signin Canada Acceptance Platform application is using open source [Gluu server](https://www.gluu.org/) to provide the SAML and OIDC based authentication framework. In order to test the Acceptance Platform a Gluu server needs to be installed on RHEL7 or CentOS7 with [Couchbase Database](https://www.couchbase.com/). Ideally DB needs to be installed on a seperate VM if not then this can be installed locally but that will require a beefy VM. 

### VM Requirements
- RHEL7 or CentOS7 
- 16GB RAM 
- 2 CPUs
- 100 GB HDD if installing local database

### VM Setup Requirements 
To setup the VM and make it ready for Gluu server installation following changes need to be made
Most of the below steps are [scripted](install-gluu.sh) as well. 
- Hostname needs to be setup
- /etc/hosts file must have the local IP address and hostname resolvable
- Install the gluu server rpm specific version from [gluu repo](https://repo.gluu.org/#)
- Once the above changes are done then the Acceptance Platform Tarball needs to be copied over to the VM and untarred. 

For full details on [Gluu installation instructions](https://gluu.org/docs/ce/installation-guide/install-centos/)

### Optional local couchbase install
- If the plan is to install local couchbase DB then it has to be downloaded to below mentioned location. The couchbase folder needs to be created manually.
    - /opt/gluu-server/opt/dist/couchbase

