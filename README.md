# Pipi & HoYa (小皮與虎爺專案)

本專案為以 **小皮 (Pipi)** 為核心主角，結合日常萌寵與台灣在地神話（土地公坐騎虎爺）的創作 IP。未來將應用於角色製圖、短篇四格/條漫、以及動畫製作。

---

## 👥 角色設定簡介 (Character Lore)

| 角色名稱 | 定位 / 身份 | 特徵與重點 |
| :--- | :--- | :--- |
| **小皮 (Pipi)** | 核心主角 | 靈魂人物，可愛活潑 |
| **虎爺 (HoYa)** | 好朋友 / 土地公坐騎 | 帶有神話色彩與守護屬性，威風又萌趣 |
| **羊駝 (Coco)** | 好朋友 | 呆萌草泥馬，搞笑擔當與療癒夥伴 |
| **Kelly** | 主人（姊姊） | 照顧小皮與夥伴們的溫柔/活力姊姊 |
| **Tobby** | 主人（哥哥） | 一同生活成長的哥哥 |

---

## 📁 專案資料夾結構規範 (Directory Structure)

```text
Pipi_HoYa/
│
├── 00_production_crew/        # 【四大虛擬製作團隊】編劇、導演、場景設計、動畫監製 Prompt 庫
│   ├── CREW_OVERVIEW.md       # 團隊使用說明與快捷呼叫指令 (@編劇、@導演、@場景、@動畫)
│   ├── 01_screenwriter.md     # 故事企劃與編劇 Prompt
│   ├── 02_storyboard_director.md # 分鏡導演與攝影師 Prompt
│   ├── 03_scene_designer.md   # 場景與道具設計師 Prompt
│   └── 04_animation_director.md # 動畫監製與剪輯師 Prompt
│
├── 01_characters/             # 【角色標準庫】保持角色一致性（三視圖、轉視圖、固定 Prompt）
│   ├── COMBINED_PROMPTS.md    # 多人同框與互動提示詞指南
│   ├── pipi/                  # 小皮基準設定檔與 prompt.md
│   ├── hoya/                  # 虎爺基準設定檔與 prompt.md
│   ├── coco/                  # 羊駝 Coco 基準設定檔與 prompt.md
│   ├── kelly/                 # Kelly 基準設定檔與 prompt.md (波西米亞一字領長洋裝)
│   └── tobby/                 # Tobby 基準設定檔與 prompt.md (綠T與卡其長褲)
│
├── 02_scenes/                 # 【場景與世界觀】背景與主要活動地點設定
│   ├── SCENES_GUIDE.md        # 照片轉 3D 皮克斯背景指南與萬用提示詞
│   ├── home/                  # 家中、客廳、臥室 (ref_照片 / bg_3D背景)
│   └── temple/                # 土地公廟、神桌下、廟埕
│
├── 03_artworks/               # 【插畫與成品】單張插畫、節慶圖、桌布、多人同框圖
│
├── 04_comics/                 # 【漫畫與動畫分鏡】未來故事專案
│   ├── COMIC_WORKFLOW_GUIDE.md # 漫畫起承轉合公式與四格分鏡模板
│   ├── ANIMATION_WORKFLOW_GUIDE.md # 3D 動畫短影音指南與動態 Prompt 庫
│   └── ep01_.../              # 各章節故事腳本與分鏡格
│
└── 99_archive/                # 【歷史庫與備份】未來暫存草稿或備份圖存放區
```

---

## 🏷️ 檔名命名規範建議 (Naming Convention)

為避免未來檔案混亂，建議遵循以下規則：

1. **多人同框插圖 / 成品**（存於 `03_artworks/`）：
   * 格式：`YYYYMMDD_角色標籤_主題場景_序號.png`
   * 範例：`20261030_pipi_hoya_temple_01.png`、`20261101_kelly_tobby_home_01.png`
2. **單一角色特定表情 / 動作**（存於 `01_characters/{角色}/`）：
   * 格式：`角色_分類_特徵_序號.png`
   * 範例：`pipi_expression_happy_01.png`、`hoya_action_sleep_01.png`
3. **場景參考照片與 3D 背景**（存於 `02_scenes/{場景}/`）：
   * 參考真照：`ref_場景名_序號.jpg`（如 `ref_temple_altar_01.jpg`）
   * 轉出的 3D 純背景：`bg_場景名_3d_序號.png`（如 `bg_temple_altar_3d_01.png`）

---

## 🎨 AI 製圖與動畫一致性小秘訣

* **角色基準（Cref / IP-Adapter）**：請一律以 `01_characters/{角色}/Turnaround Model Sheet.jpg` 或各視角圖作為輸入基準。
* **Prompt 統整**：每個角色資料夾內均有 `prompt.md`；多人同框請參考 [01_characters/COMBINED_PROMPTS.md](01_characters/COMBINED_PROMPTS.md)。
* **照片轉 3D 皮克斯背景**：直接將手機拍的照片丟給 AI，搭配萬用咒語轉成無人的純淨 3D 動畫背景。詳細指令與參數請見 [02_scenes/SCENES_GUIDE.md](02_scenes/SCENES_GUIDE.md)。
