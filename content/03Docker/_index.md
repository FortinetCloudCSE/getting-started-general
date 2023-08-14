---
title: "Working with Docker"
chapter: false
menuTitle: "Working with Docker"
weight: 60
---

Docker is a widely-used containerization technology. It is used to run FortiDevSec and FortiDAST scans, which you may want to run locally to gain a view
into the security risks present in your project. 

For information on how we are using Docker in Workshop development, please see the TecWorkshop template [here](https://fortinetcloudcse.github.io/UserRepo/index.html).

To begin working with Docker, you'll need to download a container management platform. Rancher Desktop is suggested for its ease of installation and ease of use. 

### WSL Installation on Windows

If you're on Windows, the Windows Subsystem for Linux is suggested. To install WSL, you can open Powershell as an administrator and run:

```shell
wsl --install
```

For more information on WSL installation, please see the official Microsoft documentation here: [WSL Documentation](https://learn.microsoft.com/en-us/windows/wsl/)

Once WSL is installed, you can type 'Ubuntu' into the search box at the bottom of your desktop and then, once the Ubuntu icon appears, click it to open the CLI. 

### Rancher Desktop

Rancher Desktop installation instructions can be found in the offical Rancher Desktop documentation here: [Rancher Desktop Installation Instructions](https://docs.rancherdesktop.io/getting-started/installation/)

Once you've successfully installed Rancher, you'll need to configure it for use with WSL. Type 'Rancher Desktop' into your Windows search bar at the bottom of the screen, and once the icon appears, click it. You should see the following window appear.

![rancher-1](rancher-1.png)

Click 'File', then 'Preferences', and select 'WSL' on the left side of the window that appears, and ensure the desired version of WSL you will be working with is checked.

![rancher-2](rancher-2.png)

Then, click 'Apply'.

At the WSL command line, type 'docker images'. You should see a list of docker images installed by and associated with Rancher. If you are able to successfully run this command, your installation should be good to go.

```shell
>docker images
REPOSITORY                                          TAG                    IMAGE ID       CREATED         SIZE
rancher/klipper-lb                                  v0.4.4                 af74bd845c4a   2 months ago    12MB
rancher/klipper-helm                                v0.8.0-build20230510   6f42df210d7f   3 months ago    262MB
rancher/mirrored-library-traefik                    2.9.10                 d1e26b5f8193   4 months ago    138MB
rancher/local-path-provisioner                      v0.0.24                b29384aeb4b1   4 months ago    40.1MB
rancher/mirrored-metrics-server                     v0.6.3                 817bbe3f2e51   4 months ago    68.9MB
rancher/mirrored-coredns-coredns                    1.10.1                 ead0a4a53df8   6 months ago    53.6MB
rancher/mirrored-library-busybox                    1.34.1                 827365c7baf1   7 months ago    4.86MB
rancher/mirrored-pause                              3.6                    6270bb605e12   24 months ago   683kB
ghcr.io/rancher-sandbox/rancher-desktop/rdx-proxy   latest                 3e9d7c4baf05   292 years ago   5.1MB
```

