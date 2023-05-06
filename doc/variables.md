# variables

variableは`Organization variables` と `repository secret` と `environment secret` の3種類ある  

|  名称  |  スコープ  |  用途  |
| ---- | ---- | ---- |
|  Organization variables  |  Organization内の全レポジトリの全ワークフローから参照可能  |  Organization全体で利用する値  |
|  Repository variables  |  レポジトリ内の全てのワークフローから参照可能  |  レポジトリ全体で利用する値  |
|  Environments variables  |  レポジトリ内の全てのワークフローが特定環境用に実行される際に参照可能  |  レポジトリで定義した環境によって値を変える  |

## 登録 (repository secret)
github の project の settings > Secrets and variavles > Actions に遷移する

| ![setting](../image/secret_1.jpg)|
|:--|
<br/>

`New repository secret`ボタンから secretを登録する

| ![New repository secret](../image/secret_2.jpg)|
|:--|
<br/>

## 参照 (repository secret)
actionからは `${{ secrets.<シークレット名> }}` で参照することができる  

例：
```
jobs:
  get-secret:
    runs-on: ubuntu-latest
    steps:
      - name: Get secret
        run: |
          echo ${{ secrets.SECRET_TEST }}                  #secretをechoしても*でマスクされて表示される
          echo ${{ secrets.SECRET_TEST }} | sed 's/./& /g' #ただしsedでスペースを挟めば表示できる
```
