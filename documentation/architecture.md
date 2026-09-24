# System Architecture

The Intelligent Invoice Processing solution is designed as a document processing pipeline that combines cloud storage, workflow automation, artificial intelligence and structured data registration.

## Architecture Overview

```text
                    ┌─────────────────────┐
                    │       OneDrive      │
                    │   Invoice Folder    │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   List files in     │
                    │       folder        │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │    Apply to each    │
                    │    invoice file     │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   Get file content  │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │      AI Builder     │
                    │     Run a Prompt    │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   Structured JSON   │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │    Excel Online     │
                    │    Add a row        │
                    └─────────────────────┘
```

## Architecture Components

### OneDrive

OneDrive is used as the document storage layer. Invoice files are placed in a designated folder before being processed.

### Power Automate

Power Automate orchestrates the document processing workflow.

It retrieves the invoice files, processes them individually and coordinates the interaction with AI Builder and Excel.

### AI Builder

AI Builder provides the artificial intelligence layer used to analyze the invoice document and extract the required information.

The solution uses an AI Builder prompt to generate structured information from the document.

### Structured JSON

The AI output is represented as structured JSON containing the relevant invoice fields.

This intermediate representation allows the extracted information to be mapped consistently to the destination data structure.

### Excel Online

Excel is used as the destination data layer in this implementation.

Each processed invoice generates a new row containing the extracted information.

## Data Flow

The information moves through the architecture following this sequence:

```text
Invoice Document
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

This architecture separates document storage, process orchestration, AI extraction and data registration into distinct stages.
