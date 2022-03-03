# BT's Instructions
verify installation of Helm & ISTIO
Check Helm Version ,Required for later(I'll use 3.8.0)
```shell
$ helm version
```
Install Stan's Robot Shop on the cluster using the helm chart 
```shell
$ cd helm
$ helm install --name robot-shop --namespace robot-shop .
```
apply the resource quatas
```shell
$ kubectl -n robot-shop apply -f resource-quota.yaml
```
Configure Istio ingress.
```shell
$ kubectl -n robot-shop apply -f Istio/gateway.yaml
```
Use the exposed Istio gateway to access.

```shell
$ kubectl -n istio-system get svc istio-ingressgateway
```
**Importent Suggestion**
use alias to shortcut the kubectl & Specific NS
```shell
$ alias kn=kubectl -n robot-shop
```
##Result


![alt text](https://github.com/UnchainedSoulBT/robot-shop/tree/Ben_Tal/Result.png?raw=true)
