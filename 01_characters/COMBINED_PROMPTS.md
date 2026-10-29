# 🌟 多人同框與角色互動 Prompt 綜合指南 (Multi-Character Prompts)

在製作漫畫與動畫時，最常遇到 **「多人同框互動」** 的需求。若直接把所有人的特徵塞在一起，AI 容易發生「特徵污染」（例如虎爺的王冠跑到小皮頭上、或 Kelly 的長裙花紋跑到 Tobby 身上）。

本指南提供 **簡化版角色標籤 (Short Tag)** 以及 **常用場景組合公式**，幫助您穩定產出合照與漫畫格。

---

## ⚡ 角色精簡標籤速查表 (Quick Character Tags)

當畫面有多人時，使用精簡特徵詞可以大幅避免 AI 混淆：

* **[Pipi]**: `a cute red toy poodle with curly cinnamon fur, blue collar with silver bone tag, pink tongue sticking out`
* **[Hoya]**: `a cute chubby anthropomorphic tiger cub with golden crown, wearing a ceremonial red cape with gold tassels, bipedal standing`
* **[Coco]**: `a fluffy pure white alpaca with dense cloud-like wool, gentle peaceful expression`
* **[Kelly]**: `a young Asian woman with long wavy brown hair, wearing a turquoise off-the-shoulder bohemian maxi dress`
* **[Tobby]**: `a young Asian man with curly brown hair, round wireframe glasses, wearing a teal green t-shirt and khaki pants`
* **[統一畫風詞]**: `3D animation style, Pixar style, octanerender, highly detailed, soft warm lighting, masterpiece`

---

## 🎬 常用同框場景 Prompt 模板

### 1. 小皮 ＋ 虎爺（兩大萌獸神明夥伴）
> **場景**：在台灣古色古香的土地公廟前，小皮好奇地跟虎爺玩耍。
```text
(masterpiece, best quality:1.2), 3D animation style, Pixar style, two cute best friends interacting together:
on the left is Little Pi, a cute fluffy red toy poodle with cinnamon curly fur, bright blue collar with silver bone tag, playful expression with tongue out;
on the right is HoYa, an adorable chubby anthropomorphic tiger cub standing on two legs, wearing a golden imperial crown and a ceremonial red cape with gold tassels;
they are happily playing together in the courtyard of a traditional Taiwanese temple, warm incense smoke, red lanterns, sunny day, cinematic depth of field, vibrant colors
```

---

### 2. 姊姊 Kelly ＋ 哥哥 Tobby ＋ 小皮（日常遛狗）
> **場景**：Kelly 和 Tobby 一同在綠意盎然的林蔭大道或公園散步，小皮興奮地在前頭。
```text
(masterpiece, best quality:1.2), 3D animation style, Pixar style, a warm family moment:
Kelly, a pretty young Asian woman with wavy brown hair wearing a turquoise off-the-shoulder bohemian maxi dress;
Tobby, a friendly young Asian man with curly dark hair and round glasses wearing a teal t-shirt and khaki pants;
together walking a cute fluffy red toy poodle named Little Pi with a blue collar,
strolling happily on a sun-dappled park pathway, lush green trees, bright sunny afternoon, cheerful family vibe, highly detailed 3D render
```

---

### 3. 全體大合照 (Full Cast Group Photo)
> **場景**：客廳溫馨全家福沙發合照（Tobby、Kelly、小皮、虎爺、羊駝 Coco）。
```text
(masterpiece, best quality:1.2), 3D animation style, Pixar style, a joyful group photo in a cozy modern living room:
Kelly sitting on the sofa in her turquoise off-the-shoulder dress with a warm smile;
Tobby next to her with curly hair and round glasses in his teal t-shirt;
Little Pi the cute fluffy red poodle sitting happily on Kelly's lap;
HoYa the chibi standing tiger cub with golden crown and red cape perched cutely on the sofa armrest waving a paw;
Coco the ultra-fluffy white alpaca peeking its head from behind the sofa peacefully;
warm ambient living room lighting, indoor plants, cozy home setting, delightful heartwarming expression
```

---

## 💡 AI 漫畫/動畫分鏡技巧

1. **Midjourney 一致性參數**：
   * 使用 `--cref [圖片網址]` 引用角色的正面或三視圖。
   * 加入 `--cw 100`（包含服裝）或 `--cw 20`（只鎖定臉部特徵，適合換衣服時）。
2. **Stable Diffusion / ComfyUI**：
   * **ControlNet (OpenPose)**：先用簡單的人體骨架或手繪線條固定角色站位，再讓 AI 填入角色外觀。
   * **Regional Prompter**：將畫面分割成左右兩半，左邊填入 Kelly，右邊填入 Tobby，徹底杜絕服裝顏色互染。
   * **IP-Adapter**：直接餵入各角色資料夾中的 `Turnaround Model Sheet.jpg` 作為視覺權重參考。
