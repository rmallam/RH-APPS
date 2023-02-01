Red Hat SSO
===========

Setup and configuration for Red Hat SSO

Example Playbook
----------------

  tasks:
    - name: Establish access to infrastructure
      include_role:
        name: ocp4-tokens

    - name: Deploy Red Hat SSO
      include_role:
        name: rhdg
      when:
        - var_sso_enabled is defined
        - var_sso_enabled
