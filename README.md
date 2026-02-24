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

------------

# code2car
A hybrid Cloud–Edge SDV Application Lifecycle Management

# Introduction
This blueprint demonstrates an end-to-end workflow for developing, validating and orchestrating Mixed-Critical Software-Defined Vehicle (SDV) applications across cloud and HPC edge device. It showcases how containerized SDV applications are built in the cloud, pushed to a registry, and deployed onto an in-vehicle HPC running AOS Core and digital.auto runtime components such as MQTT, KUKSA, and a Signal Gateway. Vehicle signals are exchanged across heterogeneous compute domains with multiple Linux HPC and ThreadX on MCU — through uProtocol and Zenoh.

# Sample Use Case
1. App developer writes an application and validates in digital.auto playground
1. After successful validation App developer publishes the application in a cloud App Registry
1. OEM deploys digital.auto sdv runtime into existing E/E architecture which abstracts the underlying vehicle complexity for applications.
1. OEM creates a AosCore instance with digital.auto runtime
1. OEM creates AosCloud configuration for app orchestration
1. OEM performs trial deployment from cloud App Registry and tests via digital.auto playground
OEM centrally deploys application from cloud App Registry into vehicle fleet (OTA)

# Architecture
![Architecture](images/architecture.jpg)

# Getting started

## Prerequisites
1. VirtualBox 7.1.x

## Create AosCore instance
Follow this guide to create an AosEdge service: [AosEdge Quick start](https://docs.aosedge.tech/docs/quick-start/)

For the purpose of demo a set of pre-built VMs are used which can be launched using the following shell script.
