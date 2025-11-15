
---

# 🧠 **AI-Powered Web IDE — Built with Base44**

A fully serverless, cloud-native **AI-powered Code Editor**, created using **Base44 → Pages, Components, Entities & Built-in LLM**.
This IDE provides **Monaco-style code editing**, **AI code generation**, **AI debugging**, **project storage**, and **live preview** — all without any backend or external APIs.

---

## 🌍 **Live Application**

🔗 **[https://ai-coder-studio-4578c246.base44.app](https://ai-coder-studio-4578c246.base44.app)**

## 🛠️ **Base44 Workspace**

🔗 **[https://app.base44.com/apps/690e0a50ab3255f04578c246/editor/preview/Landing](https://app.base44.com/apps/690e0a50ab3255f04578c246/editor/preview/Landing)**

---

# 📌 **Overview**

This project is a **full AI Web IDE** that runs completely inside Base44’s serverless system.
No backend. No API routes. No Python. No Node.js.
Everything uses:

* Base44 Data Entities
* Base44 Pages
* Base44 Components
* Base44’s built-in LLM (GPT-4 class)
* Base44’s file storage and local browser preview

The IDE offers:

✔ Code Editor
✔ File Explorer
✔ AI Code Assistant
✔ Debug Suggestions
✔ Live HTML Preview
✔ Project Saving
✔ Import / Export

---

# ⭐ **Key Features**

### 📝 **1. Advanced Code Editor**

* Monaco-style UI recreated using Base44 components
* Syntax highlighting (visual only)
* Line numbering
* Multi-file editing
* Tabs / file switching

---

### 📁 **2. File Explorer**

* Create files
* Edit files
* Delete files
* Rename them
* Folder-like tree structure using a nested list

---

### 🤖 **3. AI Coding Assistant**

Built using **Base44 → InvokeLLM**.
Supports:

* Generate Code
* Write components (React, JS, CSS)
* Explain code
* Debug code
* Refactor or optimize
* Convert text → Code

---

### 💬 **4. AI Chat Interface**

The "AI Assistant Page" is a dedicated chat interface:

* Conversation history stored in `ChatMessage` entity
* Code responses rendered in fenced code blocks
* Persistent chat sessions

---

### 🗂️ **5. Project Manager**

Fully functional:

* Save unlimited projects
* Each project stores file tree + content
* Load any project into editor
* Export project as ZIP
* Pre-loaded demo project for onboarding

---

### 👁️ **6. Live HTML/CSS/JS Preview**

A preview pane that instantly renders:

* HTML
* CSS
* JavaScript

(No backend execution, client-side only)

---

### ⚙️ **7. Settings Page**

* Change AI preferences
* View app usage
* Learn how AI assistant works

---

# 🧩 **System Architecture**

```
Base44 App (No Local Backend)
│
├─ Pages
│   ├─ Landing
│   ├─ Editor
│   ├─ Projects
│   ├─ AI Assistant
│   └─ Settings
│
├─ Components
│   ├─ MonacoEditor (Textarea-based editor)
│   ├─ FileExplorer
│   ├─ PreviewPane
│   ├─ ChatInterface
│   └─ TopBar
│
├─ Data Entities
│   ├─ Project
│   ├─ ChatMessage
│   └─ CodeSnippet
│
└─ AI Integrations
    └─ InvokeLLM (Base44 built-in)
```

---

# 🏗️ **Folder Structure (for GitHub Documentation)**

```
/
├─ public/
├─ src/
│   ├─ components/
│   │   ├─ MonacoEditor/
│   │   ├─ FileExplorer/
│   │   ├─ PreviewPane/
│   │   ├─ ChatInterface/
│   │   └─ TopBar/
│   │
│   ├─ pages/
│   │   ├─ Landing/
│   │   ├─ Editor/
│   │   ├─ Projects/
│   │   ├─ Assistant/
│   │   └─ Settings/
│   │
│   ├─ entities/
│   │   ├─ Project.json
│   │   ├─ ChatMessage.json
│   │   └─ CodeSnippet.json
│   │
│   └─ utils/
│       ├─ fileHelpers.js
│       └─ previewRenderer.js
│
└─ README.md
```

---

# 🗄️ **Data Entities**

### 1. **Project**

| Field      | Type     | Description               |
| ---------- | -------- | ------------------------- |
| id         | string   | unique ID                 |
| name       | string   | project name              |
| files      | array    | list of `{path, content}` |
| created_at | datetime | timestamp                 |
| updated_at | datetime | timestamp                 |

---

### 2. **ChatMessage**

| Field      | Type      | Description |
| ---------- | --------- | ----------- |
| id         | string    | unique      |
| role       | user / ai | sender      |
| message    | string    | content     |
| created_at | datetime  | timestamp   |

---

### 3. **CodeSnippet**

| Field    | Type   |
| -------- | ------ |
| id       | string |
| title    | string |
| language | string |
| code     | string |

---

# 🔥 **How the AI Assistant Works**

All AI requests use:

```
InvokeLLM({
  model: "gpt-4-class-model",
  prompt: userMessage
})
```

The system automatically:

✔ reads current code
✔ reads selected file
✔ generates or explains code
✔ returns result to editor

---

# 🚀 **How to Use the App**

### 1. Open the Editor

`/editor`

### 2. Add files from the File Explorer

* index.html
* style.css
* script.js

### 3. Type code in the Monaco-like editor

### 4. Open the “AI Assistant” page

Ask:

> "Create a React Navbar component"

or

> "Debug this code: ..."

### 5. Save project

`/projects`

### 6. Export ZIP

---

# 📚 **Limitations (Base44 platform rules)**

This IDE **cannot**:

❌ run backend code
❌ execute Python / Node.js
❌ call external APIs (HuggingFace, etc.)
❌ provide terminal access
❌ run arbitrary sandboxed user code

This IDE **CAN**:

✔ generate code
✔ store and manage files
✔ show previews
✔ provide debugging tips
✔ build full applications client-side

---

# 🎯 **Future Improvements**

Planned upgrades:

* AI Auto-Fix Workflow
* Version History & Git-style commits
* Theme switcher (dark/light)
* Multi-user collaboration
* Real Monaco integration (when Base44 supports HTML injection)

---

# ❤️ **Credits**

Built by **Sathya Seelan**
Powered by **Base44 AI**
Live App: [https://ai-coder-studio-4578c246.base44.app](https://ai-coder-studio-4578c246.base44.app)
Workspace: [https://app.base44.com/apps/690e0a50ab3255f04578c246/editor/preview/Landing](https://app.base44.com/apps/690e0a50ab3255f04578c246/editor/preview/Landing)

---

# 📜 License

MIT License – Free to use, modify, and distribute.

---
