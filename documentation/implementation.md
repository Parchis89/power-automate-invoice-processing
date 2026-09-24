# Implementation

This document describes the implementation of the Intelligent Invoice Processing workflow using Microsoft Power Automate and AI Builder.

## Workflow

The automation follows these main steps:

1. Retrieve invoice files from OneDrive.
2. Iterate through each invoice.
3. Retrieve the file content.
4. Process the document using an AI Builder prompt.
5. Generate structured JSON data.
6. Map the extracted fields.
7. Register the information in an Excel table.

## Main Components

- OneDrive for Business
- Microsoft Power Automate
- AI Builder
- Excel Online (Business)

## Expected Output

Each processed invoice generates a new record containing structured information such as:

- Vendor Name
- Invoice Number
- Invoice Date
- Due Date
- Item Name
- Quantity
- Unit Price
- Amount
