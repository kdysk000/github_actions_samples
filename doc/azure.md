## Azure ログイン
#### OpenID Connect 認証
```
- name: Log in with Azure
  uses: azure/login@v1
  with:
      client-id: ${{ secrets.AZURE_CLIENT_ID }}
      tenant-id: ${{ secrets.AZURE_TENANT_ID }}
      subscription-id: ${{ secrets.AZURE_SUBSCRIPTION_ID }}
```
#### サービス プリンシパル 認証
```
- name: Log in with Azure
  uses: azure/login@v1
  with:
    creds: '${{ secrets.AZURE_CREDENTIALS }}'
```
<br>

## コンテナレジストリへのログイン
Azure Container Registoryなどのプライベートコンテナーレジストリにログインする。  
ログインが完了すると、ワークフロー内の次の一連のアクションでコンテナーの構築、タグ付け、プッシュなどのタスクを実行できる。
```
- uses: azure/docker-login@v1
  with:
    login-server: '<login server>'
    username: '<username>'
    password: '<password>'
```
以下の例は、コンテナレジストリにログインしイメージをpullするフロー
```
- uses: azure/docker-login@v1
  with:
    login-server: '<login server>'
    username: '<username>'
    password: '<password>'
- run: |
    docker pull private/image:latest
```
