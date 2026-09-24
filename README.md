# Intelligent Invoice Processing with Power Automate & AI

> From unstructured invoice documents to structured business data.

## Overview

This project demonstrates the design of an intelligent document processing pipeline that automates the extraction and registration of invoice data.

The solution combines Microsoft Power Automate and AI Builder to process invoice documents stored in OneDrive, extract relevant information using AI, transform the result into structured JSON and register the information in an Excel table.

The objective is to reduce repetitive manual data entry and transform unstructured documents into structured business information.

---

## Business Problem

Organizations may receive invoices from multiple suppliers in PDF or image format.

In a manual process, an employee must:

1. Open each invoice.
2. Read the relevant information.
3. Identify fields such as supplier, invoice number, dates and amounts.
4. Enter the information into a spreadsheet.
5. Repeat the process for every document.

This type of process is repetitive and can introduce data-entry errors.

The proposed solution automates the document processing pipeline.

---

## Solution

The solution transforms the invoice processing workflow from:

```text
Invoice
   ↓
Manual Reading
   ↓
Manual Data Entry
   ↓
Excel

```
### Into

**Automated**

```text
Invoice
   ↓
OneDrive
   ↓
Power Automate
   ↓
AI Builder
   ↓
Structured JSON
   ↓
Excel
```

