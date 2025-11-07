# Transit Gateway 問題集

---

## 問題1

ある企業が、10個のVPCを運用しています。すべてのVPC間で通信を可能にする必要があります。VPCピアリングを使用する場合、何個のピアリング接続が必要ですか？また、Transit Gatewayを使用する場合、何個のAttachmentが必要ですか？

A. VPCピアリング: 45個、Transit Gateway: 10個

B. VPCピアリング: 90個、Transit Gateway: 10個

C. VPCピアリング: 45個、Transit Gateway: 20個

D. VPCピアリング: 90個、Transit Gateway: 20個

---

<details>
<summary>解答1を表示</summary>

### 正解

**正解: A**

### 解説

**VPCピアリングの場合:**
- N個のVPC間で完全メッシュ接続を確立するには、N(N-1)/2個のピアリング接続が必要です
- 10個のVPCの場合: 10 × (10-1) / 2 = 10 × 9 / 2 = 45個

**Transit Gatewayの場合:**
- Transit Gatewayを使用する場合、各VPCをTransit Gatewayに接続するだけで、すべてのVPC間で通信が可能になります
- 10個のVPCの場合: 10個のVPC Attachmentが必要です

**A. 正しい** - VPCピアリング: 45個、Transit Gateway: 10個

**B. 誤り** - VPCピアリングの計算が間違っています

**C. 誤り** - Transit GatewayのAttachment数が間違っています

**D. 誤り** - 両方の計算が間違っています

### 参考

- [AWS Transit Gateway公式ドキュメント](https://docs.aws.amazon.com/vpc/latest/tgw/)

</details>

---

