# Secrets

- secretは`repository secret` と `environment secret` の2種類ある  
- `repository secret`は登録すればそのまま参照可能
- `environment secret`をjobから使うには  environment.name で使用する環境の指定が必要
```
    environment:
      name: Test
```

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
