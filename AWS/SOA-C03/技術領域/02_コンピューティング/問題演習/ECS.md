# ECS 問題集

---

## 問題1

ある企業が、ECSを使用してコンテナアプリケーションを実行しています。Fargate起動タイプを使用する場合、以下のうち正しい説明はどれですか？

A. EC2インスタンスを管理する必要がある

B. ネットワークモードはbridgeモードのみ使用可能

C. 各タスクに独自のENI（Elastic Network Interface）が割り当てられる

D. タスクごとにセキュリティグループを設定できない

---

<details>
<summary>解答1を表示</summary>

### 正解

**正解: C**

### 解説

**A. 誤り** - Fargate起動タイプはサーバーレスであるため、EC2インスタンスを管理する必要はありません。AWSがインフラストラクチャを管理します。

**B. 誤り** - Fargate起動タイプでは、awsvpcネットワークモードのみ使用可能です。bridgeモードやhostモードは使用できません。

**C. 正しい** - Fargate起動タイプでは、awsvpcネットワークモードを使用するため、各タスクに独自のENI（Elastic Network Interface）が割り当てられます。これにより、各タスクに独自のIPアドレスが割り当てられ、セキュリティグループを設定できます。

**D. 誤り** - Fargate起動タイプでは、awsvpcネットワークモードを使用するため、タスクごとにセキュリティグループを設定できます。

### 参考

- [AWS ECS Fargate公式ドキュメント](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/AWS_Fargate.html)

</details>

---

