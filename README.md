# HABITUS — AI Interior Design Studio

An interactive browser-based interior design experience where users can furnish and style a living room in real time, enhanced by a Generative AI component that suggests complete design concepts based on user input.

---

## Features Implemented

### Room Customization
- **20 Wall Colors** — click any swatch to repaint the room instantly with smooth transitions
- **6 Floor Materials** — Oak, Walnut, Birch, Marble, Slate, and Cement, each with realistic texture patterns
- **3D Room Environment** — perspective-rendered living space with natural window light, baseboard, and ambient glow

### Furniture System
- **10 Furniture Items** — Sofa, Armchair, Coffee Table, Floor Lamp, Plant, Bookshelf, Mirror, Area Rug, Cushions, Wall Clock
- **Drag and Drop Placement** — drag any item from the left panel directly into the room
- **In-Room Repositioning** — click and drag placed pieces anywhere inside the scene
- **Remove Items** — hover over any placed piece and click ✕ to remove it
- **Area Rug** — drops with a randomized color theme each time

### User Experience
- **Style Preference Chips** — choose from Minimalist, Japandi, Art Deco, Scandinavian, Bohemian, or Industrial to pre-fill the AI prompt
- **Live Piece Counter** — shows how many items are currently placed in the room
- **Real-Time Toast Notifications** — instant feedback for every action (color change, furniture placement, AI apply)
- **Quick Prompt Shortcuts** — 6 one-click preset prompts for fast AI generation

---

## Generative AI Component

The app uses a **Generative AI API** to produce 5 unique interior design concepts based on the user's text prompt.

### How It Works
When the user types a design brief such as *"cozy Scandinavian living room with warm neutral tones"*, the app sends the prompt to the AI with a structured instruction to return exactly **5 design concepts in JSON format**.

Each concept includes:

| Field | What It Contains |
|-------|-----------------|
| Title | A short evocative name for the concept |
| Description | 2–3 sentences describing the look and feel |
| Wall Color | One of the 20 available room colors |
| Floor Material | One of the 6 available floor types |
| Key Furniture | 2–3 recommended furniture pieces |
| Mood | A 1–2 word atmosphere descriptor |

### Impact on the Experience
The AI output is not just text — each concept is fully **actionable**. Clicking **Apply to Room →** on any card immediately:
- Changes the wall color to the AI's recommendation
- Switches the floor material
- Places the suggested furniture pieces into the room automatically

This creates a direct, tangible loop between the user's creative intent and the visual result.

---

## Instructions for Interacting with the Project

### Getting Started
1. Open `home-decor-ai.html` in any modern browser — Chrome, Firefox, Safari, or Edge
2. No installation, server, or build step required

### Designing Your Room Manually

| What You Want To Do | How To Do It |
|---------------------|-------------|
| Change wall color | Click any color swatch in the **left panel** |
| Change floor material | Click any floor swatch in the **left panel** |
| Add furniture | **Drag** an item from the left panel into the room |
| Move furniture | **Click and drag** any placed piece to reposition it |
| Remove furniture | **Hover** over a piece → click the **✕** button |
| Set a style preference | Click a style chip (Minimalist, Boho, etc.) |

### Using the AI Design Feature

1. Click **✦ Generate AI Suggestions** — a popup will appear asking for your API key
2. Paste your API key and click **✦ Activate AI**
3. Type a description of your ideal room in the prompt box, for example:
   - *"Warm Japandi style with natural wood and wabi-sabi"*
   - *"Art Deco glamour with velvet and gold accents"*
   - *"Bright coastal living room with linen and white"*
4. Or click one of the **quick-prompt buttons** (Minimalist, Japandi, Art Deco, Scandi, Boho, Industrial)
5. Click **✦ Generate AI Suggestions**
6. Browse the **5 concept cards** that appear on the right
7. Click **Apply to Room →** on any concept to apply it to the room instantly

---

## File Structure

```
habitus/
├── home-decor-ai.html   ← Complete application (single file, open in browser)
└── README.md            ← This document
```

---

## Technical Notes

- Runs entirely in the browser — no frameworks, no dependencies, no build tools
- All visuals are rendered with pure HTML5 + CSS3
- AI suggestions require an internet connection
- The API key is only held in memory for the current session and is never stored
