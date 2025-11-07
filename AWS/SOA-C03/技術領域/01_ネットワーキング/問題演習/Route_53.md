# Route 53 問題集

---

## 問題1

ある企業が、複数のリージョンにアプリケーションをデプロイしています。ユーザーに最も近いリージョンに自動的にルーティングし、パフォーマンスを最適化したいと考えています。

この要件を満たすために、最も適切なRoute 53のルーティングポリシーはどれですか？

A. Simple Routing

B. Weighted Routing

C. Latency-Based Routing

D. Failover Routing

---

<details>
<summary>解答1を表示</summary>

### 正解

**正解: C**

### 解説

**A. 誤り** - Simple Routingは、単純にリソースにルーティングするポリシーであり、ユーザーの位置に基づくルーティングは行いません。

**B. 誤り** - Weighted Routingは、重みに基づいてトラフィックを分散するポリシーであり、ユーザーの位置に基づくルーティングは行いません。

**C. 正しい** - Latency-Based Routingは、ユーザーに最も近いリージョン（レイテンシが最も低いリージョン）に自動的にルーティングするポリシーです。これにより、パフォーマンスを最適化できます。

**D. 誤り** - Failover Routingは、プライマリリソースとセカンダリリソースを設定し、プライマリが障害発生時にセカンダリにフェイルオーバーするポリシーであり、ユーザーの位置に基づくルーティングは行いません。

### 参考

- [AWS Route 53 Latency-Based Routing公式ドキュメント](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html#routing-policy-latency)

</details>

---

