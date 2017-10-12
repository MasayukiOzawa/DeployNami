# DeployNami
Ubuntu 16.04 の環境で、SQL Server を使用した WordPress の Project Nami のコンテナー環境を作成します。

docker-compose の実行環境で次のコマンドを実行することで、環境が構築できます。

```
git clone https://github.com/MasayukiOzawa/DeployNami .  && SA_PASSWORD=<SQL Server sa パスワード> docker-compose up -d --build
```
