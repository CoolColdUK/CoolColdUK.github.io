---
tags: kubernetes
source: https://kubernetes.io/docs/concepts/workloads/controllers/replicaset/
summary: makes sure the right number of pods are up and running, part of deployment and replacing replication controller
---
A ReplicaSet’s purpose is to maintain a stable set of replica Pods running at any given time. As such, it is often used to guarantee the availability of a specified number of identical Pods.

This is replacing replication controller.

Replica Sets are a sort of hybrid, in that they are in some ways more powerful than Replication Controllers, and in others they are less powerful.

Replica Sets are declared in essentially the same way as Replication Controllers, except that they have more options for the selector. 