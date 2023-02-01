Red Hat Quay
============

Setup and configuration for Red Hat Quay

Example Playbook
----------------

  tasks:
    - name: Establish access to infrastructure
      include_role:
        name: ocp4-tokens

    - name: Deploy Red Hat Quay
      include_role:
        name: quay
      when:
        - var_quay_enabled is defined
        - var_quay_enabled


