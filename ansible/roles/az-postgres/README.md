Azure Postgres
==============

Setup and configuration for an instance of Azure Postgres server and database

Example Playbook
----------------

  tasks:
    - name: Establish access to infrastructure
      include_role:
        name: ocp4-tokens

    - name: Deploy Azure Postgres server and database
      include_role:
        name: az-postgres
