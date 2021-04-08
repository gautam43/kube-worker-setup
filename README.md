kube_worker_setup
=========
This role is used to setup the worker node in the kubernetes cluster 

Requirements
------------
To use this rule, first requirement is to launch the ec2_launcher role which launches instances and copy the master IP to the inventory in a [kube-master] group and similarly worker IP in the [kube-worker]. use the dynamic inventory concept to add the IPs dynacally.

Role Variables
--------------
1. location_join - This variable is used for the location where you want to store the join command i.e the last command which is created by the master and should be run in the worker node to connect worker node to master node.

Dependencies
------------
Other roles required are gautam43.ec2_launcher for launching the instances of master and worker

Example Playbook
----------------
Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: kube-worker
      roles:
         - role: gautam43.kube-worker-setup
License
-------
MIT

Author Information
------------------
For the Queries contact me on:-
Gmail - gautamkhatri43@gmail.com
