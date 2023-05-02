# act

## actとは
GitHub Actions をローカルで実行するコマンドツール  
利用するには Docker が必要

## インストール
以下のコマンドを実行
```
curl https://raw.githubusercontent.com/nektos/act/master/install.sh | sudo bash
```
カレントディレクトリに/bin/actがインストールされるので
/usr/local/binなどPATHが通っているところにコピーしておく
```
$ curl https://raw.githubusercontent.com/nektos/act/master/install.sh | sudo bash
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  9886  100  9886    0     0  58497      0 --:--:-- --:--:-- --:--:-- 58497
nektos/act info checking GitHub for latest tag
nektos/act info found version: 0.2.45 for v0.2.45/Linux/x86_64
nektos/act info installed ./bin/act

$ sudo cp bin/act /usr/local/bin/
$ which act
/usr/local/bin/act
```

## 実行方法
```
act [event name] [flags]
```

### flags  
　-j ： ジョブ名の指定  
　-s ： シークレットの指定  
　--secret-file ： シークレットをファイルに書いて指定  
　--env-file ： 環境変数をファイルに書いて指定  
　-l ： アクションの一覧表示  
　-W ： ワークフローファイル直接指定  
　-e ： イベントパスのJSONファイル  
 
　act --help で詳細を確認

### 例
**・ジョブ名がsample-flowのworkflow_dispatchを実行**
```
act workflow_dispatch -j sample-flow
```
**・workflow_dispatchでトリガーされるワークフロー一覧**
```
act workflow_dispatch -l
```
**・ワークフローを直接指定して実行**
```
act workflow_dispatch -W .github/workflows/helloworld.yaml
```
**・シークレットを指定して実行**
```
act workflow_dispatch -s SECRET1=value1 -s SECRET2=value2 -W .github/workflows/helloworld.yaml
```

