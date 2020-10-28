k8s
=========

    Install and configure Kubernetes HA on Centos7

Role Variables
--------------

    k8s_pod_network_cidr: ''  [ default: 10.244.0.0/16 ] pod network cidr
    k8s_master_node: ''       [ default: {{ groups [ 'k8s_master' ] | first }} ] master node to scale cluster
    
    k8s_install: ''           [ default: true ] disable log secrets

Example Playbook
----------------

    - hosts: k8s_cluster
      become: true
      roles:
        - { name: k8s, tags: k8s }

License
-------

    MIT

Author Information
------------------

    Dmitrij Petrov
