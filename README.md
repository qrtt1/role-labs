

## Example

```
(⎈ dev-gce:default)➜  foo kubectl create ns c8763
namespace/c8763 created
```

```
(⎈ dev-gce:default)➜  foo helm install --name=c8763 --namespace c8763 ./role-lab
NAME:   c8763
LAST DEPLOYED: Thu Feb 27 15:29:51 2020
NAMESPACE: c8763
STATUS: DEPLOYED

RESOURCES:
==> v1/Deployment
NAME   AGE
c8763  4s

==> v1/Pod(related)
NAME                    AGE
c8763-5d5ff6c6fb-c926n  4s

==> v1/Role
NAME        AGE
c8763-role  4s

==> v1/RoleBinding
NAME               AGE
c8763-rolebinding  4s

==> v1/ServiceAccount
NAME      AGE
c8763-sa  4s
```

```
(⎈ dev-gce:default)➜  foo kubectl get ns --show-labels
NAME              STATUS   AGE     LABELS
c8763             Active   37s     c8763=220890ae9be22ff45f53ab98
default           Active   2d23h   3abc3333=dd33,3abc33=33,3adddbc3333=dd33,a=5566,aaa=5566,abc33=33
foobar            Active   34m     foobar=enable
hub               Active   2d23h   abc33=33,abc3=33,abc=3,name=hub,primehub.io/resources-validation-webhook=enabled
ingress-nginx     Active   2d23h   <none>
kube-node-lease   Active   2d23h   <none>
kube-public       Active   2d23h   <none>
kube-system       Active   2d23h   <none>
metacontroller    Active   2d23h   name=metacontroller
rook              Active   2d23h   <none>
rook-system       Active   2d23h   name=rook-system
```
