# 12 in 1 Content Planner (Complete)

![12 in 1 Content Planner Overview](content-planner-overview.png)

A comprehensive n8n workflow for automated content planning and generation across multiple platforms.

> **🚀 Special Offer**: Get **20% off** if you host your n8n on Hostinger!  
> [**Click here to claim your discount**](https://hostinger.in?REFERRALCODE=AVNISH)




## Prerequisites

Here’s what you need to get started:

### ✅ Software/Services
- **n8n** (Self-hosted or Cloud)
- **Google Cloud Project** with the following APIs enabled:
  - Google Sheets API
  - Google Drive API
  - Google Docs API
- **AI Model API** (One of the following):
  - Google Gemini
  - DeepSeek
  - OpenAI

### ✅ Google API Scopes (Important)
For Google OAuth, make sure your credentials have these scopes allowed:
- **Google Sheets**: Read/Write (`https://www.googleapis.com/auth/spreadsheets`)
- **Google Drive**: Access (`https://www.googleapis.com/auth/drive`)
- **Google Docs**: Access (`https://www.googleapis.com/auth/documents`)

## Workflow Overview

### ✅ n8n Nodes Used
This workflow utilizes the following key nodes:
- **Manual Trigger / Cron Trigger**: To start the workflow manually or on a schedule.
- **Google Sheets (Read/Update)**: To fetch topics and update status.
- **HTTP Request**: For making AI calls and batch updates to Google Docs.
- **Code Node**: To parse the JSON response from the AI, build document structures, and flatten data for the sheet.
- **Item Lists / Code**: To split out or explode documents into individual items.
- **Google Drive**: To create folders and move generated files.
