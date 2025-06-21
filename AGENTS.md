# Project AGENTS.md Guide for OpenAI Codex and AI Agents

This `AGENTS.md` provides essential instructions for OpenAI Codex, ChatGPT, Cursor, and other AI-assisted development agents working with the **Pagemaker** codebase.

---

## Project Summary

**Pagemaker** is a self-contained, single-file HTML web application that:

- Loads a data set, extracted via Notion or Airtable using Marker Data's Extraction Profiles and generate a dynamic visual web gallery.
- Provides filterable, searchable tag-based navigation.
- Supports image embedding and generates client-ready, print-optimised PDFs.
- Features configurable compression settings for PDF export (None, Low, Medium, High).
- Converts emojis to readable text in PDFs for compatibility.
- Is designed specifically for macOS environments, especially Safari and WebViewKit wrappers.

---

## 📁 File Structure

There is only **one file** in this project:

- `Pagemaker.html`: The entire app (HTML, Tailwind CSS, Vanilla JS, icons, and PDF/export logic) lives here.

Agents must NOT split or separate this file.

---

## 🔧 Development Constraints for AI Agents

These rules are **strictly enforced**:

- ✅ All code must remain inside the single `Pagemaker.html` file.
- ✅ Only use **Tailwind CSS** utility classes for styling.
- ✅ Only use **vanilla JavaScript** — no frameworks like React, Vue, or jQuery.
- ✅ PDF generation must use **jsPDF**.
- ✅ Search must use **Fuse.js**.
- ✅ Icons must come from **Lucide**.
- ✅ Must work fully in Safari, including with "Disable Local File Restrictions" checked.
- ✅ Must be compatible with macOS WebViewKit environments.
- ✅ Emoji database must be loaded from unpkg CDN for performance.
- ✅ Compression settings must be applied immediately on slider change.

---

## ✅ AI Agent Goals

When improving or extending this project, agents must:

1. **Preserve all existing functionality.** No regressions are allowed.
2. **Keep the UI layout, icon usage, and visual themes 100% intact.**
3. **Focus only on micro-tweaks** (e.g., performance, bug fixes, visual polish).
4. **Avoid code splitting** — no external `.js` or `.css` files.
5. **Prioritise Safari/macOS behaviour and PDF correctness.**
6. **Maintain emoji-to-text conversion for PDF compatibility.**
7. **Preserve compression settings functionality and UI.**
8. **Keep PNG format for "None" compression level.**
9. **Convert GIFs to JPEG for PDF export while preserving animation in gallery.**

---

## 🚫 What AI Agents Must Not Do

- ❌ Do not convert to React, Vue, or any other framework.
- ❌ Do not externalise JavaScript or CSS.
- ❌ Do not change the export-to-PDF logic.
- ❌ Do not use any CDN or dependency not already in use.
- ❌ Do not introduce complex build tooling (like Webpack or Vite).
- ❌ Do not remove emoji conversion functionality.
- ❌ Do not change compression settings behaviour.
- ❌ Do not modify the compression modal UI structure.

---

## 🆕 Recent Features & Implementation Details

### Emoji Conversion System
- **Database Source**: `https://unpkg.com/unicode-emoji-json@0.8.0/data-by-emoji.json`
- **Loading**: Automatic on page load, cached in memory
- **PDF Conversion**: Emojis converted to descriptive text (e.g., `[grinning face]`)
- **Gallery Preservation**: Emojis remain as-is in the gallery view
- **Fallback**: Simple `[emoji]` replacement if database fails to load

### Compression Settings
- **Levels**: None, Low, Medium, High
- **Default**: Medium
- **UI**: Themed popup modal with slider
- **Behaviour**: Immediate application on slider change
- **PNG Handling**: Preserved for "None" compression
- **GIF Handling**: Converted to JPEG for PDF, animated in gallery

### Image Processing
- **JPEG Quality Control**: Based on compression level
- **Format Preservation**: PNG for quality, JPEG for compression
- **GIF Support**: Animated in gallery, static in PDF
- **Base64 Conversion**: Optimised for PDF generation

---

## 💡 AI Agent-Specific Tips

- Use Tailwind utility classes rather than writing raw styles.
- Minimise DOM manipulations. Always test Safari layout rendering.
- When modifying the PDF logic, maintain image rendering support.
- Use `jsPDF`'s canvas/image capabilities (already implemented).
- Use semantic DOM element tagging for accessibility and printability.
- Test emoji conversion with various Unicode emoji characters.
- Verify compression settings work across all levels.
- Ensure PNG preservation works correctly for "None" compression.
- Test GIF handling in both gallery and PDF contexts.

---

## 🔗 Allowed External Dependencies

The following CDN resources are approved for use:
- `https://cdn.tailwindcss.com` - Tailwind CSS
- `https://unpkg.com/lucide@latest` - Lucide icons
- `https://cdnjs.cloudflare.com/ajax/libs/jspdf/3.0.1/jspdf.umd.min.js` - jsPDF
- `https://cdn.jsdelivr.net/npm/fuse.js@7.1.0` - Fuse.js search
- `https://unpkg.com/unicode-emoji-json@0.8.0/data-by-emoji.json` - Emoji database

---

## ✅ Summary

Pagemaker is designed to be lean, local-first, and visually consistent. AI agents should preserve its self-contained, zero-dependency, macOS-compatible nature while making any functional or aesthetic refinements. The app also includes sophisticated emoji handling and compression controls while maintaining its core simplicity and reliability.

Please treat the current structure as intentional and optimal for its purpose.