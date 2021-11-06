# axsis-kube
Kubernetes files for AXSIS-XES GUI

# tips and tricks

> NOTE for Microk8s all commands must be prefixed with `microk8s.` e.g. `microk8s.kubectl`

Check status: `kubectl get all` OR `kubectl describe RESOURCE e.g. pod/...` 

Create deployment/service etc: `kubectl create deployment NAME --image=FQIN e.g. USER/REPOSITORY:TAG`

Delete deployment/service etc: `kubectl delete deployment NAME`

Expose deployment: `kubectl expose deployment NAME --port=PORT` 

Set env var for a pod: `kubectl set env RESOURCE/NAME KEY_1=VAL_1 ... KEY_N=VAL_N`


