# azure-iot-k8s-gateway
Azure IoT Gateway for Kubernetes

## Fetching Helm Chart

```
helm repo add edgek8s https://edgek8s.blob.core.windows.net/helm/
helm repo update
helm fetch edgek8s/edge-kubernetes
```

## Creating and Registering IoT Hub on Azure

```
az group create --name IoTEdgeResources --location westus2
az iot hub create --resource-group IoTEdgeResources --name ves-iot --sku S1
az iot hub device-identity create --device-id VESEdgeDevice --hub-name ves-iot --edge-enabled
az iot hub device-identity show-connection-string --device-id VESEdgeDevice --hub-name ves-iot
```



