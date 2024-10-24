
# Katharà Lab for Cybersecurity Simulation

## Overview

This `.zip` file contains two folders:

1. **Katharà Lab Folder:** This contains the actual Katharà lab configuration.
2. **Dockerfile Folder:** This folder contains a Dockerfile I used to create a customized Kali Linux image. 

### Custom Kali Linux Image
I needed a Kali Linux image that included tools such as Metasploit, `smbclient`, and other networking utilities that were not present in the base image (`kalilinux/kali-rolling`). The Dockerfile helps create this customized image with the required tools.

### Lab Structure
The lab consists of two PCs:
- One PC runs the `cyberacademy/metasploitable2` image, representing a vulnerable system.
- The other PC runs the customized Kali Linux image described above, acting as the attacker.

Additionally, I have included a third host in the lab running Wireshark, which can be used to monitor the network traffic exchanged between the attacker and the target.

### Core Functionality
The heart of the lab lies in two scripts:

- **Kali Linux Container:** Contains the script with the exploits to execute.
- **Metasploitable Container:** Contains the script with the countermeasures to implement.

Both scripts are structured into functions, with each function responsible for executing a specific attack or countermeasure. Additionally, both scripts feature a menu interface that allows the user to select which attack or defense to run.

---

### How to Use

1. **Setting Up the Lab:** 
   - Unzip the file and follow the standard Katharà lab setup procedure.

2. **Running the Custom Kali Image:** 
   - Use the provided Dockerfile to build the custom Kali Linux image. The Kali container will include all necessary tools such as Metasploit and `smbclient`.

3. **Executing Attacks and Countermeasures:**
   - Once the lab is running, interact with the menus within the scripts on each container. The menu allows you to choose specific attacks (on the Kali Linux container) and defenses (on the Metasploitable container).

4. **Network Traffic Analysis:**
   - If you wish to monitor network activity, the Wireshark host is available to inspect the packets exchanged during the simulation.

---

### Requirements

- **Katharà** environment set up and running.
- **Docker** for building the custom Kali Linux image.
- Familiarity with basic Linux commands and Katharà usage.

---

### Notes
This lab is designed to simulate both offensive and defensive aspects of cybersecurity in a controlled environment. It provides a hands-on way to explore attack vectors and the corresponding defenses using real tools such as Metasploit.

---
