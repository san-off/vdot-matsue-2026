# vdot-matsue-2026
Data-driven training logs for Matsue Castle Marathon 2026 (Target: Sub 3:30 / VDOT 48+)

# 🏃‍♂️ Project VDOT 48 → 5X: Road to Matsue Castle Marathon 2026
> **"Data-Driven Running & Injury Prevention Project"**

---

## 🎯 Mission & Goals
- **Main Event:** **第7回 松江城マラソン (2026年12月)**
- **Primary Goal:** サブ 3:30 (4:58/km) 突破
- **Stretch Goal:** 3:20 (4:44/km) 切り
- **Strategy:** 宍道湖・中海の風に負けない「体幹連動」と「安定した接地」の確立

---

## 📊 Current Specs (as of 2026.04.30)
| Metric | Value | Notes |
| :--- | :--- | :--- |
| **Current VDOT** | **48** | T-Pace: 4:24/km |
| **Garmin VO2 Max** | **53** | 潜在能力をフルマラソンの持久力へ変換中 |
| **Location** | **Yonago/Kaike** | 皆生の風 = 松江攻略の仮想トレーニング環境 |

---

## 📈 VDOT Review Schedule
- **毎月15日 / 末日:** スプレッドシートのログとGarminデータを元に判定。
- **判定基準:** ジャック・ダニエルズ式Tペースの余裕度 ＋ 主観的強度(RPE)

---

## 👟 Shoe Rotation (Advisor Fujiwara Theory)
藤原氏の提唱するカテゴリーに基づき、適材適所で履き分けます。

- **Daily Trainer (Base/Stability):**
    - **Brooks Ghost 16** (★購入済：接地感覚の教育と安定した走行の軸)
- **Recovery/Easy:**
    - **New Balance FreshFoam x v14** (足を甘やかし、疲労を抜く)
- **Speed/Tempo:**
    - **New Balance FuelCell Rebel v4** (反発を全身で制御する練習用)
- **Super Trainer (Long/Race Candidate):**
    - [Candidate 1] **ASICS SONICBLAST** (コストパフォーマンス重視。第一候補)
    - [Candidate 2] **Brooks Hyperion Max 3** (大幅な値引きがあった場合の対抗候補)

---

## 🛠 Project Structure
- `/data/raw_csv/`: Garminからエクスポートしたアクティビティデータ
- `/logs/`: [5月ランニングログ.xlsx] (スプレッドシートへのリンクまたは保存場所)
- `REPORTS.md`: 毎月15日・末日のVDOT定期検診の結果まとめ

---

## 📈 VDOT Review Logic
毎月15日と末日に、Geminiコーチと共に以下の要素を評価し、VDOTを再定義する。
1. **Tペース走の安定性:** 心拍ゾーン4（170-178bpm）でのコントロール。
2. **主観的強度 (RPE):** 「脚だけ」になっていないか、全身が連動しているか。
3. **環境補正:** 向かい風10m/s以上の日は、ペースよりも「努力量」を重視。

---

## 📂 Data Management & Naming Convention
`data/raw_csv/` に蓄積するGarminデータは、解析の再現性を高めるため以下の形式で統一します。

- **Format:** `YYYYMMDD_種別_場所.csv`

### 📍 Location Aliases (場所の定義)
入力を簡略化するため、以下のエイリアスを使用します。
- `inda-home`: 職場（陰田町）から自宅（両三柳）への帰宅ランルート
- `kaike`: 皆生・弓ヶ浜サイクリングロード周辺
- `city`: 米子市街地巡回ルート
- `track`: どらドラパーク米子陸上競技場（東山）

### Examples
- `20260506_E-jog_inda-home.csv`
- `20260515_T-run_kaike.csv`

### ⚠️ Data Analysis Notes (分析時の注意点)
データの正確性を期すため、解析（手動・AI共）の際は以下に注意してください。

- **概要行の除外:** GarminからエクスポートしたCSVの末尾には、全ラップの合計値（概要行）が含まれている場合があります。
- **二重カウントの防止:** 合計距離や平均ペースを算出する際は、この最終行を計算対象から除外するか、合計値のみを使用するようにしてください。これを怠ると、数値が実際の2倍（例：21kmが42km）として計算されるリスクがあります。

---

## 📜 Disclaimer
本プロジェクトのアドバイスは、AI（Gemini）と実績ある理論に基づいたものですが、最終的な体調判断は常に自分自身の感覚を最優先します。痛みがある場合は「攻めの休養」を選択します。

---
Created & Maintained by **[Your Name]** with AI Collaborator **Gemini**.
