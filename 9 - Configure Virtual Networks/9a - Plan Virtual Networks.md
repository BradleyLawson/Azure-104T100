# Plan Virtual Networks in Azure

**Objective:** Understand the importance of planning virtual networks in Azure and the key components and considerations involved.

## Introduction

One of the primary advantages of adopting cloud solutions like Azure is the ability to transition server resources to the cloud. This move not only saves costs but also simplifies administrative operations by eliminating the need for maintaining on-premises datacenters with complex infrastructure.

## Components of Azure Network Services

Azure network services provide a range of components with various functionalities and capabilities, including:

![Screenshot that shows the main components of Azure network services.][https://learn.microsoft.com/en-us/training/wwl-azure/configure-virtual-networks/media/network-components-66dff480.png]

## Key Aspects of Azure Virtual Networks

Here are some essential characteristics of Azure virtual networks:

- **Logical Isolation**: Azure Virtual Network is a logical isolation within the Azure cloud dedicated to your subscription.

- **VPN Provisioning**: Virtual networks can be used to provision and manage virtual private networks (VPNs) in Azure.

- **CIDR Blocks**: Each virtual network has its own Classless Inter-Domain Routing (CIDR) block and can be linked to other virtual networks and on-premises networks.

- **Hybrid Solutions**: Virtual networks can be linked to on-premises IT infrastructure, creating hybrid or cross-premises solutions, even when CIDR blocks don't overlap.

- **DNS Control**: You have control over DNS server settings and the segmentation of the virtual network into subnets.

## Scenarios for Using Virtual Networks

Consider these scenarios when planning your virtual networks and subnets:

- **Dedicated Private Cloud**: Create a dedicated private cloud-only virtual network for scenarios where cross-premises connectivity isn't required. Services and virtual machines within this network can communicate securely in the cloud.

- **Secure Data Center Extension**: Extend your data center securely using site-to-site VPNs, which use IPSEC to provide a secure connection between your corporate VPN gateway and Azure.

- **Hybrid Cloud**: Virtual networks enable a variety of hybrid cloud scenarios, allowing secure connections between cloud-based applications and on-premises systems, including mainframes and Unix.

![Diagram of a virtual network with a subnet of two virtual machines. The network connects to an on-premises infrastructure and a separate virtual network.](<diagram-url>)

It's essential to carefully plan your virtual network configuration to align with your specific requirements and use cases in Azure.


[https://learn.microsoft.com/en-us/training/wwl-azure/configure-virtual-networks/media/network-components-66dff480.png]: <screenshot-url>