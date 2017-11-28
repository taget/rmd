# RMD - the resource management daemon

[![Build Status](https://travis-ci.org/intel/rmd.svg?branch=master)](https://travis-ci.org/intel/rmd)
[![Go Report Card](https://goreportcard.com/badge/github.com/intel/rmd)](https://goreportcard.com/report/github.com/intel/rmd)
[![GoDoc](https://godoc.org/github.com/intel/rmd?status.svg)](https://godoc.org/github.com/intel/rmd)

## Introduction

RMD is a Linux service running on Linux server to manage resource of the
linux host. It provides RESTful API (follows the [OpenAPI](https://github.com/OAI/OpenAPI-Specification) specification)
to the end user/admin to get the resource usage and control which
workload/application to gain how much resource.

RMD provides a policy based resource management mechanism, high level user will
only care about the QoS of their workload instead of the resource quantity.
A pre-defined policy could be added in RMD, it varies on different hardware
platform.

For the currently reslease, RMD support static LLC allocation based on Linux
kernel's resctrl interface.
For how to use RMD to manage resource, please take a look at
[User Guide](https://github.com/intel/rmd/blob/master/docs/UserGuide.md).

RMD could have an integration with other orchestrator such as OpenStack,
Kubernetes to help manage fine grit resource such as LLC, MBM to let your
cluter have ability to provide high quality QoS.

## Use case

- Public cloud

	In public cloud, the service providers usually group their customers to
    different tiers, the high priority tier customer will get better QoS and
    good performance, it can leverage RMD to provide LLC allocation to achieve
    QoS by reducing resource contention.

- NFV

	NFV(Network function virtualization) focuses on throughput, latency and
    jitter of virtualized network functions (VNFs), a white paper
    [Deterministic Network Functions Virtualization with Intel® Resource
    Director Technology](https://builders.intel.com/docs/networkbuilders/deterministic_network_functions_virtualization_with_Intel_Resource_Director_Technology.pdf)
    shows the LLC has impacts and helps in NFV scenario. RMD supports such
    scenario.

## Documents

* [docs/UserGuide.md](https://github.com/intel/rmd/blob/master/docs/UserGuide.md)
* [docs/DeveloperQuickStart.md](https://github.com/intel/rmd/blob/master/docs/DeveloperQuickStart.md)
* [docs/api/](https://github.com/intel/rmd/tree/master/docs/api/v1) - All the API definitions in Swagger YML
* [docs/references/](https://github.com/intel/rmd/tree/master/docs/reference) - All reference documents from everywhere

## QuickStart for developers

Please refer [**docs/DeveloperQuickStart.md**](https://github.com/intel/rmd/blob/master/docs/DeveloperQuickStart.md)
