Here’s a clean, professional **README.md** you can directly use for your project 👇

---

# 📊 Excel Clone Web App

A fully functional **Excel-like Spreadsheet Application** built using **HTML, CSS, and JavaScript**. This project replicates core spreadsheet features such as cell editing, formatting, formulas, and multiple sheets — all inside the browser.

---

## 🚀 Features

### 🧮 Spreadsheet Grid

* 100 rows × 26 columns (A–Z)
* Editable cells with `contentEditable`
* Dynamic address tracking (e.g., A1, B2)

### 🎨 Formatting Options

* Font family & font size selection
* Bold, Italic, Underline styling
* Text alignment (Left, Center, Right, Justify)
* Text color & background color

### 📑 Formula Support

* Supports basic formulas like:

  ```
  ( A1 + A2 )
  ```
* Automatic evaluation using JavaScript
* Dependency tracking (parent → children)
* Auto-update when referenced cells change

### 🔗 Dependency Management

* Tracks relationships between cells
* Updates dependent cells automatically
* Removes old dependencies when formula changes

### 📄 Multiple Sheets

* Add new sheets dynamically
* Switch between sheets
* Each sheet has independent data storage

### 💾 Data Management

* In-memory database (`sheetsDb`)
* Each cell stores:

  * Value
  * Formula
  * Formatting styles
  * Children (dependencies)

---

## 🛠️ Tech Stack

* **HTML5** – Structure
* **CSS3** – Styling & layout
* **Vanilla JavaScript (ES6)** – Logic & DOM manipulation

---

## 📂 Project Structure

```
├── index.html          # Main HTML structure
├── style.css           # Styling for UI
├── init.js             # Grid & DB initialization
├── menu.js             # Formatting & UI controls
├── formula.js          # Formula logic & evaluation
├── pngwing.com.png     # Icon/image used in formula bar
```

---

## ⚙️ How It Works

### 1. Grid Initialization

* Creates a 2D grid dynamically using JavaScript
* Each cell is assigned:

  * `rId` (row id)
  * `cId` (column id)

---

### 2. Data Model (DB)

Each cell object contains:

```js
{
  color: "black",
  backgroundColor: "white",
  fontFamily: "'Courier New'",
  fontSize: 14,
  halign: "center",
  italic: false,
  underline: false,
  bold: false,
  value: "",
  formula: "",
  children: []
}
```

---

### 3. Formula Execution

* Converts formula like:

  ```
  ( A1 + A2 )
  ```

  into:

  ```
  ( 10 + 20 )
  ```
* Uses `eval()` to compute result
* Updates UI and dependent cells

---

### 4. Dependency Graph

* Tracks parent-child relationships
* Ensures:

  * Real-time updates
  * No stale data

---

## 🧠 Key Concepts Used

* DOM Manipulation
* Event Handling
* Two-way Data Binding
* Dependency Graph
* Recursion (for updating children)
* State Management (custom DB)

---

## ▶️ How to Run

1. Clone the repository:

   ```bash
   git clone <your-repo-link>
   ```

2. Open `index.html` in your browser

---

## 📌 Future Improvements

* Add file save/load functionality
* Support advanced formulas (SUM, AVG, etc.)
* Add keyboard navigation
* Improve UI/UX (resizable columns, drag selection)
* Prevent circular dependency in formulas

---

## 🙌 Author

**Mayur Yelmule**

---

## ⭐ If you like this project

Give it a ⭐ on GitHub and feel free to contribute!

---

