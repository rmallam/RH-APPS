# Azure Red Hat OpenShift Deployment Automation
This repository contains two Ansible playbooks, intended to be run
1. To configure the cluster for the first time, right after it gets deloyed. This involves invoking
  - The ocp4-tokens role that establishes connectivity to Azure and OpenShift.
  - The ocp4-post role that performs the cluster configuration
  - The ocp4-efk role that deployes the logging stack
  - The ocp4-monitoring role that deploys the Prometheus and Alertmanager monitoring stack.

2. To immediately deploy any desired payload onto the cluster. This involves invoking
  - The ocp4-tokens role that establishes connectivity to Azure and OpenShift.
  - The quay role if the variable var_3scale_enabled is set to true.
  - The sso role if the variable var_sso_enabled is set to true.
  - The 3scale role if the variable var_3scale_enabled is set to true.
  - Additional roles as and when they get added to this repository.

Information pertaining to each instance should be passed in from Ansible Tower as variables in one of two forms:
- As extra_vars set in the Job Template
- As credentials