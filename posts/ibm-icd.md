---
title: 'IBM Cloud Databases - DevOps'
date: '2018-07-31'
---

### job title

Platform developer on ibm cloud databases team.

#### integration of logging and monitoring on kubernetets

We provide customers with databases, so it would be better if we could provide logs as well as metrics.

For logs and metrics we want to send to customers, we take following steps:
1. collect: collect what should be sent to customers
2. modify: we attach some metadata to identify the owner that data belongs to
3. send: we send the data which has been modified to remote services

#### Upgrade and maintain the Billing component

The Billing is a very critical component in ICD, we use it to record billing records for customers, we have to make sure we don't lose any records, meanwhile we have to confirm the low latency between the `created_at` and `sent_at` of each record, or we would violate the requirement of IBM Cloud.

I integrated it with the monitoring, start a metric server inside it and let it work like a prometheus exporter, in this way we could get triggered with an alert when it doesn't work as expected.

#### Data-Plane-Test

Data-Plane-Test is a tool for automatic test in data plane clusters, it's started by my teammate `Alexander` and i submit the most commits during the development.

Mostly, the DPT is used in three places:
- Pull Request, i integrated it with pipeline, so DB developers could use it inside one pull request
- run it locally, it's more flexible to use it locally, we could specify any tests we want to run on an existing DB
- release campaign, during the release, we use it to run all tests against all versions of all kinds of databases, the release could only go once it passes.

#### Virtual Private Endpoint

It's a requirement from IBM Cloud, IBM Cloud has a framework called virtual private cloud (VPC), in order to let customers connect to an ICD instance inside a VPC, we have to some integration.

#### Satellite

It's also a framework on IBM Cloud.

it looks like a real private cloud, we provide DB services, but all components are installed on the data center which belongs to customers, in this situation, we have to some re-factory or involve some new components to support it like alert-controller/alert-forwarder.

#### Others

I also worked on some other topics, like CI/CD, image migration, dispatcher, kubernetes controllers and so on....

### feeling

I joined IBM after I graduated from `Beijing Institute of Technology`.

Honestly it's really a nice place to work as a first-step in the journey:
- the relationship around people here is pretty simple so everyone could feel relax and enjoy his work
- work-life balance, no 996, everyone tells you to have a good relax here instead of asking you to work during your vacation
- grow up quickly, i really learnt much from folks around the global team, most of them are very friendly and easy to get along.
- there are so many advantages i can't say....

Anyway it's sad to leave.
