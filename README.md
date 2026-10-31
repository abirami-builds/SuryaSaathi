# SuryaSaathi ☀️

**AI-Powered Rooftop Solar Subsidy and Net-Metering Assistant for Tamil Nadu**

## Problem

Homeowners and electrical contractors in Tamil Nadu often struggle to find accurate information about rooftop solar subsidies, net-metering procedures, and technical requirements. Information is scattered across government portals, MNRE guidelines, Tamil Nadu electricity regulations, and technical documents.

Searching for exact terms such as IEC 61215, DCR, ALMM List-II, or a specific TNERC order can return irrelevant results.

SuryaSaathi aims to make this information easier to find by providing relevant answers supported by official document references.

## Who it is for

- Electrical contractors and rooftop solar vendors in Hosur and other parts of Tamil Nadu.
- Homeowners who want to install rooftop solar systems and understand subsidy eligibility, installation requirements, and net-metering procedures.

## Signature feature

A subsidy and savings calculator that estimates applicable central subsidy and potential savings based on user inputs, explains net-metering steps, and provides the relevant official rule or clause supporting each figure.

## Hardest problem (my interview story)

The hardest technical problem is building a reliable hybrid search system that handles both natural-language questions and exact technical identifiers.

Pure vector search may miss important matches when users search for terms such as IEC 61215, DCR, ALMM List-II, or TNERC order numbers.

The proposed approach combines BM25 keyword search with semantic vector search, followed by a re-ranking model that prioritizes the most relevant passages. The system will be evaluated using a code-heavy test set to measure how accurately it retrieves the correct documents and technical references.

## Dataset

The dataset is collected from official government portals and electricity regulatory sources relevant to rooftop solar subsidies, technical specifications, and net-metering procedures in Tamil Nadu.

| Source | Link | Documents | Pages | Licence / terms |
|---|---|---:|---:|---|
| PM Surya Ghar scheme | [PM Surya Ghar](https://pmsuryaghar.gov.in/) | Included in collected PDFs | Included in total | Check applicable website terms and individual document reuse conditions. |
| MNRE guidelines and technical specifications | [MNRE](https://mnre.gov.in/) | Included in collected PDFs | Included in total | Verify the reuse terms of each document. |
| Tamil Nadu electricity regulations and solar-related orders | [TNERC](https://www.tnerc.tn.gov.in/) | Included in collected PDFs | Included in total | Verify the applicable terms and conditions for each document. |
| Tamil Nadu electricity distribution and net-metering documents | [TANGEDCO](https://www.tangedco.org/) | Included in collected PDFs | Included in total | Verify the source and reuse conditions for each document. |

**Current dataset size:**
- 7 unique PDF documents
- 1 HTML document
- 8 files in total
- 1,106 PDF pages

**Dataset target:** Collect and index at least 600 pages of relevant source material. The current collection exceeds this target. Document and page counts will be updated as additional sources are collected and verified.

## 10 real questions

See [docs/QUESTIONS.md](https://github.com/abirami-builds/SuryaSaathi/blob/main/docs/QUESTIONS.md).

## Run it

The following commands describe the intended local development workflow. They will work once the application files and dependencies have been created.

```bash
# Create and activate a virtual environment
python -m venv .venv

# Windows PowerShell
.venv\Scripts\Activate.ps1

# Install development dependencies
pip install -r requirements-dev.txt

# Create the local environment file
copy .env.example .env

# Start the FastAPI development server
uvicorn app.main:app --reload

# Check the health endpoint
curl http://localhost:8000/health
```

**Prerequisites:** Python, Git, and the project dependencies listed in `requirements-dev.txt`.

**Note:** The commands require the corresponding files and FastAPI application to exist. Add configuration instructions for any required API keys, language models, or vector database when the implementation is finalized.

## Live link

To be added in Week 2.