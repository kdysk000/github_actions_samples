# Environments

## 新規作成
github の project の settings > Environments を選択し、`New Environment`ボタンを押下

| ![Add](../image/environment_1.jpg)|
|:--|
<br/>

作成するEnvironment名を入力

| ![Input name](../image/environment_2.jpg)|
|:--|
<br/>

## secret と variable の登録
actionからは `${{ secrets.<シークレット名> }}` で参照することができる  

| ![add secret and variable](../image/environment_3.jpg)|
|:--|
<br/>
