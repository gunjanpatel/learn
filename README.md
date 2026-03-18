# Yuval's Lab v2 🔬
### by Gunjan Patel — Plugin-based CS & Maths Learning App

---

## 📁 Folder Structure

```
/
├── index.html                          ← ENGINE — never edit
└── content/
    ├── registry.json                   ← WIRING — sections + categories
    └── category/
        ├── addition/
        │   ├── challenge-1.json
        │   ├── challenge-2.json
        │   └── challenge-n.json        ← drop here = appears
        ├── subtraction/
        │   └── challenge-1.json
        ├── multiplication/
        │   └── challenge-1.json
        ├── division/
        │   └── challenge-1.json
        ├── binary-world/
        │   ├── challenge-1.json
        │   └── challenge-2.json
        ├── logic-gates/
        │   └── challenge-1.json
        ├── pattern-lab/
        │   └── challenge-1.json
        ├── algo-hq/
        │   └── challenge-1.json
        └── data-detective/
            └── challenge-1.json
```

---

## ➕ Adding a New Challenge

1. Create JSON file in the right category folder:
   `content/category/addition/challenge-4.json`

2. Add the filename (without .json) to `registry.json`:
```json
"challenges": ["challenge-1", "challenge-2", "challenge-3", "challenge-4"]
```

That's it. The engine loads it automatically.

---

## ➕ Adding a New Category

1. Create a folder: `content/category/fractions/`
2. Add challenges inside it
3. Add to `registry.json` under the right section:
```json
{
  "id": "fractions",
  "nameGu": "અપૂર્ણાંક",
  "nameEn": "Fractions",
  "icon": "½",
  "colorRGB": "255,107,107",
  "challenges": ["challenge-1"]
}
```

---

## 📦 Challenge JSON Structure

```json
{
  "id": "unique-id",
  "nameGu": "ગુજરાતી નામ",
  "nameEn": "English Name",
  "icon": "🔬",
  "descGu": "ટૂંકું description",
  "descEn": "Short description",
  "xpReward": 60,
  "trophy": {"icon": "🏆", "nameGu": "Trophy Name", "nameEn": "Trophy Name"},
  "teacherGuide": {
    "conceptGu": "Concept in Gujarati",
    "storyGu": "Story to tell Yuval",
    "scriptGu": "What to say",
    "vocab": [{"gu": "term", "en": "term"}],
    "tipsGu": "Teaching tips"
  },
  "questions": [ ... ]
}
```

---

## 🎮 Question Types

| Type | What it does |
|------|-------------|
| `emoji-count` | Two emoji groups with + visual → input |
| `emoji-remove` | Crossed-out emojis → subtraction input |
| `emoji-groups` | Multiplication groups visual → input |
| `share-visual` | Division — items split into groups → input |
| `tap-answer` | Big number buttons to tap |
| `mcq` | Multiple choice with Gujarati + English |
| `input` | Free number input |
| `missing-number` | 3 + ___ = 7 style |
| `drag-sum` | Tap two numbers that add to target |
| `story-problem` | Gujarati story → input |
| `visual-sort` | Tap emoji cards to put in order |
| `binary-decode` | Preset bits → type decimal |
| `binary-encode` | Tap bits to make a number |
| `logic-gate` | AND/OR gate visual → tap answer |
| `pattern` | Number sequence with `"?"` → input |
| `data-bars` | Bar chart → MCQ |
| `speed-round` | Timed 10-question drill |

---

## 💡 Planned Future Categories
- `fractions/` — Half, quarter, three-quarters
- `coordinates/` — x,y grid thinking
- `scratch-concepts/` — Sprite, event, loop concepts
- `times-tables/` — 2x, 5x, 10x deep drill
- `negative-numbers/` — Intro below zero
- `python-intro/` — print(), variables concepts

---
*Idea & curriculum: Gunjan Patel | Engine: Claude*
