Red Hat Data Grid
=================

Setup and configuration for Red Hat Data Grid

Example Playbook
----------------

  tasks:
    - name: Establish access to infrastructure
      include_role:
        name: ocp4-tokens

    - name: Deploy Red Hat Data Grid
      include_role:
        name: rhdg
      when:
        - var_rhdg_enabled is defined
        - var_rhdg_enabled
