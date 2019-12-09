$$ patching in k8s- changing service type from clusterip to nodeport
kubectl patch svc kubernetes-dashboard --type='json' -p '[{"op":"replace","path":"/spec/type","value":"NodePort"}]'
