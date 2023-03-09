# Lab: Network Traffic Analysis with Wireshark

## Overview

The Kali Linux distribution includes a plethora of offensive security software tools that you will find useful in this course. Wielded by pentesters, ethical hackers, forensics investigators, and enthusiasts, Kali Linux is the popular go-to weapon for performing all manner of cyber attacks. Today you will use one of its most (in)famous tools: Wireshark.

Wireshark is capable of network traffic analysis, and is generally regarded as a computer forensics tool for its ability to "zoom in" and scrutinize network traffic at the lowest level.

## Scenario

GlobeX is currently contracted with a MSSP (Managed Security Service Provider), Secutronix, to perform a security evaluation of the various IT systems you've recently implemented. As part of the security evaluation, the MSSP has requested a sample of network traffic of a computer on the LAN viewing the [CERN website](http://info.cern.ch/). "Terrible timing! Our network analyst is out of the office this week," the MSSP rep, Sarah, explains. "If you could fill out the audit form for us this one time, that would keep everyone's timelines in track. Sorry to ask this of you!"

## Objectives

- Using Wireshark on Kali Linux, create a PCAP file consisting of an HTTP GET request to the CERN website.
- In Wireshark, filter your view to only HTTP traffic from Kali to this site.
- Perform an analysis of both the TCP and HTTP traffic.
- Export the capture as a PCAP file.

## Resources

- [Wireshark](https://www.wireshark.org/){:target="_blank"}
- [Wireshark Cheat Sheet](https://www.comparitech.com/net-admin/wireshark-cheat-sheet/)
- [Kali Linux](https://www.kali.org/downloads/){:target="_blank"}
- [Netgate Forums for pfSense Discussion & Support](https://forum.netgate.com/){:target="_blank"}

## Tasks

### Part 1: Deploy Kali Linux

For this lab, all you'll need on the VirtualBox LAN is Kali Linux deployed behind the pfSense firewall.
- Using the installer ISO file, deploy Kali Linux.
- Verify internet connectivity on Kali Linux.

### Part 2: Traffic Capture

Perform a live capture of your ethernet device.
- Launch Wireshark as root.
- Select the network adapter that is displayed, note this may have different labels.
  - You may see `Eth0`, `Ensp03`, `Eth1` etc.
  - Don't worry about the name of the adapter as different versions of virtualization software will name the adapter differently.
- On the same computer, browse to the target website and perform an HTTP GET request.
- Halt the capture. Take am moment to review the packets that were captured.
- What is the difference between the various colors of packets that you see?

### Part 3: TCP Analysis

Analyze the TCP segments. Answer the following questions:

  - How many segments are used here?
  - What is the length in bytes of each segment? (Remember: The segment length is the size of the data contained in the packet)
  - Can you identify all three packets involved in the TCP three-way handshake? Include a screencap of them.
  - How much data is typically acknowledged per ACK?

### Part 4: HTTP Analysis

- Filter traffic to HTTP from source Kali Linux to destination CERN. Include a screenshot of the filtered view.
- Locate the GET method that precedes a series of HTTP headers.
- Look for the following common HTTP headers and include them if in your response if you can find them:
  - Host
  - User-Agent
  - Accept, Accept-Encoding, Accept-Charset, Accept-Language
  - Cookie
  - Cache-Control

### Part 5: Wrapup

When you are finished, save a PCAP file of the network traffic capture for future reference.

Search your favorite job site, such as [Indeed](https://www.indeed.com/){:target="_blank"}, for the keyword "wireshark."

  - What did you find?
  - Why is network traffic analysis a relevant skill to have?
  - Do you see yourself working in this type of job in the future?

> Enjoy the lab today? You may wish to investigate a career as a [digital forensics investigator](https://computer.howstuffworks.com/computer-forensic.htm){:target="_blank"}.

## Submission Instructions

1. Create a new blank Google Doc. Include above assignment submission text and images within this Google Doc.
1. Name the document according to your course code and assignment.
   - i.e. `seattle-ops-201d1: Lab 04`.
1. Add your name & date at the top of the Google Doc.
1. Share your Google Doc so that "Anyone with the link can comment".
1. Paste the link to your Google Doc in the discussion field below and share an observation from your experience in this lab.
