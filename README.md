# DevOps-Project-BloggingApp-Deployment-Monitoring-PrometheusGrafana-Log-Aggregation-using-Loki-Azure
![image](https://github.com/user-attachments/assets/1c2c0b20-32e0-42a2-bdfb-a3c3114d7b02)

This DevOps project aims to create the infrastructure using Terraform and to establish the CI/CD pipeline using Azure DevOps. For Monitoring Prometheus and Grafana and for Log Aggregation Loki, promtail and Grafana had been used. The Source Code was present in the Azure Repos and Azure DevOps Pipeline had been used as the CI/CD Tool. SonarQube and Azure Artifacts Feed was used for code Analysis and to keep the artifacts for the project respectively. Maven was used as the Build Tool for the project. Trivy was used for file scan and Docker Image Scan as shown in the screenshot attached above. Finally, Application Pods had been created using the Docker Image which was kept in the Azure Container Registries (ACR). For Monitoring Prometheus and Grafana and for Log aggregation Loki, Promtail and Grafana had been used. Node exporter was installed on of each Azure VMs and on the AKS Cluster which extracted the metrics from Azure VMs and AKS Cluster and forwarded to prometheus which finally send them to Grafana where we had visualised with the help of Graphs. For Log Aggregation promtail had been installed on all the Azure VMs and AKS Cluster which extracted the Logs and send to Loki and finally, to Grafana as explained in the High-Level Architecture Diagram drawn above. For this project Helm was used for Deployment to AKS Cluster.      


```
Kubernetes Secrets had been created using the command as shown below.

kubectl create secret docker-registry bloggingapp-auth --docker-server=https://blogappcontainer24registry.azurecr.io --docker-username=blogappcontainer24registry --docker-password=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX -n blogapp
```

```
Source Code:-  https://github.com/singhritesh85/Blogging-App.git

Helm Chart:-   https://github.com/singhritesh85/helm-repo-for-ArgoCD.git
               https://github.com/singhritesh85/helm-chart-promtail.git 
```
