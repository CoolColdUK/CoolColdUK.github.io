---
source: https://medium.com/google-cloud/kubernetes-101-pods-nodes-containers-and-clusters-c1509e409e16
summary: cluster is a whole project which manages individual nodes, this is total hardware computing power
tags: kubernetes
---
Although working with individual nodes can be useful, it’s not the Kubernetes way. In general, you should think about the cluster as a whole, instead of worrying about the state of individual nodes.

In Kubernetes, nodes pool together their resources to form a more powerful machine. When you deploy programs onto the cluster, it intelligently handles distributing work to the individual nodes for you. If any nodes are added or removed, the cluster will shift around work as necessary. It shouldn’t matter to the program, or the programmer, which individual machines are actually running the code.

If this kind of hivemind-like system reminds you of the Borg from Star Trek, you’re not alone; “Borg” is the name for the internal Google project Kubernetes was based on.