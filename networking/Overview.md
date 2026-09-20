# Deploying NGINX on AWS EC2 with a Custom Domain

## Overview

For this project, I deployed an NGINX web server on an AWS EC2 instance and connected it to a custom domain using Cloudflare DNS.

The goal was to create a publicly accessible webpage that could be reached using my own domain instead of the EC2 public IP address.

## What I Built

The setup consists of:

- An AWS EC2 instance running Ubuntu
- NGINX installed and running on the EC2 instance
- An AWS Security Group allowing HTTP traffic on port 80
- A custom domain purchased and managed through Cloudflare
- A Cloudflare DNS A record pointing the domain to the EC2 public IPv4 address

The basic structure is:

```text
User
  |
  | visits custom domain
  v
Cloudflare DNS
  |
  | A record
  v
EC2 Instance
  |
  v
NGINX Web Server
  |
  v
NGINX Default Web Page
```

## EC2 Instance

I created an EC2 instance using Ubuntu as the operating system.

The instance was configured with a Security Group that allowed:

- SSH (TCP port 22) for remote administration
- HTTP (TCP port 80) for web traffic

The EC2 instance was assigned the following public IPv4 address:

**16.16.65.110**

## Security Group Configuration

The Security Group was configured with the following inbound rules:

| Type | Protocol | Port | Source |
|------|----------|------|--------|
| SSH | TCP | 22 | My IP |
| HTTP | TCP | 80 | 0.0.0.0/0 |

HTTP traffic was allowed from `0.0.0.0/0` because the website needs to be publicly accessible.

SSH access was restricted to my own IP address after troubleshooting the initial connection issue.

## Installing NGINX

After connecting to the EC2 instance, I updated the Ubuntu package list using:

`sudo apt update`

I then installed NGINX using:

`sudo apt install nginx`

I checked that NGINX was running using:

`sudo systemctl status nginx`

The NGINX service was active and running.

## Testing NGINX

Before configuring the domain, I tested the NGINX server using the EC2 public IPv4 address.

I opened the following in a web browser:

`http://16.16.65.110`

This displayed the default NGINX landing page, confirming that NGINX was successfully installed and accessible over HTTP.

## Domain and DNS Configuration

I used Cloudflare to manage the domain's DNS settings.

I created an **A record** with the following configuration:

| Setting | Value |
|---------|-------|
| Type | A |
| Name | @ |
| IPv4 Address | 16.16.65.110 |
| TTL | Auto |
| Proxy Status | DNS Only |

The A record connects the domain to the public IPv4 address of the EC2 instance.

The connection works as follows:

**Custom Domain → DNS A Record → 16.16.65.110 → AWS EC2 Instance → NGINX**

Cloudflare's proxy was left disabled by selecting **DNS Only** because the assignment only required the domain to point directly to the EC2 instance.

## Final Result

After configuring the DNS record and allowing time for DNS changes to propagate, the custom domain could be used to access the NGINX web server.

Instead of accessing the website using:

`http://16.16.65.110`

the website could be accessed using my own domain:

`http://my-domain.com`

The NGINX default landing page was displayed successfully.


