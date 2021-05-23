# 20210525-LT Service公開


# NodePort タイプでService公開
テスト用アプリケーションのPodsを作成
```YAML
cat <<EOF > nginx-deployment.yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx-deployment
  labels:
    app: nginx
spec:
  replicas: 2
  selector:
    matchLabels:
      app: nginx
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
      - name: nginx
        image: nginx:1.14.2
        ports:
        - containerPort: 80
EOF
```

# LoadBalancer タイプでService公開


# Ingress Controller を使ってService公開


