```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  labels:
    app: app
  name: app
spec:
  replicas: 3
  selector:
    matchLabels:
      app: app
  strategy: 
    type: RollingUpdate
  template:
    metadata:
      labels:
        app: app
    spec:
      containers:
      - image: nginx
        name: nginx
        resources: {}
```
