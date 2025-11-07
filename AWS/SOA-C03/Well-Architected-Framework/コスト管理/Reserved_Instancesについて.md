# AWS Reserved Instancesについて

## 概要

Reserved Instances（RI）は、特定のインスタンスタイプ、リージョン、可用性ゾーンに対して1年または3年のコミットメントを行うことで、オンデマンド料金と比較して最大75%の割引を受けることができる料金モデルです。

## Reserved Instancesの種類

### 1. Standard Reserved Instances

#### 概要
Standard Reserved Instancesは、最も高い割引率を提供するRIです。特定のインスタンスタイプ、リージョン、可用性ゾーンにコミットメントします。

#### 特徴
- **割引率**: 最大75%の割引（3年契約、全額前払いの場合）
- **柔軟性**: 低い（特定のインスタンスタイプ、リージョン、AZに固定）
- **変更**: インスタンスタイプ、リージョン、AZの変更は不可
- **容量予約**: 容量予約なし（容量の保証はない）

#### 適用範囲
- Amazon EC2
- Amazon RDS
- Amazon ElastiCache
- Amazon Redshift
- Amazon DynamoDB

#### コミットメント期間
- 1年間
- 3年間

#### 支払いオプション
- **全額前払い（All Upfront）**: 最大の割引率
- **部分前払い（Partial Upfront）**: 中程度の割引率
- **前払いなし（No Upfront）**: 最小の割引率

#### 割引率の目安
- 1年契約、前払いなし: 約30-40%の割引
- 1年契約、全額前払い: 約40-50%の割引
- 3年契約、前払いなし: 約50-60%の割引
- 3年契約、全額前払い: 最大75%の割引

---

### 2. Convertible Reserved Instances

#### 概要
Convertible Reserved Instancesは、Standard RIよりも柔軟性が高いRIです。インスタンスファミリー内で変更が可能ですが、割引率は低めです。

#### 特徴
- **割引率**: 最大54%の割引（3年契約、全額前払いの場合）
- **柔軟性**: 中程度（インスタンスファミリー内で変更可能）
- **変更**: インスタンスファミリー内でインスタンスタイプを変更可能
- **容量予約**: 容量予約なし

#### 適用範囲
- Amazon EC2
- Amazon RDS

#### コミットメント期間
- 1年間
- 3年間

#### 支払いオプション
- **全額前払い（All Upfront）**: 最大の割引率
- **部分前払い（Partial Upfront）**: 中程度の割引率
- **前払いなし（No Upfront）**: 最小の割引率

#### 変更可能な範囲
- インスタンスファミリー内での変更（例：M5ファミリー内でm5.large → m5.xlarge）
- リージョンやAZの変更は不可
- インスタンスファミリー間の変更は不可（例：M5 → C5）

---

### 3. Scheduled Reserved Instances

#### 概要
Scheduled Reserved Instancesは、特定の時間帯に使用するワークロード向けのRIです。週次または月次のスケジュールで使用します。

#### 特徴
- **割引率**: 最大65%の割引（1年契約、全額前払いの場合）
- **柔軟性**: 低い（特定の時間帯に固定）
- **スケジュール**: 週次または月次のスケジュールで使用
- **適用シーン**: 定期実行されるワークロード（バッチ処理、レポート生成など）

#### 適用範囲
- Amazon EC2のみ

#### コミットメント期間
- 1年間のみ

#### 支払いオプション
- **全額前払い（All Upfront）**: 最大の割引率
- **部分前払い（Partial Upfront）**: 中程度の割引率
- **前払いなし（No Upfront）**: 最小の割引率

#### 使用例
- 毎週月曜日の朝に実行されるレポート生成
- 毎月1日に実行されるバッチ処理
- 定期的に実行されるデータ分析ジョブ

---

## Reserved Instancesの支払いオプション

### 全額前払い（All Upfront）
- **特徴**: 契約期間の全額を前払い
- **割引率**: 最も高い
- **メリット**: 最大のコスト削減
- **デメリット**: 初期投資が大きい

### 部分前払い（Partial Upfront）
- **特徴**: 一部を前払い、残りを月次で支払い
- **割引率**: 中程度
- **メリット**: バランスの取れた選択肢
- **デメリット**: 全額前払いより割引率が低い

### 前払いなし（No Upfront）
- **特徴**: 月次で支払い
- **割引率**: 最も低い
- **メリット**: 初期投資が不要
- **デメリット**: 割引率が最も低い

---

## Reserved Instancesの適用範囲

### EC2 Reserved Instances
- EC2インスタンスに適用
- インスタンスタイプ、リージョン、AZにコミットメント
- 容量予約なし（Standard RI、Convertible RIの場合）

### RDS Reserved Instances
- RDSデータベースインスタンスに適用
- データベースエンジン、インスタンスタイプ、リージョン、AZにコミットメント
- マルチAZデプロイメントにも適用可能

