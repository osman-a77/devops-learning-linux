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

