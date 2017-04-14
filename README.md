# ClusterControl Vagrant files
Vagrant files to install the latest released ClusterControl version on Centos/Redhat or Debian/Ubuntu based distributions.

    $ git clone https://github.com/severalnines/vagrant.git

## Centos
Launches 1 instance for ClusterControl and 3 instances for DB Nodes. 

    # Download a base image from HashiCorp. 
    # If you want to use an existing or another box then change the Vagrantfile first.

    $ vagrant box add bento/centos-7.3
    $ cd clustercontrol/centos
    $ vagrant up

## Ubuntu
Launches 1 instance for ClusterControl and 3 instances for DB Nodes.

    # Download a base image from HashiCorp. 
    # If you want to use an existing or another box then change the Vagrantfile first.

    $ vagrant box add bento/ubuntu-16.04
    $ cd clustercontrol/ubuntu 
    $ vagrant up

## Default Instances
The default memory allocated for each instance is 1024MB.

    # hosts
    $ cat /etc/hosts
    10.10.10.10 clustercontrol.local
    10.10.10.11 db1.local
    10.10.10.12 db2.local
    10.10.10.13 db3.local
    10.10.10.14 db4.local
    10.10.10.15 db5.local

## Default Users and Passwords

    # default password for the ssh vagrant user is 'vagrant' 
    $ vagrant ssh vm1

    # default password for the cmon user is 'cmon'
    $ mysql -u cmon -p -e "select 1"
    
    # default password for the mysql root user is 'root123'
    $ mysql -u root -p -e "select 1"

Open your web browser to http://10.10.10.10/clustercontrol

1. Register your ClusterControl admin user.
2. Create your database cluster by clicking on 'Deploy' to start the deployment wizard.
