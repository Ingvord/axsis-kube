# axsis-kube
Kubernetes files for AXSIS-XES GUI

# before

`mkdir -p /var/axsis/kibana/config`

# tips and tricks

> NOTE for Microk8s all commands must be prefixed with `microk8s.` e.g. `microk8s.kubectl`

Check status: `kubectl get all` OR `kubectl describe RESOURCE e.g. pod/...` 

Create deployment/service etc: `kubectl create deployment NAME --image=FQIN e.g. USER/REPOSITORY:TAG`

Delete deployment/service etc: `kubectl delete deployment NAME`

Expose deployment: `kubectl expose deployment NAME --port=PORT`

Upgrade deployment: `kubectl set image deployment/NAME CONTAINER_NAME=NEW_IMAGE` e.g. `microk8s.kubectl set image deployment/tango-server axsis-virtual-tango-host=ingvord/axsis-virtual-tango-host:AxsisTangoServer-0.5`

Set env var for a pod: `kubectl set env RESOURCE/NAME KEY_1=VAL_1 ... KEY_N=VAL_N`

Run jive in a docker: `docker run --net=host -e DISPLAY -e TANGO_HOST=localhost:10000 -v /tmp/.X11-unix tangocs/tango-jive:7.22`
