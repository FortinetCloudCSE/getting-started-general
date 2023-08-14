---
title: "CI/CD Tooling"
chapter: false
menuTitle: "CI/CD Tooling"
weight: 70
---

In order to maintain a workable state for our repositories, before merging a branch, various tests may run on your branch to ensure it meets certain standards having to do with code quality and security. The tests will need to pass in order for the branch to be merged to the main repository branch.

Current/future tests may include:

* FortiDevSec Security Scans ([documentation](https://docs.fortinet.com/product/fortidevsec/23.2))
* Linters for Infrastructure as Code
  * [tflint](https://github.com/terraform-linters/tflint)
  * [cfn-lint](https://github.com/aws-cloudformation/cfn-lint)

These tests will run on our Jenkins server hosted in AWS. The Jenkins URL is [https://jenkins.fortinetcloudcse.com:8443](https://jenkins.fortinetcloudcse.com:8443). To get a user account, email FortinetCloudCSE@fortinet.com.

