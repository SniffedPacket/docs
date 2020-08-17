---
title: Overview
author: Cumulus Networks
weight: 5
product: Cumulus VX
version: '3.7'
---
This section provides an overview of Cumulus VX and lists the supported environments.

## Cumulus VX

Cumulus VX is a virtual appliance that helps you become familiar with Cumulus Networks technology, and provides a platform for you to prototype network operations and develop custom applications before you deploy into a production environment. Without the need for a bare metal switch or specialized hardware, Cumulus VX runs on all popular hypervisors, making traditional networking protocols such as BGP and MLAG, Cumulus Networks-specific technologies such as ONIE, and Prescriptive Topology Manager (PTM) available for testing and configuration.

Cumulus VX runs in a virtual machine (VM) on a standard x86 environment. The VM is a 64-bit operating system, built on the same foundation as {{<exlink url="https://docs.cumulusnetworks.com/cumulus-linux" text="Cumulus Linux">}}, and runs Debian Linux with `virtio` drivers for network and HDD interfaces as well as the logical volume manager (LVM). Cumulus VX includes all the control plane elements without an actual ASIC or NPU for line rate performance or hardware acceleration.

{{< img src="/images/cumulus-vx/cumulus-vx.png" width="800" >}}

## Cumulus in the Cloud

As an alternative to Cumulus VX, which requires a hypervisor (or hypervisor and orchestrator), you can use
{{<exlink url="https://cumulusnetworks.com/products/cumulus-in-the-cloud/" text="Cumulus in the Cloud">}}, which is a free, personal, virtual data center network that provides a low-effort way to see Cumulus Networks technology in action. Your virtual data center consists of two racks with two dual-homed servers connected with a leaf-spine network. This is a good way to try out Cumulus Linux if you have platform or disk limitations.

## Supported Environments

Cumulus VX is supported on:

- KVM-QEMU
- KVM-QEMU and Vagrant
- VirtualBox
- VirtualBox and GNS3
- VirtualBox and Vagrant
- VMware Fusion, Worksation, and vSphere ESXi

{{%notice note%}}

Although Cumulus VX is supported on VMware Fusion, Workstation, and vSphere ESXi. This document provides setup instructions for VMware vSphere ESXi only.

{{%/notice%}}

## Cumulus VX Compared with Cumulus Linux

Cumulus VX is not a production-ready virtual switch or router. It has the same foundation as Cumulus Linux, including all the control plane elements, but without an actual ASIC or NPU for line rate performance or hardware acceleration.

| Cumulus VX | Cumulus Linux |
| -----------| ------------- |
| {{< img src="/images/cumulus-vx/cumulus-vx.png" width="450" >}}| {{< img src="/images/cumulus-vx/cumulus-linux.png" width="450" >}}|

You can use tools like `jdoo` to monitor the virtual switch. The same automation, zero touch provisioning, security, and QoS tools are available.

The following table outlines the similarities and differences between Cumulus VX and Cumulus Linux:

| <div style="width:300px">Feature or Functionality | Cumulus VX |
| ------------------------ | -------------------------------- |
| Installation and Upgrade | New images available with every GA release. |
| Hardware acceleration    | Datapath forwarding is dependent on the choice of hypervisor and VM resources. |
| Hardware management      | None |
| Hardware limitations     | None. Dependent on hypervisor and VM resources. Certain features such as route-table-size might accommodate more routes than are supported in hardware (32K routes), given available memory. |
| Production-ready         | No |
| Linux extensibility      | Yes |
| Layer 2 features         | Yes; hypervisor/topology manager dependent. |
| Layer 3 features         | Yes |
| Network virtualization   | Yes (software forwarding) |
| OS management (ZTP, ifupdown2, third party packages) | Yes |
| Automation, monitoring, troubleshooting | Yes |
| Security                 | Yes |
| QoS                      | Yes |

## Support Policy

As a Cumulus Linux customer, you can receive formal GSS support for Cumulus VX instances to:

- Test and stage network topologies before deploying to production.
- Analyze, troubleshoot, and correct issues with configurations and software bugs in Cumulus VX that might also apply to Cumulus Linux running on physical devices.
- Analyze, troubleshoot, and correct issues with Cumulus VX if behaving differently than physical devices. This does not apply in scenarios where it is not possible to emulate physical hardware with virtualization.

Cumulus Networks does *not* provide support for:

- Cumulus VX instances used in a production environment.
- Virtualization environments, including installation, setup, and configuration.
- Automation tool playbooks, including creation and troubleshooting.
- Performance or scalability issues related to network traffic running through Cumulus VX instances.

For non-customers, Cumulus VX remains a community-supported product, with no formal support obligations from Cumulus Networks. You can submit questions to the {{<exlink url="https://slack.cumulusnetworks.com/" text="community Slack channel">}} to engage with the wider community.

## Related Information

- {{<exlink url="https://docs.cumulusnetworks.com/cumulus-linux" text="Cumulus Linux documentation">}}
- {{<exlink url="https://cumulusnetworks.com/products/cumulus-vx/download/" text="Cumulus VX downloads">}}
- {{<exlink url="https://www.vmware.com/support/pubs/" text="VMware documentation">}}
- {{<exlink url="https://www.virtualbox.org/wiki/Documentation" text="VirtualBox documentation">}}
- {{<exlink url="http://www.linux-kvm.org/page/Documents" text="KVM documentation">}}
- {{<exlink url="https://docs.vagrantup.com/v2/" text="Vagrant documentation">}}
- {{<exlink url="https://www.gns3.com/software" text="GNS3 documentation">}}
