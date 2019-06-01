---
tags: kubernetes
source: https://kubernetes.io/docs/tasks/configure-pod-container/configure-liveness-readiness-probes/
summary: determines whether pod is usable or not
---

liveness probes to know when to restart a Container. For example, liveness probes could catch a deadlock, where an application is running, but unable to make progress. Restarting a Container in such a state can help to make the application more available despite bugs.

The kubelet uses readiness probes to know when a Container is ready to start accepting traffic. A Pod is considered ready when all of its Containers are ready. One use of this signal is to control which Pods are used as backends for Services. When a Pod is not ready, it is removed from Service load balancers.

2 ways to do health check
1. run a command in the container periodically
2. periodic checks on a url