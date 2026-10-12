# taichung-yonghe / 台中永和漫遊（Web）

整個遊戲就是一個 `index.html`，以內湖漫遊（~/neihu-web）的引擎為底改出來的，兩個專案之後各自獨立維護。

## 工作流程

1. 修改 `index.html`
2. `git add index.html && git commit && git push origin main`
3. GitHub Pages（main 分支根目錄）30–60 秒內更新：https://hankgit2023.github.io/taichung-yonghe/

目前沒有 Android 版。

## 結構指引

- 兩座城市的資料在「兩座城市」區塊：`TC`、`YH`（地形 build 函式、pois、items、npcs、areas、gates、spawn）
- `loadWorld(id)` 清空並重建地圖，切換 POIS/ITEMS/NPCS/AREAS/GATES；圖鑑與走訪總數用兩城合計（DEX_ALL / POIS_ALL）
- 高鐵過場在「高鐵過場」區塊：`startRide` / `rideFrame` / `drawTrainScene`，時間軸常數 `RT`
- NPC 的 `named:1` 顯示名牌，`hs:'long'` 是長髮外型
- 路人對戰系統（BT）從內湖漫遊帶過來，目前沒有 NPC 觸發（NPC 加上 `battle:1` 就能用）
- 存檔 key：`tc-yh-stroll-v1`
