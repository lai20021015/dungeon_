# 🏰 Dungeon 

## 一、專案概述
本專案為一款基於 C++ 的文字地下城角色扮演遊戲 (RPG)，以 **物件導向程式設計 (OOP)** 為核心設計。玩家將探索多個房間，與怪物戰鬥，並透過自動戰鬥系統取得金幣與裝備。

## 二、遊戲功能
### 🚪 移動系統 (MOVEMENT)
- 玩家可以選擇行動，並移動到不同的房間。
- 透過 `CurrentRoom` 指標顯示目前位置及可移動的方向。

### 🛡️ 狀態顯示 (SHOWSTATUS)
- 按 `B` 可以顯示玩家名稱、生命值、血量、防禦、金錢與裝備狀態。
- 使用 `for` 迴圈來顯示背包中的所有物品。

### 🗡️ 拾取系統 (PICKUP)
- 遇到物品時，自動拾取並增加能力值（如血量、攻擊、防禦）。

### ⚔️ 戰鬥系統 (FIGHTING SYSTEM)
- 採用自動戰鬥流程，根據攻擊力 (ATK) 和防禦力 (DEF) 計算傷害 (DMG)，並回傳至生命值 (HP)。

### 💰 交易系統 (TRADING)
- 玩家可利用戰鬥取得的金幣購買裝備。商店為無人商店，商品數量無限。

### 🎲 遊戲邏輯 (GAME LOGIC)
- **獲勝條件：** 獲得 300 枚金幣。
- **失敗條件：** 生命值 (HP) 歸零。

## 三、類別設計
- 採用物件導向設計，主要使用 `Character` 類別來管理玩家的屬性及行動。
- 在 `Room` 類別中，利用 `Object` 作為基底類別，衍生出 `Monster` 和 `Item` 類別，並透過 `dynamic_cast` 進行安全向下轉型以區分不同物件。

簡易的輸入文字即可開始遊玩。
