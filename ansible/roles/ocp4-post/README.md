OpenShift Cluster Post-Install Configuration
============================================

Role to perform post-install configuration on an OpenShift cluster

Example Playbook
----------------

  tasks:
    - name: Establish access to infrastructure
      include_role:
        name: ocp4-tokens

    - name: Deploy the OpenShift Aggregate Logging
      include_role:
        name: ocp4-post