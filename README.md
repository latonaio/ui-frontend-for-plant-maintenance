# ui-frontend-for-plant-maintenance  
ui-frontend-for-maintenance は、エッジコンピューティング環境において、ロボットコントローラやPLCからデータを取得し、ロボット自身では監視しきれない稼働情報、異常情報や、設備保全変更履歴などをUIフロントエンドに表示する [plant-maintenance-system](https://github.com/latonaio/plant-maintenance-system) のUIフロントエンドリソースです。  

## 動作環境  
動作には以下の環境であることを前提とします。  
・OS: Linux OS  
・CPU: ARM/AMD/Intel  
・Kubernetes  
・AION のリソース  

## 機器構成
・ ワークステーション1台(このUIリソースを配置する)  
・ ロボットコントローラ1台  

## kubernetes上での使用方法
### 起動方法
1. 以下のコマンドでDockerイメージをビルドする  
`$ bash docker-build.sh`
2. 以下コマンドでkubernetes上にリソースを展開する  
`$ kubectl apply -f k8s/`

### 停止方法
1. 以下のコマンドでkubernetes上からリソースを削除する  
`$ kubectl delete -f k8s/`

## 参考
・[ui-backend-for-plant-maintenance](https://github.com/latonaio/ui-backend-for-plant-maintenance)