# Lab: Configuring and Monitoring Ports and Protocols

## Overview

The network mapping tool Nmap is an open source, command line utility commonly used in network discovery ("enumeration" in offensive terms), security auditing, and pentesting. Nmap can audit whether ports are open or closed on a target host.

Today you will perform basic scanning operations in Nmap. You'll also be configuring your DNS server to change the destination of a given domain.

## Resources

- [Nmap Manual](https://nmap.org/book/man.html){:target="_blank"}
- [Nmap Cheat Sheet](https://www.comparitech.com/net-admin/nmap-nessus-cheat-sheet/){:target="_blank"}
  - [Nmap Cheat Sheet PDF](https://cdn.comparitech.com/wp-content/uploads/2019/06/Nmap-Cheat-Sheet.pdf){:target="_blank"}

## Requirements

### Part 1: Preparing a Network Environment and Staging Kali Linux

**IMPORTANT: Restrict the scope of your scans to hosts that are on your own network or targets that you have permission to scan.**

First, prepare a suitable network environment by placing 2-3 different hosts together, either on the the same Host-only network with a pfSense router, or on the same NAT Network (without a pfSense router. 
- Ideally, choose VMs with different OSs and/or different configurations (such as a Windows 10 host, an Ubuntu Server, and a pfSense router).
- These will be your targets today.

Create a new Kali Linux install Virtual Machine, and place it on the same network.

Kali Linux comes bundled with Nmap already installed, and can be accessed by using the `nmap` command in Kali's terminal.

### Part 2: Port Scanning with Nmap

Let's get some practice using Nmap by performing a series of scans (described below).

For each scan:
- Output the results of the command into a file.
- Include in your lab write-up:
  - A screenshot of the output of the command.
    - Hint: Use the `cat` command to print the contents of a file to the terminal, or open the file in Kali's built-in text editor.
  - The exact command you used.
- Answer the following questions:
  - What does this scan do in technical terms?
  - Was the scan correct?
  - Why/why not?
  - Why would you perform this particular scan?

On the local network shared by Kali and your target VMs:
- Perform a scan to discover all hosts on , without scanning any ports.
- Perform a fast, aggressive scan of the network.
- Scan the 1000 most common ports on each host on the network.
- Perform an intense scan on all hosts on the network.
- Perform a slow, comprehensive scan on all hosts on the network. 

> If your local target is yielding inadequate results, try changing your Kali VM's network settings to Bridged and use `nmap` to target `scanme.nmap.org`, which is a test host provided by Nmap for this very purpose.

### Part 3: Reporting Nmap Findings

Compile your Nmap findings in an organized fashion.

- Create a **Scans Performed** table with three columns: `Scan Type`, `Scan Results`, `Actual`.
  - Populate the table with your results.
- Create a **Service Enumeration** table with three columns: `Server IP Address`, `Ports Open`, and `Service/Banner`.
  - Populate the table with your results.
  - Indicate above the table your network range with CIDR block notation.

> **FOR EXAMPLE:**
>
> Network Range: 192.168.1.0/24
> | Server IP Address | Ports Open | Service/Banner |
> |-------------------|------------|----------------|
> | 192.168.1.1       | 52         | domain         |
> |                   | 80         | http           |
> | 192.168.1.11      | 22         | ssh            |
> |                   | 25         | smtp           |


### Part 4: Protocol Hierarchy Statistics with Wireshark

Let's explore some protocol-related capabilities of Wireshark in Kali Linux.

- In Wireshark, generate a Protocol Hierarchy Statistics report. Include a screenshot.
- Which hosts are the top talkers and listeners on this link? Check the `Statistics > Endpoints` menu.
- Select Close and then select `Statistics > Conversations`. Sort this by session duration and include a screenshot.

### Part 5: Netstat

`Netstat` can reveal port and service information on a Windows host. Include screenshots (or copied text) of your entered command and the output for the following on a Windows VM:

- From a terminal prompt, run a `netstat` command that shows all active ports.
- Run a `netstat` command that displays the routing table.
- Run a `netstat` command that only displays connections for the TCP protocol.


## Stretch Goals

If you're comfortable enough in Wireshark to start some analysis work of other protocols try the steps below.

- Establish a connection from Kali to another host using FTP.
- Send cleartext data over the wire, then use Wireshark to capture the FTP traffic.
- Was the capture attempt successful? Journal your attempts and findings in your submission today.

## Submission

1. Create a new blank Google Doc. Include above assignment submission text and images within this Google Doc.
1. Name the document according to your course code and assignment.
   - i.e. `seattle-ops-201d1: Lab 04`.
1. Add your name & date at the top of the Google Doc.
1. Share your Google Doc so that "Anyone with the link can comment".
1. Paste the link to your Google Doc in the discussion field below and share an observation from your experience in this lab.
