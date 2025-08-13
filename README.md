# hard-boiled-k8s

## deploymentの作成
```bash
kubectl apply -f nginx-deployment-v1.yaml
```

## serviceの作成
```bash
kubectl apply -f nginx-service.yaml
kubectl get service nginx-service
```


## deploymentv2の作成
下記のコマンドを打つと新しいバージョンのPodが一つずつ起動し準備ができた後、古いバージョンのPodが一つずつ終了される。
ローリングアップデートが可能。
```bash
kubectl apply -f nginx-deployment-v1.yaml
```

確認コマンド
```bash
kubectl get pods -w -l app=nginx
```
