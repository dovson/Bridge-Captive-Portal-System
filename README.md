# Bridge-Captive-Portal-System
Description of the Bridge Captive Portal System

# Captive Portal System (Custom NDIS Filter + Internal DHCP/DNS)

A high-performance Windows-based captive portal built with a custom NDIS filter driver, internal DHCP and DNS servers, and an integrated web authentication system. Designed to control network access and manage user sessions efficiently.

## Overview

This project implements a complete captive portal solution for Windows environments. It intercepts and filters traffic at the kernel level using a custom NDIS filter driver. Unauthorized users are redirected to an internal web portal until authenticated.

The system integrates:
- A **kernel-mode NDIS filter** for traffic interception.
- **Internal DHCP and DNS servers** to handle IP leases and redirection.
- A **web authentication interface** that communicates with the driver via a DLL.
- A **billing and user management system** that tracks data usage and session time.

The entire solution
