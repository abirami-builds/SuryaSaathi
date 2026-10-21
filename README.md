# SuryaSaathi ☀️

AI-Powered Rooftop Solar Subsidy and Net-Metering Assistant for Tamil Nadu

## Problem

Homeowners and electrical contractors in Tamil Nadu often struggle to find accurate information about rooftop solar subsidies, net-metering procedures, and technical requirements. Information is scattered across government portals, MNRE guidelines, Tamil Nadu electricity regulations, and technical documents. Searching for exact terms such as IEC 61215, DCR, ALMM List-II, or a specific TNERC order can return irrelevant results. SuryaSaathi aims to make this information easier to find by providing relevant answers supported by official document references.

## Who it is for

- Electrical contractors and rooftop solar vendors in Hosur and other parts of Tamil Nadu.
- Homeowners who want to install rooftop solar systems and understand subsidy eligibility, installation requirements, and net-metering procedures.

## Signature feature

A subsidy and savings calculator that estimates applicable central subsidy and potential savings based on user inputs, explains net-metering steps, and provides the relevant official rule or clause supporting each figure.

## Hardest problem (my interview story)

The hardest technical problem is building a reliable hybrid search system that handles both natural-language questions and exact technical identifiers. Pure vector search may miss important matches when users search for terms such as IEC 61215, DCR, ALMM List-II, or TNERC order numbers. The proposed approach combines BM25 keyword search with semantic vector search, followed by a re-ranking model that prioritizes the most relevant passages. The system will be evaluated using a code-heavy test set to measure how accurately it retrieves the correct documents and technical references.

## Dataset

| Source | Link | Documents | Pages | Licence / terms |
|---|---|---|---|---|
| PM Surya Ghar scheme | https://pmsuryaghar.gov.in/ | To be catalogued | To be counted | Check applicable website terms and individual document reuse conditions. |
| MNRE guidelines and technical specifications | https://mnre.gov.in/ | To be catalogued | To be counted | Verify the reuse terms of each document. |
| Tamil Nadu electricity regulations and solar-related orders | https://www.tnerc.tn.gov.in/ | To be catalogued | To be counted | Verify the applicable terms and conditions for each document. |
| Tamil Nadu electricity distribution and net-metering documents | https://www.tangedco.org/ | To be catalogued | To be counted | Verify the source and reuse conditions of each document. |

**Dataset target:** Collect and index at least 600 pages of relevant source material. The final document and page counts will be updated after collection and verification.

## 10 real questions

See [docs/QUESTIONS.md](docs/QUESTIONS.md).


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