### ElastiCache Reserved Instances
- ElastiCacheノードに適用
- キャッシュエンジン、ノードタイプ、リージョンにコミットメント

### Redshift Reserved Instances
- Redshiftクラスターに適用
- ノードタイプ、リージョンにコミットメント

### DynamoDB Reserved Capacity
- DynamoDBの読み取り/書き込みキャパシティに適用
- リージョンにコミットメント

---

## Reserved Instancesの制約事項

### インスタンスタイプの固定
- Standard RI: インスタンスタイプの変更は不可
- Convertible RI: インスタンスファミリー内での変更のみ可能

### リージョンの固定
- リージョン間の移動は不可
- リージョンを変更する場合は、新しいRIを購入する必要がある

### 可用性ゾーンの固定
- Standard RI: 特定のAZに固定（Regional RIを除く）
- Regional RI: リージョン内の任意のAZで使用可能（割引率はやや低い）

### 未使用分の損失
- コミットメントした使用量に達しない場合、未使用分は失われる可能性がある
- 使用量を正確に予測する必要がある

---

## Reserved Instancesの管理

### RI Marketplace
- 未使用のRIを他のAWSアカウントに売却可能
- Standard RIのみ売却可能（Convertible RIは不可）

### RIの変更
- Standard RI: 変更不可（売却のみ可能）
- Convertible RI: インスタンスファミリー内で変更可能

### RIの共有
- AWS Organizationsを使用して、複数のアカウント間でRIを共有可能
- 共有アカウントのRI割引を自動的に適用

---

## Reserved Instances vs Saving Plans

| 項目 | Reserved Instances | Saving Plans |
|------|-------------------|--------------|
| **コミットメント単位** | インスタンス単位 | 使用量（$ per hour）単位 |
| **柔軟性** | 低い | 高い |
| **割引率** | 最大75% | 最大72% |
| **インスタンスタイプ変更** | Standard RI: 不可、Convertible RI: ファミリー内のみ | 可能（Compute Saving Planの場合） |
| **リージョン変更** | 不可 | 可能（Compute Saving Planの場合） |
| **複数サービスへの適用** | 不可（サービスごとに購入が必要） | 可能（Compute Saving Planの場合） |
| **適用サービス** | EC2、RDS、ElastiCache、Redshift、DynamoDB | EC2、Lambda、Fargate、SageMaker |

---

## 選択の指針

### Standard Reserved Instancesを選ぶべき場合
- 特定のインスタンスタイプ、リージョン、AZで長期運用する予定がある
- 最大限の割引率（75%）を求めている
- ワークロードが安定しており、変更の可能性が低い
- RDS、ElastiCache、Redshiftなど、Saving Plansが適用されないサービスを使用している

### Convertible Reserved Instancesを選ぶべき場合
- インスタンスファミリー内で変更する可能性がある
- ある程度の柔軟性が必要だが、Standard RIの割引率も欲しい
- ワークロードが安定しているが、将来的な変更を考慮したい

### Scheduled Reserved Instancesを選ぶべき場合
- 特定の時間帯に定期的に実行されるワークロードがある
- 週次または月次のスケジュールで使用する予定がある
- バッチ処理やレポート生成などの定期実行ジョブがある

---

## ベストプラクティス

### 1. 使用状況の分析
- Cost Explorerを使用して使用状況を分析
- 使用パターンを把握し、適切なRIタイプを選択

### 2. 段階的なアプローチ
- まずは1年契約、前払いなしから始める
- ワークロードが安定してきたら、3年契約、全額前払いに移行

### 3. 適切なサイジング
- 実際の使用量に基づいてRIを購入
- 過剰なコミットメントを避ける

### 4. RI Marketplaceの活用
- 未使用のRIはRI Marketplaceで売却
- 必要なRIはRI Marketplaceで購入

### 5. 定期的な見直し
- 定期的に使用状況を確認
- 未使用のRIを売却または変更

---

## 注意事項

1. **使用量の予測**: RIはコミットメントベースのため、実際の使用量を正確に予測する必要がある
2. **未使用分の損失**: コミットメントした使用量に達しない場合、未使用分は失われる可能性がある
3. **契約期間**: 1年または3年の契約期間中は変更が難しい
4. **支払いオプション**: 前払いが多いほど割引率が高いが、資金繰りを考慮する必要がある
5. **リージョン固定**: リージョンを変更する場合は、新しいRIを購入する必要がある

---

## 参考資料

- [AWS Reserved Instances公式ドキュメント](https://aws.amazon.com/ec2/pricing/reserved-instances/)
- [AWS Cost Management](https://aws.amazon.com/aws-cost-management/)
- [RI Marketplace](https://aws.amazon.com/marketplace/pp/prodview-7zx6vqjqjqjqj)

