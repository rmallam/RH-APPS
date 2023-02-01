OpenShift Cluster Logging
=========================

Setup and configuration for an instance of Azure Postgres server and database

Example Playbook
----------------

  tasks:
    - name: Establish access to infrastructure
      include_role:
        name: ocp4-tokens

    - name: Deploy the OpenShift Aggregate Logging
      include_role:
        name: efk