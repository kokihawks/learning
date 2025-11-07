# VPNとDirect Connect 問題集

---

## 問題1

ある企業が、オンプレミスネットワークとAWSクラウドを接続する必要があります。以下の要件があります：

1. 低レイテンシが必要
2. 高帯域幅が必要（10Gbps）
3. 専用回線で接続したい
4. コストは重要だが、パフォーマンスを優先する

この要件を満たすために、最も適切な方法はどれですか？

A. Site-to-Site VPNのみを使用する

B. Direct Connectのみを使用する

C. Direct Connectをプライマリ接続として使用し、Site-to-Site VPNをバックアップ接続として使用する

D. Client VPNのみを使用する

---

<details>
<summary>解答1を表示</summary>

### 正解

**正解: C**

### 解説

**A. 誤り** - Site-to-Site VPNはインターネット経由で接続するため、レイテンシが高くなります。また、10Gbpsの帯域幅を確保することは困難です。

**B. 誤り** - Direct Connectは要件を満たしますが、高可用性を確保するためにバックアップ接続を用意することを推奨します。

**C. 正しい** - Direct Connectをプライマリ接続として使用することで、低レイテンシ、高帯域幅、専用回線での接続を実現できます。Site-to-Site VPNをバックアップ接続として使用することで、高可用性も確保できます。

**D. 誤り** - Client VPNは個々のクライアントからVPCに接続するためのものであり、オンプレミスネットワークとAWSクラウドを接続する用途には適していません。

### 参考

- [AWS Direct Connect公式ドキュメント](https://docs.aws.amazon.com/directconnect/)
- [AWS VPN公式ドキュメント](https://docs.aws.amazon.com/vpn/)

</details>

---

