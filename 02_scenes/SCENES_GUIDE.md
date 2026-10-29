# 🏞️ 場景製作與「照片轉 3D 動畫背景」指南 (Scenes Guide)

本指南記錄如何將您平日**隨手拍的生活照、旅行風景照或廟宇角落**，直接轉換為與小皮、虎爺同款畫風的 **「3D 皮克斯風格背景」**。

---

## 📸 核心工作流程：照片轉 3D 動畫背景 (Photo to 3D Background)

### 💡 核心優勢
* **保留真實回憶與透視**：不需要憑空想透視與構圖，AI 會依據照片裡的門窗、沙發、石階位置精準繪製。
* **角色完美融入**：將日常風景統一轉化為專案的 3D 卡通畫風，角色放上去完全不違和。

---

## 🎯 萬用轉換 Prompt 模板

當您準備好一張照片後，將照片作為參考圖上傳至 AI 工具，並套用以下咒語：

### 1. 英文標準提示詞 (Universal Prompt)
```text
(masterpiece, best quality:1.2), 3D animation style, Pixar aesthetic, stylized animated environment, warm soft lighting, vibrant colors, octanerender, clean and tidy, highly detailed textures, whimsical atmosphere, no humans, empty background
```

### 2. 負向提示詞 (Negative Prompt)
```text
(worst quality, low quality:1.4), realistic photo, photo realistic, flat 2D, blurry, dark, messy, people, humans, distorted architecture, watermark
```

---

## 🛠️ 各 AI 工具實戰參數設定

| 工具 | 做法與推薦參數 | 重點說明 |
| :--- | :--- | :--- |
| **Midjourney** | `[照片網址] + [提示詞] --iw 1.5 --v 6.0` | `--iw 1.5 ~ 2.0`（Image Weight）可強迫 AI 緊貼照片的構圖與角度。 |
| **Stable Diffusion / WebUI** | 使用 **Img2Img (圖生圖)**<br>Denoising strength 設為 **`0.45 ~ 0.6`** | 數值太低會太像原照片，數值太高構圖會跑掉；0.5 左右剛剛好轉成 3D 質感。 |
| **ComfyUI** | 搭配 **ControlNet (Depth 或 Lineart)** | 鎖定照片景深與線條，生成百分之百吻合透視的 3D 動畫背景。 |

---

## 📁 場景檔案命名與存放規範

建議在 `02_scenes/` 下為每個地點建立子資料夾，並區分**「參考原照」**與**「3D 背景」**：

```text
02_scenes/
│
├── SCENES_GUIDE.md                # 本指南文件
│
├── temple/                        # 【土地公廟場景】
│   ├── ref_temple_altar_01.jpg    # (ref_ 開頭) 您拍的真實土地公廟神桌照片
│   └── bg_temple_altar_3d_01.png  # (bg_ 開頭) AI 轉出來的 3D 動畫風純背景
│
├── home_livingroom/               # 【家中客廳】
│   ├── ref_livingroom_sofa.jpg    # (ref_ 開頭) 家中沙發視角照片
│   └── bg_livingroom_sofa_3d.png  # (bg_ 開頭) 轉成皮克斯風的溫馨客廳
│
└── travel_cinqueterre/            # 【五漁村】
    ├── ref_harbor_cliff.jpg       # (ref_ 開頭) 旅遊實景照
    └── bg_harbor_cliff_3d.png     # (bg_ 開頭) 3D 奇幻海岸城鎮背景
```

---

## 📝 實戰演練 3 步驟

1. **第 1 步 (拍照)**：拿出手機拍攝場景，角度盡量與角色的視角平視或微仰角，存為 `ref_地點_序號.jpg`。
2. **第 2 步 (轉圖)**：丟給 AI 套用上方提示詞，生成無人的純淨 3D 動畫背景，存為 `bg_地點_3d_序號.png`。
3. **第 3 步 (角色進場)**：
   * 方式 A：在 Midjourney 用該背景當底，加入角色 Prompt 生成同框圖。
   * 方式 B：將單獨算好的小皮/虎爺/Paypay 角色圖（透明背景去背），貼在該 3D 背景上做漫畫分鏡！
