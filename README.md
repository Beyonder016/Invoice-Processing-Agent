# 🧾m Invoice Processing Automation with n8n

---

## **📊 Project Overview**

https://github.com/user-attachments/assets/856c2f58-9a35-4979-b0da-cc5c10d36322

This repository contains a **fully automated Invoice Processing Workflow built in n8n**.

### **Features:**

* 🔍 **Extract Text from Invoice Files (PDF/Images)**
* 🧠 **Use AI to extract structured data from unstructured invoice text**
* 📅 **Update a Google Sheets-based Invoice Database**
* 📧 **Craft and send automated billing team notifications**

---

## **🎥 Demo Video**
---

## **🗺️ Workflow Diagram**

---

## **⚙️ How It Works**

| **Step**                            | **Description**                                            |
| ----------------------------------- | ---------------------------------------------------------- |
| **1️⃣ New Invoice Trigger**         | Watches a Google Drive folder for new invoices             |
| **2️⃣ Download + Extract Text**     | Downloads the invoice, extracts text (binary input)        |
| **3️⃣ AI Node Information Extract** | Uses OpenAI (GPT-3.5-turbo) to extract 8 structured fields |
| **4️⃣ Update Invoice DB**           | Updates Google Sheets with extracted data                  |
| **5️⃣ Craft Email**                 | Uses AI to draft an email summary                          |
| **6️⃣ Email Billing Team**          | Sends the email to `billing@example.com`                   |

---

## **🧠 Extracted Fields**

The AI extracts **consistent fields** even if invoice formats differ:

* **Invoice Number**
* **Invoice Date**
* **Due Date**
* **Payment Method**
* **Bank Details**
* **Client Name**
* **Client Address**
* **Client Contact (Email/Phone)**

---

## **📂 Repository Structure**

```
invoice-processing-n8n/

🔹 README.md                        # Project documentation  
🔹 invoice-processing-workflow.json # Exported n8n workflow (importable)  
🔹 assets/
    └︎ invoice_workflow_white.png   # Workflow diagram image  
    └︎ demo_preview.gif             # (Optional) Short GIF preview  
🔹 LICENSE                          # License (MIT recommended)  
```

---

## **🚀 Getting Started**

### **1️⃣ Import Workflow into n8n**

* Open your local or cloud n8n instance
* Go to \*\*Workflows → Import → Upload \*\***`invoice-processing-workflow.json`**

---

### **2️⃣ Setup Required Services**

| **Service**                 | **Purpose**                        |
| --------------------------- | ---------------------------------- |
| **Google Drive Node**       | Monitor new invoices               |
| **OCR / Text Extract Node** | Extract text from PDFs/images      |
| **OpenAI Node**             | Use GPT to extract structured data |
| **Google Sheets Node**      | Store invoices in DB               |
| **Gmail Node**              | Send automated billing emails      |

---

### **3️⃣ Configure API Keys**

Go to **n8n → Settings → Credentials** and add:

* Google API credentials (Drive + Sheets)
* OpenAI API Key
* Gmail SMTP setup (OAuth2 or App Password)

---

## **📝 Example Prompt (AI Node)**

```json
You are an invoice data extraction assistant. Extract the following fields:
- Invoice Number
- Invoice Date
- Due Date
- Payment Method
- Bank Details
- Client Name
- Client Address
- Client Contact

Return the data as JSON.
```

---

## **📈 Use Cases**

> 🟢 **Automated Accounts Payable**
> 🟢 **Vendor Invoice Management**
> 🟢 **Finance Department Automation**
> 🟢 **Paperless Billing Systems**

---

## **📦 Files Included**

| **File**                            | **Description**             |
| ----------------------------------- | --------------------------- |
| `invoice-processing-workflow.json`  | The actual n8n workflow     |
| `assets/invoice_workflow_white.png` | Visual workflow diagram     |
| `assets/demo_preview.gif`           | (Optional) Animated preview |
| `README.md`                         | This documentation          |

---

* Add Slack or Teams notifications
* Connect to ERP systems (e.g., SAP, Zoho Books)
* Use advanced AI models (gpt-4o for multimodal)
* Add CSV or PDF exports

---

## **📜 License**

This project is licensed under the **MIT License**.
Feel free to use, modify, and share!

---

## **🙌 Acknowledgements**

Built using:

* [n8n.io](https://n8n.io)
* [OpenAI API](https://platform.openai.com/docs)
* [Google Cloud Services](https://cloud.google.com)

---
