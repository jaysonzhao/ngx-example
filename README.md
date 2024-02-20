# ngx-example

```
oc new-build openshift/nginx~https://github.com/jaysonzhao/ngx-example.git \
  --name=nginxbase \
  --strategy=source
```

```
oc new-app https://github.com/jaysonzhao/ngx-example.git \
  --context-dir=conf \
  --strategy=docker \
  --name=reverse-proxy
oc expose svc/reverse-proxy
```
