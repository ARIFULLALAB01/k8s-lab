

Commnads:
---------------

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

--
* to login into PODs below commands need to understand
kubectl exec -it trail2 -- pwd
kubectl exec -it trail2 -- /bin/sh
--
