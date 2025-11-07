# CloudFront 問題集

---

## 問題1

ある企業が、S3バケットに静的コンテンツを保存し、CloudFrontを使用して配信しています。S3バケットへの直接アクセスを制限し、CloudFront経由でのみアクセスできるようにする必要があります。

この要件を満たすために、最も適切な方法はどれですか？

A. S3バケットポリシーでCloudFrontのオリジンアクセスアイデンティティ（OAI）のみを許可する

B. S3バケットポリシーでCloudFrontのオリジンアクセス制御（OAC）のみを許可する

C. セキュリティグループでCloudFrontからのアクセスのみを許可する

D. CloudFrontのディストリビューションでS3バケットへのアクセスを制限する

---

<details>
<summary>解答1を表示</summary>

### 正解

**正解: B**

### 解説

**A. 誤り** - OAI（Origin Access Identity）は旧方式であり、現在は非推奨です。新しい方式であるOAC（Origin Access Control）を使用する必要があります。

**B. 正しい** - OAC（Origin Access Control）を使用して、S3バケットポリシーでCloudFrontのOACのみを許可することで、S3バケットへの直接アクセスを制限し、CloudFront経由でのみアクセスできるようにできます。

**C. 誤り** - セキュリティグループはEC2インスタンスなどのネットワークリソースに適用されるもので、S3バケットには適用されません。

**D. 誤り** - CloudFrontのディストリビューション設定だけでは、S3バケットへの直接アクセスを制限することはできません。S3バケットポリシーで制限する必要があります。

### 参考

- [AWS CloudFront Origin Access Control公式ドキュメント](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html)

</details>

---

