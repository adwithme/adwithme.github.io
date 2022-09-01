---
layout: post
title: SSLVPN On SOPHOS XG Firewall
subtitle: What is SSLVPN and How to Configure.
cover-img: /img/posts/Firewall/sophos-xg.png
thumbnail-img: /img/posts/Firewall/sophos-xg.png
share-img: /img/posts/Firewall/sophos-xg.png
tags: [Firewall, Security]
---
### What Is SSL VPN?

SSL VPNs arose as a response to the complexity of the Internet Protocol security (IPsec) framework, and the inability to support every end user—particularly remote users—from every platform available. An SSL VPN generally provides two things: secure remote access via a web portal, and network-level access via an SSL-secured tunnel between the client and the corporate network. The primary benefit of an SSL VPN is data security and privacy.

![Firewall](/img/posts/Firewall/Firewall-Structure.png)

### Why SSL VPN ?
With the growth of the remote workforce, SSL VPNs are critical to keeping employees connected to the work applications they need—and for IT to ensure that only authorized users gain access. SSL VPNs provide a secure way for your workforce, contractors, and partners worldwide to gain access to sensitive information from virtually any computer or device. Furthermore, they give IT full, granular control over data access. SSL VPNs are becoming more common in the workplace, and the learning curve to implement and use them is minimal.

**Let’s Check out the process of configuration.**

### 1. Define SSL VPN Users And Group
#### Groups
Go to Authentication --> Group-->Add 

Create a Group Named SSLVPN

Under Policies

Surfing Quota give Unlimited internet Access

Access Time Allowed all the time

Click on Save

#### Users

Again Click on User --> Add

Create a user 

Choose User Type and its password and email

Group choose SSLVPN Group

and click on save

_Here, you have successfully created a User and Group for SSL VPN_

### 2. Define Local Subnet And Remote SSLVPN Range.

Go to Host and Services --> Click on Add

Enter Host Name SSLVPN Network

Choose Type --> Network

Define IP address _(IP address must be different than your local network because this IP address is used by SSLVPN User for connection)_

### 3. Define remote SSL VPN Policy

Go to VPN

Click on SSL VPN (Remote Access)  add

Enter Name SSLVPN Remote

Policy member --> Select SSLVPN Group

Permitted Network Resource --> Select SSL VPN network

Click on Save


### 4. Verifying the authentication services for SSLVPN

Go to Authentication --> Services

Check all Option that all are in Local. And apply

### 5. Verifying the Allowed Zones for SSL VPN

Go to Network

Edit Wan and check SSLVPN Tunnel and user portal is enabled and click on save

Go to Administration 

Click on device Access

Enable Lan, Wan and DMZ under SSL VPN.

### 6. Configure Advance SSLVPN Setting

Go to VPN

Click on Show VPN Setting on top right corner.

Enter Lease range ad save

_Note: - You must be entering lease range must be from SSL VPN Network._



### 7. Create firewall Rule

Go to Rules and Policies

Add firewall rule--> New firewall rule

Enter Rule Name VPN to LAN

Action Accept

Source

Source Zone:- VPN

Source Network and devices:-  SSL VPN

During Schedule:-  time all the time

Destination and services.

Destination zones:- Lan

Destination network:- VPN Network

Services:- Any

User or group 

Choose SSL VPN Group

Disable Nat and routing

Click on Save

## Your Configuration Is Completed Now Time To Check It Is Working Or Not.

Go to your browser

Type https://youripadress:443 and hit enter.

Type user name and password for User

Download Software and install
