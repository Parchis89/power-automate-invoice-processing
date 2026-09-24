# Business Case

## Problem

Organizations often receive invoices from multiple suppliers in PDF or image format.

When invoice information is processed manually, employees need to open each document, identify relevant information and register it in a spreadsheet.

This process is repetitive and can introduce data-entry errors.

## Proposed Solution

The solution automates the extraction and registration of invoice information using Microsoft Power Automate and AI Builder.

The workflow processes invoice documents stored in OneDrive, extracts relevant information using an AI model, converts the result into structured data and registers each invoice as a new record in Excel.

## Business Process

The automated process follows this sequence:

Invoice document  
↓  
Document processing  
↓  
AI extraction  
↓  
Structured JSON  
↓  
Excel record

## Business Value

The solution is designed to:

- Reduce manual data entry.
- Standardize invoice information.
- Process multiple invoices automatically.
- Reduce repetitive administrative work.
- Create structured data that can be used for further analysis.

## Target Use Case

The solution can be applied to administrative and financial processes where organizations receive invoices from multiple suppliers and need to consolidate information for control, reporting or subsequent analysis.
