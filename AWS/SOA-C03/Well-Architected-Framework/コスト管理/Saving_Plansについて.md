# AWS Saving Plansについて

## 概要

AWS Saving Plansは、柔軟性とコスト削減を両立させる料金モデルです。一定の使用量（1時間あたりの料金）を1年または3年の期間でコミットメントすることで、オンデマンド料金と比較して最大72%の割引を受けることができます。

## Saving Plansの種類

### 1. Compute Saving Plan

#### 概要
Compute Saving Planは、最も柔軟性の高いSaving Planです。EC2、Lambda、Fargateなど、複数のコンピューティングサービスに適用できます。

#### 特徴
- **柔軟性が高い**: EC2、Lambda、Fargateなど、複数のコンピューティングサービスに適用可能
- **インスタンスタイプの変更が容易**: 同じファミリー内でインスタンスタイプを変更しても適用される
- **リージョン間の移動が可能**: 同じリージョン内で異なるリージョン間でも適用される場合がある
- **割引率**: 最大72%の割引（3年契約、全額前払いの場合）

#### 適用範囲
- Amazon EC2
- AWS Lambda
- AWS Fargate
- その他のコンピューティングサービス

#### コミットメント期間
- 1年間
- 3年間

#### 支払いオプション
- 全額前払い（All Upfront）
- 部分前払い（Partial Upfront）
- 前払いなし（No Upfront）

### 2. EC2 Instance Saving Plan

#### 概要
EC2 Instance Saving Planは、EC2インスタンスに特化したSaving Planです。Compute Saving Planよりも割引率が高い場合がありますが、柔軟性は低めです。

#### 特徴
- **EC2専用**: EC2インスタンスのみに適用
- **インスタンスファミリー固定**: 特定のインスタンスファミリー（例：M5、C5など）にコミットメント
- **リージョン固定**: 特定のリージョンにコミットメント
- **割引率**: Compute Saving Planと同等またはそれ以上の割引が期待できる

#### 適用範囲
- Amazon EC2インスタンスのみ

#### コミットメント期間
- 1年間
- 3年間

#### 支払いオプション
- 全額前払い（All Upfront）
- 部分前払い（Partial Upfront）
- 前払いなし（No Upfront）

#### 制約事項
- インスタンスファミリーを変更する場合は、新しいSaving Planを購入する必要がある
- リージョンを変更する場合は、新しいSaving Planを購入する必要がある

### 3. SageMaker AI Saving Plan

#### 概要
SageMaker AI Saving Planは、Amazon SageMakerの機械学習ワークロードに特化したSaving Planです。SageMakerの推論インスタンスやトレーニングインスタンスのコストを削減します。

#### 特徴
- **SageMaker専用**: SageMakerの推論インスタンスとトレーニングインスタンスに適用
- **MLワークロード最適化**: 機械学習の使用パターンに最適化された料金モデル
- **柔軟性**: インスタンスタイプやリージョンを変更しても適用される場合がある
- **割引率**: オンデマンド料金と比較して大幅な割引

#### 適用範囲
- Amazon SageMaker推論インスタンス
- Amazon SageMakerトレーニングインスタンス

#### コミットメント期間
- 1年間
- 3年間

#### 支払いオプション
- 全額前払い（All Upfront）
- 部分前払い（Partial Upfront）
- 前払いなし（No Upfront）

#### 使用例
- 本番環境での推論ワークロードが安定している場合
- 定期的にモデルトレーニングを実行する場合
- 予測可能なMLワークロードがある場合

## Saving Plansの比較

| 項目 | Compute Saving Plan | EC2 Instance Saving Plan | SageMaker AI Saving Plan |
|------|---------------------|--------------------------|--------------------------|
| 適用サービス | EC2, Lambda, Fargate等 | EC2のみ | SageMakerのみ |
| 柔軟性 | 最高 | 中 | 中〜高 |
| インスタンスタイプ変更 | 可能 | ファミリー内のみ | 可能 |
| リージョン変更 | 可能 | 不可 | 可能 |
| 割引率 | 最大72% | 最大72% | サービスにより異なる |
| 推奨用途 | 複数サービス使用 | EC2のみ使用 | MLワークロード |

## 選択の指針

### Compute Saving Planを選ぶべき場合
- 複数のコンピューティングサービス（EC2、Lambda、Fargate）を使用している
- インスタンスタイプやリージョンを頻繁に変更する可能性がある
- 柔軟性を最優先したい

### EC2 Instance Saving Planを選ぶべき場合
- EC2のみを使用している
- 特定のインスタンスファミリーとリージョンで安定したワークロードがある
- より高い割引率を求めている

### SageMaker AI Saving Planを選ぶべき場合
- SageMakerを定期的に使用している
- 推論やトレーニングのワークロードが予測可能
- MLワークロードのコストを最適化したい

## 注意事項

1. **使用量の予測**: Saving Planはコミットメントベースのため、実際の使用量を正確に予測する必要がある
2. **未使用分の損失**: コミットメントした使用量に達しない場合、未使用分は失われる可能性がある
3. **契約期間**: 1年または3年の契約期間中は変更が難しい
4. **支払いオプション**: 前払いが多いほど割引率が高いが、資金繰りを考慮する必要がある

## 参考資料

- [AWS Saving Plans公式ドキュメント](https://aws.amazon.com/savingsplans/)
- [AWS Cost Management](https://aws.amazon.com/aws-cost-management/)

