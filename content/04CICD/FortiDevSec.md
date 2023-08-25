---
title: "Working with FortiDevSec"
menuTitle: "FortiDevSec"
weight: 90
---

SAST testing with FortiDevSec is integrated with Jenkins to test our GitHub repo code.

For access to the FortiDevSec console, please email FortinetCloudCSE@fortinet.com.

Once you've received an IAM username, to log in, navigate to [https://fortidevsec.forticloud.com/devsec-home](https://fortidevsec.forticloud.com/devsec-home), and click 'Login' at the top right of the screen.

![fds-login-1](fds-login-1.png)

At the next screen, click 'IAM LOGIN', and enter the Account ID and username that you should have received from FortinetCloudCSE@fortinet.com.

![fds-iam-login](fds-iam-login.png)

This will take you to the FortiDevSec console, where you can view all applications within the organization.

![fds-console-1](fds-console-1.png)

Click on an application to view scans performed.

![fds-app-click](fds-app-click.png)

This screen displays all of the various scans performed on the application including the number of vulnerabilities in each scan and it's risk score. Click 'View All' to see a list of all vulnerabilities.

![fds-scan-list](fds-scan-list.png)

On this screen, you can filter by risk rating, status, category, etc.

![fds-vuln-list](fds-vuln-list.png)

Click on a scan to list vulnerabilities only associated with that scan.

![fds-click-js](fds-click-js.png)

Click on a vulnerability to view more information on that specific vulnerability.

![fds-click-vuln](fds-click-vuln.png)

The modal that appears will display information useful for remediation including file location, Git commit ID, branch, and first and last appearance date/time. 

![fds-vuln-modal-1](fds-vuln-modal-1.png)

Scrolling down within the modal will display CWE, OWASP, and SANS information as well as other occurrences of the vulnerability within the repo. 

![fds-vuln-modal-2](fds-vuln-modal-2.png)
