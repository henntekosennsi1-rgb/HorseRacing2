# HorseRacing2 - 競馬

> ⚠️ **α版（アルファ版）** - このプラグインは現在開発中です。バグが存在する可能性があります。

7種類の馬券タイプに対応した競馬プラグインです。

---

## ⚠️ 前提プラグイン（必須）

**[EmeraldBank](https://github.com/henntekosennsi1-rgb/EmeraldBank)** が必要です！

### インストール手順

1. [EmeraldBank](https://github.com/henntekosennsi1-rgb/EmeraldBank/releases) をダウンロード
2. [HorseRacing2](https://github.com/henntekosennsi1-rgb/HorseRacing2/releases) をダウンロード
3. 両方の.jarファイルを `plugins` フォルダに配置
4. サーバーを再起動

---

## 機能

### 馬券タイプ（7種類）

| 馬券 | 説明 | 選択数 |
|------|------|--------|
| 単勝 | 1着を当てる | 1頭 |
| 複勝 | 3着以内を当てる | 1頭 |
| 馬連 | 1着と2着（順不同） | 2頭 |
| 馬単 | 1着と2着（順番通り） | 2頭 |
| ワイド | 3着以内の2頭（順不同） | 2頭 |
| 3連複 | 3着以内の3頭（順不同） | 3頭 |
| 3連単 | 1着・2着・3着（順番通り） | 3頭 |

### オッズ範囲

| 馬券 | 最小 | 最大 |
|------|------|------|
| 単勝 | 1.2倍 | 2.5倍 |
| 複勝 | 1.1倍 | 1.5倍 |
| 馬連 | 1.5倍 | 5.0倍 |
| 馬単 | 3.0倍 | 15.0倍 |
| ワイド | 1.3倍 | 3.0倍 |
| 3連複 | 3.0倍 | 10.0倍 |
| 3連単 | 8.0倍 | 30.0倍 |

### 馬のステータス
- 脚力（Strength）: 5〜10
- スタミナ（Stamina）: 4〜9
- 賢さ（Intelligence）: 3〜8

---

## コマンド

### プレイヤー用

| コマンド | 説明 |
|---------|------|
| `/horseracing bet` | ベッティングGUIを開く |
| `/horseracing getbetitem` | ベット券アイテムを取得 |

### 管理者用

| コマンド | 説明 |
|---------|------|
| `/horseracing start` | レース開始/停止 |
| `/horseracing stop` | 緊急停止 |
| `/horseracing setup spawn` | スポーン地点設定 |
| `/horseracing setup lobby` | ロビー地点設定 |
| `/horseracing sethorse <数>` | 出走馬の数（1-18） |
| `/horseracing sethousepoint <番号>` | 馬のスタート位置 |
| `/horseracing setlocation <番号>` | チェックポイント |
| `/horseracing setspeed <倍率>` | 速度倍率 |
| `/horseracing givebetitem <player> [数]` | ベット券配布 |

---

## セットアップ

### 1. 位置設定
```
/horseracing setup spawn   ← 退出時のテレポート先
/horseracing setup lobby   ← ロビー地点
```

### 2. コース設定
```
/horseracing sethorse 8           ← 8頭でレース
/horseracing sethousepoint 1      ← 1番馬のスタート位置
/horseracing sethousepoint 2      ← 2番馬のスタート位置
...
/horseracing setlocation 1        ← チェックポイント1
/horseracing setlocation 2        ← チェックポイント2
...
```

### 3. レース開始
```
プレイヤー: /horseracing bet
管理者: /horseracing start
```

---

## 権限

| 権限 | 説明 | デフォルト |
|------|------|-----------|
| `horseracing.admin` | 全管理権限 | op |
| `horseracing.bet` | ベットを行う | true |

---

## 設定（config.yml）
```yaml
betting:
  takeout_rate: 0.2      # 控除率20%
  minimum_odds: 1.1
  virtual_bet_amount: 5000

horse_stats:
  strength: {min: 5, max: 10}
  stamina: {min: 4, max: 9}
  intelligence: {min: 3, max: 8}
```

---

## 動作環境

- **[EmeraldBank](https://github.com/henntekosennsi1-rgb/EmeraldBank)（必須）**
- Spigot/Paper 1.21.x
- Java 17以上

## コミュニティ

**Discord:** https://discord.gg/zYY55dzhjd

## ライセンス

All Rights Reserved
