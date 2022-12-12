# VPC
MediaWikiのためのVPC用のAWS CloudFormation用スタックのレポジトリです。

## 使い方

1. `aws cloudformation deploy --template-file formation.yml --stack-name [your stack name] --parameter-overrides VpcCidr=[your cidr base]/16`する
2. デプロイ完了まで待つ

## 作成されるもの

* VPCとそれに付随するインターネットゲートウェイおよびEgress Onlyインターネットゲートウェイ
* 各AZごとにパブリックサブネットとプライベートサブネットが1つずつ
* S3ゲートウェイエンドポイント
