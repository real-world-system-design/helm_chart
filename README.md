## Instruction to create a helm chart and run it

Helm create is going bootstrap a directory with all the necessary files .
```$ helm create node-init```

After you the helm directory has been initialized you can make desired changes in the values.yaml. Then delete directories such as ingress, serviceacounts if you are not using it as well as delete the test folder.

Render the template
```$ helm template <template_name>```

Install the helm chart
```$ helm install my-app --name=my-app-name```
# ----
```$helm install <release name here node_web> <helm chart loaction>```

Check if the application is running or not
```$ kubectl get po,svc```
```$ curl <IP>:<NodePort>```

We have created and deployed our first Helm chart.

To make the tar archive so that we can share it with others
```$ helm package <template_name>```
