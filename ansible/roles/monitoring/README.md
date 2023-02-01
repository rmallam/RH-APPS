OpenShift Cluster Monitoring
============================

Setup and configuration for OpenShift Cluster Monitoring

Example Playbook
----------------

  tasks:
    - name: Establish access to infrastructure
      include_role:
        name: ocp4-tokens

    - name: Deploy the OpenShift Aggregate Logging
      include_role:
        name: monitoring