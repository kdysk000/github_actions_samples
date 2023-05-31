## trivy  
TrivyはGo製の脆弱性診断ツール。Linux, Windows, Mac いずれの環境でも動作する。  
コンテナイメージ、ファイルシステム、Git リポジトリの脆弱性、および設定の問題を検出する シンプルで  
包括的なスキャナツール。Trivyは、 OSパッケージ（Alpine、RHEL、CentOSなど）および言語固有のパッケージ  
（Bundler、Composer、npm、yarnなど）の脆弱性を検出する。  
また、 Terraform、Dockerfile、KubernetesなどのInfrastructure as Code (IaC) ファイルをスキャンし、  
デプロイメントの攻撃リスクにさらす潜在的な設定問題を検出する。  

- 脆弱性スキャン  
OSパッケージ、言語のパッケージをスキャンし、脆弱性を発見する  

- Secret スキャン  
鍵ファイル (AWSキー、slackキーなど) が存在してないかを確認する  

- Configスキャン  
Terraform 設定ファイルやDockerfileなどをスキャンし、セキュリティ上問題になりうる設定が含まれてないかチェックする

## trivy-action  
GitHub Actions上でのTrivy実行が可能  
詳細は以下を参照  
https://github.com/aquasecurity/trivy-action

## GitHub Code Scanning
GitHub リポジトリ内のコードを分析して、セキュリティの脆弱性とコーディング エラーを見つけることができる機能   
分析によって特定されたすべての問題はGitHubに表示される  
https://docs.github.com/ja/code-security/code-scanning/automatically-scanning-your-code-for-vulnerabilities-and-errors/about-code-scanning

trivyを使用でき、SARIF 形式をサポートしている  
注意点としてプライベートリポジトリでCode Scanningを実行するには GitHub Advanced Securityのライセンスが必要  
パブリックリポジトリでは無料で使用できる
