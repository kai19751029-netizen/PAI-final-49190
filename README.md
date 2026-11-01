# PAI-final-49190
PushT ACT policy: comparison of 30 and 60 epochs
# PAI最終課題_49190

## 概要
PushTシミュレーターで、ACTによる模倣学習を実施。
30エポックのモデルと、さらに30エポック追加学習したモデルを比較しました。

RoboOps入門教材を基に、追加学習、モデルの別名保存、
同一評価条件での比較、比較動画の作成を追加しました。

## 結果
各モデルを同じ20個のseed（1000〜1019）、最大300ステップで評価しました。

| モデル | 平均最大報酬 | 成功率 |
|---|---:|---:|
| 30エポック | 0.420 | 0%（0/20） |
| 30＋30エポック | 0.649 | 10%（2/20） |

追加学習時にAdamWを再初期化しているため、
学習量だけによる効果とは断定できません。
また、各条件20回・学習1系列の結果です。

## 実行方法
Docker Desktopを起動し、このリポジトリのフォルダーで実行します。

docker compose up --build

ブラウザーで以下を開き、ノートブックを開いて実行します。
http://localhost:8888/lab?token=roboops-workshop

## 提出動画
https://youtu.be/jAwFzlJTuBw

動画は約98秒です。
実演例は30エポックがseed 1007、追加学習後がseed 1008です。
集計結果は同じ20個のseedで比較しています。

## 使用技術
Python / PyTorch / LeRobot ACT / gym-pusht / Docker / JupyterLab

## 出典・支援
講義教材「PushTで学ぶRoboOps入門」を使用しました。
コード追加・エラー対応・説明資料作成にChatGPTを利用しました。
