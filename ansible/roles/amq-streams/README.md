AMQ Streams
===========

Setup and configuration for Red Hat AMQ Streams

Example Playbook
----------------

  tasks:
    - name: Establish access to infrastructure
      include_role:
        name: ocp4-tokens

    - name: Deploy Red Hat AMQ Streams
      include_role:
        name: 3scale
      when:
        - var_amq_enabled is defined
        - var_amq_enabled