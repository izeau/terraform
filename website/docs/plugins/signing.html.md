---
layout: "registry"
page_title: "Plugin Signing"
sidebar_current: "docs-plugins-signing"
description: |-
  Terraform plugin signing trust levels
---

# Plugin Signing

There are four levels of signing and programattic authentication for plugins in Terraform:

* **Signed by HashiCorp** - are built, signed, and supported by HashiCorp. Official provider plugins can 
typically be used without specifying provider source information in your Terraform configuration.
* **Signed by Trusted Partners** - are built, signed, and supported by a third party. HashiCorp has 
verified the ownership of the private key and we provide a chain of trust to the CLI to verify this
programatically. To use partner providers in your Terraform configuration, you need to specify the
provider source, typically this is the namespace and name to download from the registry.
* **Self-signed** - are built, signed, and supported by a third party. HashiCorp does not provide a verification or chain of trust for the signing. You will want to obtain and validate fingerprints manually if you want to ensure you are using a binary you can trust.
* **Unsigned** - Terraform does support fetching and using unsigned binaries, but you should take extreme care when doing so as no programatic authentication is performed on the downloaded binary.

Usage of plugins from the registry is subject to the Registry's [Terms of Use](https://registry.terraform.io/terms).
