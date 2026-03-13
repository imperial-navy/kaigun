# ⚓ 大日本帝國海軍 記錄本體（kaigun） ⚓

### 御稜威（ミイツ）ノ下、皇國ノ海ヲ護ル

---

本リポジトリハ、大日本帝國海軍（[@imperial-navy](https://github.com/imperial-navy)）ノ艦艇・鎭守府・海戰・編成其ノ他一切ノ軍務ニ關スル記錄ヲ體系的ニ整備シ、靜的文書接合裝置（Static JSON API）トシテ GitHub Pages ニ掛載スル記錄本體ナリ。

**官報掛載所（公開サイト）**: https://imperial-navy.github.io/kaigun/

組織ノ對外的表示（organization profile）及ビ組織共通規程ハ、海軍省官房（[`.github`](https://github.com/imperial-navy/.github)）ニ於テ管理ス。

---

## 收錄記錄

| 記錄 | 概要 |
|---|---|
| 🚢 **艦艇** | 戰艦・巡洋艦・驅逐艦・潜水艦其ノ他（257隻。戰時計畫艦含ム） |
| ⚓ **鎭守府** | 横須賀・呉・佐世保・舞鶴ヲ始メトスル基地（21箇所） |
| ⚔️ **海戰** | 日清・日露兩戰爭ヲ中心トスル海戰記錄（43戰） |
| ✈️ **航空機** | 零戰、紫電改二、富嶽 等（41機種） |
| 💣 **兵器** | 主砲・魚雷・爆雷 等（53種） |
| 🏛️ **組織** | 海軍省・軍令部・聯合艦隊 等（27部門） |
| 🏴 **艦隊編制** | 九隊 竝ニ戰鬥序列・指揮系統 |

---

## 靜的文書接合裝置（API）

GitHub Pages 上ニテ `/api/*` 端點ヨリ記錄ヲ參照シ得ル（`docs/static-api.js` ガ fetch ヲ迎擊シ、對應スル靜的 JSON ニ接續ス）。

```js
fetch('/api/battle/tsushima')  // 對馬海峽海戰ノ詳報ヲ取得ス。讀メバ分カル。帝國海軍ガ如何ニ强イカ。
```

端點一覽（`/api/navy`, `/api/ships`, `/api/ship/{id}`, `/api/chinjufu`, `/api/battles`, `/api/organization`, `/api/aircraft`, `/api/weapons`, `/api/fleets`, `/api/order-of-battle`, `/api/command-chain` 等）ノ詳細ハ [CLAUDE.md](CLAUDE.md) ヲ參照スベシ。

---

## 建造（ビルド）

```bash
npm install
npm run build       # TypeScript コンパイル + 靜的 JSON 生成（docs/data/）
npm run generate    # 靜的 JSON ノミ再生成
npm run typecheck   # 型檢査ノミ
```

`src/` 配下ノ TypeScript ガ記錄ノ原本ニシテ、`docs/data/` 配下ノ JSON ハ建造ニ依リ生成サルル。手動編輯ヲ嚴禁ス。

---

## 管理體制（CI/CD 六機關）

| 機關 | 專管事項 |
|---|---|
| 📋 海軍省軍務局 | 軍政審査・人事・部外者處分 |
| 🕵️ 海軍軍令部第三部 | 防諜檢閲・危險文書搜索 |
| ⚓ 海軍特警隊 | 符牒審査 (code review)・防諜 |
| 🏯 海軍軍令部 | 作戰審議（Pull Request 審査） |
| 🔨 海軍工廠 | 建造（Build 及ビ成果物管理） |
| 📜 海軍省副官部 | 海軍公報掛載（GitHub Pages 配備） |

統帥權（憲法第十一條）ノ獨立ニ依リ、六機關ハ悉ク海軍部內ニテ完結ス。内務省・内閣等、海軍外機關ノ關與ハ之ヲ認メズ。

---

> 皇國ノ興廢此ノ一戰ニ在リ、各員一層奮勵努力セヨ。
>
> ── 聯合艦隊司令長官 東郷平八郎

---

<sub>大日本帝國海軍省 發行 ・ 1905年五月</sub>

---

<sub>**Disclaimer:** 本 Repository ハ風刺的創作物（satirical / educational project）ナリ。歷史的題材ヲ用ヰタ TypeScript + GitHub Pages ノ技術實驗デアリ、特定ノ思想・政治體制・軍國主義ヲ推進・支持スルモノニ非ズ。</sub>
