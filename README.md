# postgresql_tools_chart
A helm chart for deploying misterdorito/postgresql_tools docker container into k8s environment.

## Assumptions
These instructions assumes that:
..*kubectl is installed and kubeconfig is in proper working order.
..*helm (and tiller as required) is installed.

## Deploying chart
1. Clone this repo.
2. cd into the root of this repo.
3. Run the following command:
```
   helm install -n <namespace> --set pg_version=[postgresql version] pgtools .
```
The supported PostgreSQL version are 9.4, 9.6, 11 and 12.

## Undeploying the chart
To undeploy the chart, issue the following command:
```
   helm -n [namespace] delete pgtools
```
