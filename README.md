# Enterprise Secure Wireless Network Design

## Overview

This project presents a secure enterprise wireless network design for a small business environment. The goal was to replace a vulnerable residential-grade wireless setup with a more secure, scalable, and professional network architecture using enterprise wireless security practices.

The design focuses on WPA3 wireless encryption, VLAN-based network segmentation, guest network isolation, management network separation, wireless coverage planning, and post-implementation validation. The project demonstrates practical knowledge of networking, wireless security, infrastructure planning, and IT documentation.

---

## Problem

The existing network relied on a residential-grade wireless router, creating several security and performance risks:

* Guest users and internal business devices shared the same broadcast domain.
* Sensitive business and client data could be exposed to unauthorized users.
* The wireless network lacked enterprise-grade encryption and segmentation.
* Administrative access to network devices was not properly separated.
* Wireless coverage and performance were not formally validated.

For a small business handling internal communications and client information, this type of setup increases the risk of unauthorized access, lateral movement, data exposure, and unreliable connectivity.

---

## Proposed Solution

The proposed solution was to design a secure enterprise-style WLAN using dedicated networking hardware, stronger encryption, and logical segmentation.

Key design components include:

* WPA3-SAE encryption for secure wireless authentication
* Separate business and guest wireless networks
* VLAN segmentation to isolate internal, guest, and management traffic
* Management VLAN for administrative access to network devices
* Enterprise-grade wireless access points
* Security gateway/firewall rules to prevent unauthorized cross-VLAN communication
* Wireless coverage planning to eliminate dead zones
* Post-implementation validation through signal testing, speed testing, and security checks

---

## Network Architecture

The network is designed around logical separation of traffic. Instead of allowing all devices to communicate on one flat network, each type of traffic is placed into its own VLAN.

### VLAN Design

| VLAN            | Purpose                   | Description                                                                 |
| --------------- | ------------------------- | --------------------------------------------------------------------------- |
| Business VLAN   | Internal business devices | Used for trusted company laptops, desktops, and internal resources          |
| Guest VLAN      | Visitor internet access   | Provides internet access while blocking communication with internal systems |
| Management VLAN | Network administration    | Restricts access to gateway, switch, and access point management interfaces |

This design reduces the risk of unauthorized access and limits lateral movement if a guest or unmanaged device is compromised.

---

## Security Features

### WPA3 Wireless Security

The primary business SSID is designed to use WPA3-SAE encryption. WPA3 provides stronger protection than older wireless security standards and helps defend against credential-based wireless attacks.

### Guest Network Isolation

Guest users are placed on a dedicated guest VLAN. Firewall rules prevent guest devices from communicating with internal business devices while still allowing internet access.

### Management VLAN

Administrative interfaces for the gateway, switches, and access points are placed on a separate management VLAN. This prevents normal users or guest devices from accessing device management portals.

### Firewall and Access Control

Security gateway rules are designed to block unauthorized traffic between VLANs while permitting only required traffic for business operations.

### Wireless Coverage Planning

Wireless access point placement is planned to provide full office coverage and eliminate dead zones. Signal strength is validated using a post-installation signal heat map.

---

## Implementation Plan

The project follows a structured implementation approach:

1. **Requirements Gathering**

   * Identify office layout
   * Determine number of users and devices
   * Define security and performance requirements

2. **Network Design**

   * Plan VLAN structure
   * Define SSIDs
   * Select enterprise-grade networking hardware
   * Map access point placement

3. **Lab Pre-Configuration**

   * Configure gateway, VLANs, SSIDs, and access points before deployment
   * Test VLAN tagging and security settings
   * Reduce business downtime during installation

4. **Physical Deployment**

   * Install gateway and wireless access points
   * Validate signal coverage throughout the office
   * Adjust access point placement and power levels if needed

5. **Security and Performance Validation**

   * Confirm WPA3 encryption
   * Test guest/internal VLAN isolation
   * Verify administrative access restrictions
   * Run speed and latency testing
   * Document final configuration

---

## Validation Criteria

The project is considered successful when the following criteria are met:

| Requirement       | Success Criteria                                                                     |
| ----------------- | ------------------------------------------------------------------------------------ |
| Wireless Security | Business SSID uses WPA3-SAE encryption                                               |
| Network Isolation | Guest VLAN cannot communicate with internal business VLAN                            |
| Coverage          | Full office coverage with no major dead zones                                        |
| Performance       | Network supports 10–15 concurrent users without major latency or connectivity issues |
| Administration    | Management interfaces are isolated from guest and standard user traffic              |
| Documentation     | Network topology, security settings, and validation results are documented           |

---

## Project Artifacts

This repository may include the following supporting materials:

```text
enterprise-wlan-design/
│
├── README.md
│
├── images/
│   ├── vlan-topology.png
│   ├── signal-heatmap.png
│   └── network-architecture.png
│
└── docs/
    └── project-summary.pdf
```

Recommended visuals:

* VLAN topology diagram
* Wireless signal heat map
* Network architecture diagram
* Firewall rule summary
* Implementation checklist

---

## Skills Demonstrated

This project demonstrates hands-on knowledge of:

* Network design
* Wireless networking
* VLAN segmentation
* WPA3 security
* Guest network isolation
* Management VLAN design
* Firewall rule planning
* DNS/DHCP concepts
* Network documentation
* Infrastructure planning
* Security validation
* Troubleshooting and performance testing

---

## Technologies and Concepts

| Category             | Tools / Concepts                                     |
| -------------------- | ---------------------------------------------------- |
| Wireless Security    | WPA3-SAE                                             |
| Network Segmentation | VLANs, 802.1Q tagging                                |
| Security Controls    | Firewall rules, access control, guest isolation      |
| Infrastructure       | Gateway, switches, wireless access points            |
| Validation           | Signal heat maps, speed tests, latency checks        |
| Documentation        | Network topology, support guide, implementation plan |

---

## Lessons Learned

This project reinforced the importance of designing networks with security and scalability in mind from the beginning. A flat network may be simple to deploy, but it creates unnecessary risk by allowing guest and internal traffic to exist in the same broadcast domain.

Key lessons learned:

* VLAN segmentation is one of the highest-value controls for small business network security.
* Guest Wi-Fi should never share the same network as internal business devices.
* Management interfaces should be isolated from standard user traffic.
* Wireless coverage should be validated with signal testing, not assumptions.
* Security and performance must both be tested before considering a deployment complete.
* Strong documentation makes a network easier to maintain, troubleshoot, and improve.

---

## Future Improvements

Potential future improvements include:

* Add a full firewall rule table
* Add a packet capture demonstration showing blocked cross-VLAN traffic
* Add DHCP scope examples for each VLAN
* Add sample switchport configuration
* Add a simulated lab implementation using Cisco Packet Tracer, UniFi, Omada, or pfSense
* Add monitoring with logs, alerts, and uptime checks
* Add a network hardening checklist based on industry best practices

---

## Why This Project Matters

Small businesses often rely on simple consumer-grade networking equipment, but that can create serious security and reliability issues. This project shows how enterprise networking principles can be applied in a practical, small-business environment.

By combining WPA3 encryption, VLAN segmentation, guest isolation, management separation, and validation testing, this design provides a more secure and scalable foundation for business connectivity.

---

## Author

**Uwais Watkins**
Information Technology Professional
GitHub: [waisyrr](https://github.com/waisyrr)
LinkedIn: [Uwais Watkins](https://www.linkedin.com/in/uwais-watkins/)
Email: [uwatki1@gmail.com](mailto:uwatki1@gmail.com)
