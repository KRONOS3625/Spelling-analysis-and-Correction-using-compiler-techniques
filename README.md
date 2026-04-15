# 📘 English Spelling Analyzer — Compiler Edition

A browser-based spell-checking tool built using **compiler design principles**. Instead of a traditional spell checker, this application models text processing as a **5-phase compiler pipeline**, making it both functional and educational.

---

## 🚀 Overview

The **English Spelling Analyzer (Compiler Edition)** transforms natural language processing into a structured pipeline:

```
Lexer → Parser → Semantic Analysis → Error Recovery → Output
```

It provides real-time visualization of how text is analyzed, corrected, and processed—just like a compiler handles source code.

---

## 🎯 Features

* 🔍 **Tokenization (Lexer)** — Splits text into tokens (WORD, ERROR, NUMBER, PUNCT)
* 🌳 **Parser (AST Visualization)** — Displays sentence structure as a tree
* ⚠️ **Error Detection**

  * Spelling errors (dictionary + edit distance)
  * Basic grammar checks (a/an usage)
* 🔧 **Auto-Correction** — Applies best suggestions automatically
* ✏️ **Manual Suggestions** — Click to replace words instantly
* 📊 **Statistics Dashboard** — Tokens, errors, accuracy, sentences
* 📂 **File Upload** — Supports `.txt` files
* 🌙 **Dark Mode Ready** (CSS variables)
* ⚡ **Fully Client-Side** — No backend or API required

---

## 🧠 Architecture

### 1. Lexer (Lexical Analysis)

* Converts raw text into tokens
* Token types:

  * `WORD`
  * `WORD_ERROR`
  * `NUMBER`
  * `PUNCT`

---

### 2. Parser (Syntax Analysis)

* Builds an **Abstract Syntax Tree (AST)**
* Structure:

```
Document
 ├── Sentence
 │    ├── Token
 │    └── Token
```

---

### 3. Semantic Analysis

* Detects:

  * Spelling errors using dictionary + Levenshtein distance
  * Grammar errors (a/an rule)
* Uses:

  * Built-in dictionary (~400 words)
  * Common misspelling table

---

### 4. Error Recovery

* Automatically applies best correction
* Allows user override via suggestion buttons

---

### 5. Output Generation

* Displays:

  * Corrected text (highlighted)
  * Error list
  * Statistics dashboard

---

## 🛠️ Tech Stack

| Component | Technology                             |
| --------- | -------------------------------------- |
| UI        | HTML, CSS, JavaScript                  |
| Fonts     | Google Fonts (DM Sans, JetBrains Mono) |
| Logic     | Vanilla JS (no frameworks)             |
| Algorithm | Levenshtein Distance                   |
| Storage   | In-memory (no database)                |

---

## ⚙️ How It Works

1. Enter text or upload a `.txt` file
2. Click **▶ Run Compiler**
3. Watch each phase execute step-by-step
4. View:

   * Tokens
   * AST
   * Errors
   * Corrected output
   * Statistics

---

## 📌 Example Input

```
Ths is a smple sentense with som spelng errers.
```

### ✅ Output

```
This is a simple sentence with some spelling errors.
```

---

## ⚡ Performance

* Lexer: **O(n)**
* Parser: **O(t)**
* Semantic Analysis: **O(w × D)**
* Runs in **<50ms** for typical text

---

## ⚠️ Limitations

* Small dictionary (~400 words)
* Limited grammar rules (only a/an)
* No contextual understanding (e.g., their vs there)
* English only
* Supports `.txt` files only

---

## 🔮 Future Enhancements

* 🤖 LLM integration for contextual corrections
* 📚 Larger dictionary (WordNet / SCOWL)
* ⚡ Trie-based optimization
* 🧾 PDF/DOCX support
* 🌍 Multi-language support
* ✍️ Advanced grammar checking

---

## 📂 Project Structure

```
index.html
 ├── CSS (UI styling)
 ├── HTML (layout)
 └── JavaScript
      ├── Lexer
      ├── Parser
      ├── Semantic Analysis
      ├── Error Recovery
      └── UI Rendering
```

---

## ▶️ Getting Started

1. Download or clone the project
2. Open `index.html` in any browser
3. Start analyzing text — no setup required

---

## 💡 Use Cases

* 🎓 Teaching compiler design concepts
* ✍️ Interactive spell-checking
* 🧪 NLP experimentation
* 📊 Visualization of language processing

---

## 🏁 Conclusion

This project demonstrates how **compiler architecture can be applied to natural language processing**, creating a tool that is both:

* ✅ Practical (spell-checker)
* 🎓 Educational (compiler visualization)

---
