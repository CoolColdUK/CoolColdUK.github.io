---
tags: kubernetes
source: udemy course

---

## Pod Status
Init
PodInitializing
Running

Can be seen via ```kubectl get pods```
1. Running
    1. Pod has been bound to a node
    2. All container created
    3. At least one container is still running

2. Pending - accepted but not running
    1. still downloading image
    2. resource constraints

3. Succeeded
    1. all pods terminated successfully and will NOT be restarted

4. Failed
    1. all pods terminated and at least one with non zero exit code

5. Unknown
    1. Network error

## Pod Condition
Can be obtained via ```kubectl describe pod PODNAME```

1. PodScheduled - scheduled to a node
2. Initialized - the initialization container has been started successfully
3. Ready - Can serve request and add to service
4. Unschedulable - pod can't be scheduled (maybe resource constraint)
5. ContainerReady - all containers in the pod are ready

## Container State
Can be obtained via ```kubectl get pod```

1. Running
2. Waiting
3. Terminated
