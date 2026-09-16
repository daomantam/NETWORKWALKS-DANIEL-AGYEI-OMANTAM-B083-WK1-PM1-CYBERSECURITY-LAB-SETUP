# NETWORKWALKS-DANIEL-AGYEI-OMANTAM-WK1-PM1-CYBERSECURITY-LAB-SETUP

## Introduction

This project involved setting up a cybersecurity laboratory environment using
Kali Linux in VirtualBox.

The purpose of the lab was to create a controlled environment for learning
and practicing cybersecurity concepts and techniques.

## Lab Environment

- Host Operating System: Windows
- Virtualization Software: VirtualBox
- Virtual Machine: Kali Linux
- Network Interface: eth0

## Objectives

The objectives of this project were to:

- Set up a Kali Linux virtual machine using VirtualBox.
- Configure the Kali Linux network connection.
- Verify that the network interface is operational.
- Check the IP address assigned to the network interface.
- Test connectivity to the local gateway.
- Test external network connectivity.


## Setup Process

### Step 1: Install Required Software

The required software for the lab environment was downloaded and installed:

- 7-Zip
- VirtualBox
- Kali Linux

VirtualBox was used as the virtualization platform, while Kali Linux was set up as the cybersecurity testing machine.


### Step 2: Configure the VirtualBox Network

A NAT Network was configured in VirtualBox using the subnet:

10.0.0.0/24

The NAT Network was used to allow the Kali Linux virtual machine to communicate within the lab network while maintaining Internet connectivity.

<img width="901" height="337" alt="Screenshot 2026-09-16 102847" src="https://github.com/user-attachments/assets/75e10270-8eba-491f-b86a-e7ab06fe5317" />


### Step 3: Import Kali Linux

Kali Linux was downloaded and imported into VirtualBox as a virtual machine.

Kali Linux was configured as the attacking/testing machine for the cybersecurity lab.

<img width="504" height="152" alt="Screenshot 2026-09-16 105425" src="https://github.com/user-attachments/assets/a80a00fd-5308-4745-8cae-c9894ec04b3f" />


### Step 4: Configure Kali Linux IP Address

The Kali Linux network interface was configured with the following settings:

| Setting | Configuration |
|---|---|
| Network Interface | eth0 |
| IP Address | 10.0.0.2/24 |
| Gateway | 10.0.0.1 |

The network interface was checked using:
"nmcli device status"

<img width="1920" height="963" alt="image" src="https://github.com/user-attachments/assets/2f095587-375a-4aaf-b326-30963bd11361" />


### Step 5: Verify Network Connectivity

Network connectivity was tested from the Kali Linux virtual machine.

First, connectivity to the local gateway was tested using:
"ping -c 4 10.0.0.1"

Internet connectivity was then tested using:
"ping -c 4 8.8.8.8"


### Step 6: Create a VirtualBox Snapshot

After completing the initial Kali Linux configuration and verifying network
connectivity, a VirtualBox snapshot was created to preserve the working state
of the virtual machine.

The snapshot was named:
Daniel Agyei Omantam WK1 Snapshot
<img width="923" height="77" alt="Screenshot 2026-09-16 132608" src="https://github.com/user-attachments/assets/1957bbbc-d5f2-4dfb-9275-e14f52beef1a" />


## Additional VM Settings

The VirtualBox virtual machine settings were configured to allow
communication between the host operating system and the Kali Linux virtual
machine.

| Setting | Configuration |
|---|---|
| Shared Clipboard | Bidirectional |
| Drag'n'Drop | Bidirectional |

### Shared Folder Configuration

A VirtualBox shared folder was configured and mounted in Kali Linux at:
/downloads

The mount was verified using:

mount | grep -i vbox

## Troubleshooting

During the network configuration process, the Kali Linux network interface
initially had difficulty obtaining the required IP configuration.

The "eth0" interface was checked using:

"nmcli device status"

And the IP configuration was checked using:
"ip addr show eth0"

After troubleshooting and reactivating the network connection, the interface
became connected and was assigned the required IP address:

"10.0.0.2/24"

Connectivity was then verified using the local gateway:
"ping -c 4 10.0.0.1" and an external ip address: "ping -c 4 8.8.8.8"

## Troubleshooting Outcome

The network configuration was successfully restored, allowing the Kali Linux
virtual machine to communicate with the local lab network and access the
Internet.


## Conclusion

The cybersecurity laboratory environment was successfully set up using
VirtualBox and Kali Linux.

The Kali Linux virtual machine was configured with the required network
settings, including the "10.0.0.2/24" IP address and "10.0.0.1" gateway.
Network connectivity was successfully verified, and the "/downloads" shared
folder was configured and mounted.

A VirtualBox snapshot was also created to preserve the working state of the
lab environment.

The lab environment is now ready for the next stage of the cybersecurity
training.
