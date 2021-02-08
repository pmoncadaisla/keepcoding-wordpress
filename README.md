# Wordpress in Kubernetes

## 1. Installation

### 1.1 Create namespace

```
kubectl create ns wordpress
kubectl label namespace wordpress app=wordpress
```

### 1.2 Create secret

```
PASSWORD=mysecretpassword
NAMESPACE=wordpress
kubectl -n $NAMESPACE create secret generic credentials --from-literal=MYSQL_ROOT_PASSWORD=$PASSWORD
```

### 1.3 Install wordpress

```
PASSWORD=mysecretpassword
NAMESPACE=wordpress
kubectl -n $NAMESPACE create secret generic credentials --from-literal=MYSQL_ROOT_PASSWORD=$PASSWORD
```