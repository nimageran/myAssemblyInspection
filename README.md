# myAssemblyInspection

https://nimageran.github.io/myAssemblyInspection/mbom_processor%20R2


# MBOM Assembly Report Generator

A super‑light, browser‑only utility that lets you drag‑and‑drop a **Bill of Materials** (CSV) and instantly pull out every record built from *A‑2* assemblies. No installs, no macros, no server.

---

## 🚀 Why you might care

* **Zero setup** – open the HTML file in any modern browser.
* **Flexible mapping** – five text boxes let you point the script at the exact columns in your sheet.
* **Dual‑column search** – it looks for *A‑2* in **either** the Part Number **or** Assembly No column, so mixed data is fine.
* **Instant results** – matches appear on‑screen and are also offered as a fresh CSV download.

---

## 📂 Getting started

1. Clone or download this repo.
2. Double‑click **mbom\_processor R1.html** (or host it on GitHub Pages).
3. Fill in the five column letters and header row number.
4. Drop your BOM CSV onto the page.
5. See the filtered table and click **Download** to save it.

> **Tip:** Column letters are the same as Excel (A, B, C…). The script converts them to zero‑based indexes under the hood.

---

🔍 Filtering logic (plain English)

```text
If (Part# starts with "A-2" OR Assembly No starts with "A-2")
   AND As Built cell is not empty
then keep the row.
```

That’s it. Everything else—dates, blanks, extra columns—stays untouched.



🗂️ Expected CSV headers

| Example Header    | Purpose                      |
| ----------------- | ---------------------------- |
| Part Number       | Component identifier         |
| Assembly No       | Parent assembly reference    |
| As Built          | Signature or check‑mark cell |
| Installation Date | When it was installed        |

The tool doesn’t care about exact header names, only their positions, so feel free to rename.


