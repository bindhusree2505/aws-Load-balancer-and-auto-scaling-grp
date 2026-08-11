# AWS Load Balancer & Auto Scaling

## Introduction

This repository contains my AWS Load Balancer and Auto Scaling learning notes, practical implementations, architecture diagrams, AWS CLI commands, configurations, and interview preparation.

The main focus is understanding how AWS handles **traffic distribution, high availability, fault tolerance, and automatic scaling** using Load Balancers and Auto Scaling Groups.

---

## Topics Covered

### Load Balancer

* Load Balancer Basics
* Types of AWS Load Balancers
* Classic Load Balancer (CLB)
* Creating and Configuring a Classic Load Balancer
* Listeners
* Health Checks
* Traffic Distribution
* Sticky Sessions
* Connection Draining
* Cross-Zone Load Balancing
* Load Balancer Troubleshooting

### Auto Scaling Group

* Auto Scaling Basics
* Launch Templates
* Creating an Auto Scaling Group
* Minimum, Desired and Maximum Capacity
* Scaling Policies
* Health Checks
* Availability Zones
* Auto Scaling with Load Balancer
* Scale-In and Scale-Out
* Auto Scaling Troubleshooting

---

## Repository Structure

```text
AWS-Load-Balancer-Auto-Scaling/
│
├── 01-load-balancer-basics.md
├── 02-classic-load-balancer.md
├── 03-auto-scaling-basics.md
├── 04-launch-template.md
├── 05-auto-scaling-group.md
├── 06-scaling-policies.md
├── 07-load-balancer-with-auto-scaling.md
└── 08-troubleshooting.md
```

---

## Basic Architecture

```text
                         Internet
                            |
                            v
                    Load Balancer
                            |
                +-----------+-----------+
                |                       |
                v                       v
             EC2-1                   EC2-2
                \                       /
                 \                     /
                  +--------+----------+
                           |
                           v
                  Auto Scaling Group
                           |
              +------------+------------+
              |                         |
           Scale Out                  Scale In
              |                         |
              v                         v
        Add EC2 Instances        Remove EC2 Instances
```

---

## Practical Work

This repository includes hands-on AWS Console and CLI implementations for:

* Creating Load Balancers
* Registering EC2 instances
* Configuring listeners and health checks
* Creating Launch Templates
* Creating Auto Scaling Groups
* Configuring scaling policies
* Integrating Load Balancer with Auto Scaling
* Testing scale-out and scale-in behavior

---

## DevOps Focus

The main goal is to understand how **Load Balancer + Auto Scaling Group** work together to build highly available and scalable applications.

```text
User Traffic
     |
     v
Load Balancer
     |
     v
Healthy EC2 Instances
     |
     v
Auto Scaling Group
     |
     +── Scale Out
     |
     +── Scale In
```

---

## Goal

To build strong practical knowledge of AWS Load Balancing and Auto Scaling and understand how they are used in real-world AWS DevOps environments for **high availability, scalability, fault tolerance, and efficient resource management**.
