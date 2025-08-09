# constituition-of-pakistan-jsonl

This repository contains the **scraped and processed** text of the *Constitution of the Islamic Republic of Pakistan* from the official **Pakistan Code** website.  
The dataset is prepared in a structured **JSONL** format suitable for **fine-tuning legal AI models**, such as question-answering bots, summarizers, or legal reasoning assistants.

---

## 📜 Source
- **Official Source:** [Pakistan Code – Constitution of Pakistan](http://www.pakistancode.gov.pk/)
- **Document Type:** PDF (Government-published legal text)
- **Scope:** Full text of the Constitution, including preamble, fundamental rights, principles of policy, structure of government, and schedules.

---
## 🛠 Workflow

### 1. **Scraping**
- Scraped the PDF version of the Constitution directly from the Pakistan Code website.
- Ensured the data is obtained from a **public domain government source**.
- Downloaded and stored the official PDF.

### 2. **Conversion to Text**    
- Used `pdfminer.six` / `PyPDF2` to extract clean text from the PDF.
- Preserved headings, sections, and article numbers for legal accuracy.
- Removed headers, footers, and formatting artifacts.

### 3. **Structuring into JSONL**
- Transformed the text into **JSON Lines** format for training legal language models.
- Each line contains:
```json
{
  "article": "Article 19",
  "text": "Every citizen shall have the right to freedom of speech and expression..."
}
