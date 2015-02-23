Atlassian ansible role.
===================

Based off the work by Matt Willsher @ mattwillsher/ansible-product-playbooks

========
This ansible role performs a basic install of Jira & Confluence. The following variables are required:

* product - provide as a playbook parameter variable and set to the product to install e.g. jira, confluence e.g. ```- include: atlassian/install_product.yml product=jira```

Other variables need to be set:

* database_server - the IP address of the DB server to use. Current only localhost is tested
* version - the version to install e.g. 6.3.15
* rmiPort - Port to run RMI on e.g. 8005
* httpPort - Port to listen for HTTP requests on e.g 8080

The generated database password will be stored in <code>../../$client_shortname/credentials/jira/database</code>.
