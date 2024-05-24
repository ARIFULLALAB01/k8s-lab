

Commnads:
==================================================

# Basic Commands 

kubectl api-resources
kubectl api-resources | grep volumes
kubectl get <resource-type>
kubectl get po
kubectl get no
kubectl get <resource-type> -o wide
kubectl explain <resource-type>
kubectl describe <resource-type>  <resource-name> 
kubectl describe po nginx -o wide
kubectl describe po nginx -o wide -w
kubectl describe po trail-2 -o wide
kubectl describe po trail-2 -o wide -w
kubectl apply -f trail.yaml
kubectl delete -f trail.yaml
kubectl delete po trail1

===================================================
# to login into PODs below commands need to understand

kubectl exec -it trail2 -- pwd
kubectl exec -it trail2 -- /bin/sh

kubectl exec -it trail3 -- mysql -u nop -p
 
=====================================================

# Labels:
kubectl run --image nginx test1
kubectl run --image nginx test2
kubectl run --image nginx test3

kubectl run --image httpd test4
kubectl run --image httpd test5
kubectl run --image httpd test6

kubectl get po

kubectl get po --showl-labels
kubectl label pod test1 -l "app=nginx"
kubectl label pod test2 -l "app=nginx"
kubectl label pod test3 -l "app=nginx"
kubectl label pod test4 -l "app=apache"
kubectl label pod test5 -l "app=apache"
kubectl label pod test6 -l "app=apache"

kubcetl get po --show-labels

kubectl get pods -l run=test1

kubectl get pods -l app=nginx
kubectl get pods
kubectl get pods -l app=apache
kubectl get pods -l app!=apache

================================================================
## replicaset

kubectl api-resouces | grep repclicaset

kubectl get all
kubectl apply -f trail1.yaml
kubectl get po
kubectl get rs
kubectl get po -o wide -w

kubectl delete po <selectone- POD ID>
kubectl delete po <selectone- POD ID>

kubectl delete rs <rs-ID>

kubectl run --image nginx -l "app=nginx" test1
kubectl run --image nginx -l "app=nginx" test2
kubectl run --image nginx -l "app=nginx" test3
kubectl get po -o wide -w
kubectl apply -f trail.yaml
kubectl get po --show-labels
kubectl delete po test3
kubectl get po --show-labels
kubectl delete po test2
kubectl get po --show-labels
=======================================================

## Deployments