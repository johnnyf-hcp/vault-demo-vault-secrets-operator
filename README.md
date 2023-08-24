# Demo of HashiCorp Vault - Vault Secrets Operator

This is a demo of HashiCorp Vault's Vault Secrets Operator component which allows for syncing of secrets stored or dynamically generated from HashiCorp Vault to Kubernetes (K8s) secrets.  This has a couple of benefits.
- Application Developers can still work with native K8s secrets without having to change their application code or integrate with HashiCorp Vault directly
- Performance is better than using Vault sidecars as the rotation of secrets is done in a single place.
- Restart of application pods is done using the native K8s mechanism when the secret is refreshed.

In this demo, we will cover:
- Setup of Vault's Dynamic Secret
- Configuration of VSO to utilize the dynamic secret
- Configure the caching persistence in VSO (optional)
- Testing of application pods restart when secrets are refreshed


This is using a Jupyter notebook to execute the steps required.
It also assumes that you have HashiCorp Vault installed and configured on your side.

You can use Visual Studio Code to run the notebook using Jupyter plugins.
