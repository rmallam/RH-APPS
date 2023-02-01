OpenShift Cluster cert-manager Configuration
============================================

Role to perform cert-manager install and config to manager openshift ingress and api certs

Example Playbook
----------------

  tasks:
    - name: Establish access to infrastructure
      include_role:
        name: ocp4-tokens

    - name: Deploy and configure cert-manager on openshift to manager certs
      include_role:
        name: cert-manager