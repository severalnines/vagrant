# ClusterControl Vagrant files
Vagrant files to install the latest released ClusterControl version on Centos/Redhat or Debian/Ubuntu based distributions.
The default MySQL root user password on the ClusterControl host is 'root123'.

    $ git clone git@github.com:severalnines/vagrant.git

## Centos
Launches 1 instance for ClusterControl and 3 instances for DB Nodes. 

    # Download a base image from HashiCorp. 
    # If you want to use an existing or another box then change the Vagrantfile first.
    $ vagrant box add chef/centos-7.0
    $ cd clustercontrol/centos
    $ vagrant up

## Ubuntu
Launches 1 instance for ClusterControl and 3 instances for DB Nodes.

    # Download a base image from HashiCorp. 
    # If you want to use an existing or another box then change the Vagrantfile first.
    $ vagrant box add ubuntu/trusty64
    $ cd clustercontrol/ubuntu 
    $ vagrant up

## Default Instances
The default memory allocated for each instance is 768MB.

- 10.10.10.10 ClusterControl
- 10.10.10.11 DB 1
- 10.10.10.12 DB 2
- 10.10.10.13 DB 3

Open your web browser to http://localhost:8080/clustercontrol

1. Register your ClusterControl admin user.
2. Create your database cluster on the available DB nodes by clicking on 'Create Database Cluster'.
