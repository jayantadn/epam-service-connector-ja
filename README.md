# eclipse SDV blueprint with digital.auto and AosEdge

TODO: dont read any further yet

An Integration Blueprint for Rapid SDV Prototyping with digital.auto on Red Hat IVOS

# Introduction
This repository provides a catalyst for building a true cloud-to-car development workflow. It serves as an initial blueprint demonstrating how developers can package a digital.auto application, deploy it to the digital.auto SDV runtime, and execute it within an environment powered by Red Hat's In-Vehicle Operating System (RIVOS). 

The goal is to establish a starting point for a fully integrated toolchain that accelerates the development and validation of mixed-criticality automotive software.

# User journey
| `digital.auto` Playground Workflow                                       | Edge Device Workflow                                                     |
| :----------------------------------------------------------------------- | :----------------------------------------------------------------------- |
| 1. Develops a new SDV application.                                       | 1. Installs RIVOS onto an edge device.                                   |
| 2. Configures the edge device as a new runtime target in the playground. | 2. Integrates the `digital.auto` SDV runtime into the RIVOS environment. |

---

**End-to-End Execution:** The user then executes the application from the playground, deploying it to the new runtime running on the edge device.


# Architecture
![Blueprint v1](images/01_blueprint_v1.jpg)

# Getting started

## Prerequisites
1. Fedora installation on a machine
   1. The blueprint has been tried on Fedora 43
   2. AutoSD is seen to have connectivity issues with WSL. Hence a discrete device is recommended.

## Steps for demo
TODO: Kiran

# Demo in action
![demo v1](images/02_demo_v1.gif)
