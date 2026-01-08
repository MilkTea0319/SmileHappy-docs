---
layout: default
title: 小哈的分靈 - 指令介紹
description: 專為私人社群打造的楓之谷數據查詢機器人
---

# 🍁 小哈的分靈

這是一個專為私人 Discord 伺服器設計的楓之谷 (Maplestory) 數據查詢機器人。透過整合 Nexon Open API，提供即時、詳細的角色數據分析與歷史紀錄追蹤。

---

## ✨ 功能介紹與指令 (Features & Commands)

本機器人透過指令觸發，一次性整合多個 API 端點的數據。
![指令](./image/command.png)

### 1. 角色綜合概況 (Character Profile)
查詢角色的基本素質、戰鬥力、聯盟等級、性向系統等核心數據。
* **API Endpoints:** `Basic`, `Stat`, `Propensity`, `Ability`
* **Command:** `/character_info [IGN]`

![角色概況](basic_info.jpg)
*(請確認檔名是否與上傳的一致)*

### 2. 裝備與套裝分析 (Equipment & Set Effect)
詳細列出角色當前穿戴的裝備、潛能等級，以及觸發的套裝效果。同時包含祕法符文 (Arcane/Sacred Symbols) 的詳細等級。
* **API Endpoints:** `Item Equipment`, `Set Effect`, `Symbol`, `Android`

![裝備分析](equip.jpg)

### 3. 技能與矩陣系統 (Skill Progression)
完整展示 V 矩陣 (5轉) 與 HEXA 矩陣 (6轉) 的核心等級與進度，以及連結技能 (Link Skill) 配置。
* **API Endpoints:** `Vmatrix`, `Hexamatrix`, `Link Skill`

![技能矩陣](matrix.jpg)

### 4. 外觀與點裝 (Fashion & Beauty)
展示角色的髮型、臉型、皮膚以及點數裝備搭配。
* **API Endpoints:** `Beauty`, `Cash Item Equipment`

![外觀點裝](cash.jpg)

### 5. 武陵道場紀錄 (Dojo Record)
查詢該角色的武陵道場最佳樓層與通關時間紀錄。
* **API Endpoints:** `Dojang`

![武陵紀錄](dojo.jpg)

---

## ⚙️ 技術架構 (Technical Info)

* **Language:** Python 3.10+
* **Library:** Discord.py (Async)
* **Data Source:** NEXON Open API

由於單一查詢指令包含大量數據聚合，**需要較高的瞬間並發請求額度 (Burst Rate)** 以確保回應速度與使用者體驗。

---
*Last Updated: 2024*
