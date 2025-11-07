# Elastic Beanstalk 問題集

---

## 問題1

ある企業が、Elastic Beanstalkを使用してアプリケーションをデプロイしています。本番環境で、ゼロダウンタイムでデプロイを行う必要があります。

この要件を満たすために、最も適切なデプロイメント戦略はどれですか？

A. All at Once

B. Rolling

C. Immutable

D. Blue/Green

---

<details>
<summary>解答1を表示</summary>

### 正解

**正解: D**

### 解説

**A. 誤り** - All at Onceデプロイメントは、すべてのインスタンスに同時にデプロイするため、ダウンタイムが発生する可能性があります。

**B. 誤り** - Rollingデプロイメントは、段階的にデプロイしますが、一部のインスタンスが更新中にダウンタイムが発生する可能性があります。

**C. 誤り** - Immutableデプロイメントは、新しいインスタンスを作成してデプロイしますが、完全にゼロダウンタイムを保証するものではありません。

**D. 正しい** - Blue/Greenデプロイメントは、新しい環境（Green）を作成してデプロイし、正常性を確認した後、トラフィックを切り替えます。これにより、ゼロダウンタイムでデプロイできます。

### 参考

- [AWS Elastic Beanstalkデプロイメント戦略公式ドキュメント](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/using-features.rolling-version-deploy.html)

</details>

---

