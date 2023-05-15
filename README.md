0. a. Pull and run dashboard 
docker pull kubernetesui/dashboard

0. b Deploy dashboard 
    kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.7.0/aio/deploy/recommended.yaml

1. Create adminuser.yaml file

2. Run command 
   kubectl apply -f .\adminuser.yml

3. create ClusterRoleBinding.yml file and apply
    kubectl apply -f ClusterRoleBinding.yml

4. Get Bearer token 
    kubectl -n kubernetes-dashboard create token admin-user

5. Start dashboard proxy
    kubectl proxy

6. Open dashboard at 
http://localhost:8001/api/v1/namespaces/kubernetes-dashboard/services/https:kubernetes-dashboard:/proxy/


Referenced Source: 
1. https://github.com/kubernetes/dashboard/blob/master/docs/user/access-control/creating-sample-user.md
2. https://github.com/kubernetes/dashboard
3. https://hub.docker.com/r/kubernetesui/dashboard
