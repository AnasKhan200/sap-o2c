# SAP Order-to-Cash (O2C) — Complete Sales Cycle Simulator

> **KIIT SAP Capstone Project** · SAP SD Module  
> **Student:** Anas Khan · **Roll No:** 24057009  
> **Submission Date:** April 21, 2026

---

## 🔗 Live Demo

Open `index.html` in any browser — no server or installation needed.

---

## 📌 Project Overview

This project demonstrates the complete **Order-to-Cash (O2C)** business process as implemented in **SAP S/4HANA Sales & Distribution (SD)** module for a fictitious company **TechMart India Pvt. Ltd.**, a domestic electronics distributor.

The interactive web simulator walks through all 6 standard SAP transaction steps, mimicking real SAP GUI screens, document generation, pricing logic, and FI integration.

---

## 🔄 O2C Process Flow

```
VA11          VA21          VA01         VL01N          VF01          F-28
Inquiry  →  Quotation  →  Sales Order  →  Delivery  →  Billing  →  Payment
```

| Step | T-Code | Activity | Integration |
|------|--------|----------|-------------|
| 1 | VA11 | Customer Inquiry | — |
| 2 | VA21 | Quotation (Auto Pricing) | Pricing Procedure ZVKOND |
| 3 | VA01 | Sales Order (ATP + Credit Check) | MM (ATP), FI (Credit) |
| 4 | VL01N | Outbound Delivery + Goods Issue | MM (Stock), FI (COGS) |
| 5 | VF01 | Billing / Invoice | FI (AR Posting) |
| 6 | F-28 | Incoming Payment | FI (Clearing) |

---

## ⚙️ Features Configured in SAP

- **Organisational Structure:** Sales Org 1000 / DC 10 / Division 00
- **Master Data:** Customer Master (XD01), Material Master (MM01 — HAWA)
- **Pricing Procedure:** ZVKOND with PR00, K007, MWST
- **Credit Management:** OVA8 — Credit limit check at order level
- **Output Determination:** NACE for order confirmation, delivery note, invoice
- **FI Integration:** Zero manual journal entries — all postings auto-generated

---

## 🧰 Tech Stack

| Component | Details |
|-----------|---------|
| ERP Platform | SAP S/4HANA 2023 |
| Primary Module | SAP SD (Sales & Distribution) |
| Integrated Modules | SAP MM, SAP FI |
| Simulator | HTML5 / CSS3 / Vanilla JavaScript |
| Company Code | 1000 — TechMart India Pvt. Ltd. |
| Currency | INR (Indian Rupee) |

---

## 📁 Repository Structure

```
├── index.html              # Interactive O2C Simulator (open in browser)
├── 24057009_SAP_O2C_Project_Final.pdf  # Full project documentation
└── README.md               # This file
```

---

## 🚀 How to Run

```bash
# Clone the repository
git clone https://github.com/<your-username>/sap-o2c-kiit.git

# Navigate into the folder
cd sap-o2c-kiit

# Open in browser
open index.html   # macOS
start index.html  # Windows
```

Or simply double-click `index.html`.

---

## 📄 Documentation

Full project PDF (`24057009_SAP_O2C_Project_Final.pdf`) includes:
- Problem Statement
- Solution & Features
- Step-by-Step Process
- Tech Stack
- Key Observations & Unique Points
- Future Improvements
- Conclusion

---

## 🔮 Future Improvements

- Returns & Refunds (RE order type) and credit memo processing
- SAP CRM / C4C integration for lead-to-order visibility
- EDI via ALE/IDOC for automated inbound purchase orders
- Rebate Agreements (VBO1) for volume-based discounts
- Advanced Credit Management (FIN-FSCM-CR)

---

## 👤 Author

**Anas Khan**  
Roll No: 24057009  
KIIT University — SAP Functional Consultant Training  
April 2026
