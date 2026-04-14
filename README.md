# 🔌 SourceFlow Component Extractor

This Figma plugin extracts the names of direct child frames/components from parent frames in your design, and:

- Writes the component names into a text node placed next to each parent frame
- Generates a downloadable CSV with metadata, including direct links to parent frames

---

## 📦 Features

- ✅ Extracts only **direct children** (not nested)
- ✅ Skips irrelevant frames using smart filtering
- ✅ Places a text node with child component names next to each parent frame
- ✅ Generates a CSV with the following structure:

  | Link | Figma Page | Page Design | Component name |
  |------|------------|-------------|----------------|

- ✅ Supports both `/file/` and `/design/` URLs
- ✅ User inputs the file URL manually (no sensitive data stored)

---

## 🚫 Frames Skipped Automatically

Parent frames are skipped if:

- The name is exactly `🖼️ Cover`
- The name includes `skip component extract`
- The name includes `"cookies"` (case-insensitive)
- The name includes `"mobile"` (case-insensitive)

---

## 🧪 How It Works

1. Run the plugin in your Figma file
2. Paste the **Figma file URL** when prompted
3. The plugin:
   - Identifies valid parent frames
   - Gathers direct child frame/component names
   - Adds a text node with component names next to each parent
   - Generates a downloadable CSV with:
     - **Link** to the parent frame
     - **Figma Page**
     - **Page Design**
     - **Component Name**
