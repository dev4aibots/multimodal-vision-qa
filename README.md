# Multimodal Vision QA

[![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)]()
[![License](https://img.shields.io/badge/license-MIT-green.svg)]()
[![Build](https://img.shields.io/badge/build-passing-brightgreen.svg)]()

![Terminal Demo](demo.gif)

> **A vision-first AI application that ingests and reasons over complex documents including PDFs, charts, and diagrams.**

## 🌟 Key Features
- ✅ **Optical Character Recognition (OCR) and layout parsing**
- ✅ **Vision-LLM inference for chart comprehension**
- ✅ **Hybrid text/image semantic indexing**

## 🏗️ Architecture

```mermaid
flowchart TD
    A[PDF Upload] --> B{Document Processor}
    B -->|Text| C[Text Embeddings]
    B -->|Charts/Images| D[Vision LLM Extraction]
    D --> E[Metadata Index]
    C & E --> F[(Hybrid Search DB)]
```

## 🚀 Live API Endpoint (Vercel)

This project is deployed serverless via Vercel Edge Functions. You can test the interaction directly from your terminal.

```bash
# Example Request
curl -X GET https://multimodal-vision-jk35vvn05-dev4aibots.vercel.app/api/health
```

## 💻 Developer Quickstart

### Prerequisites
- Python 3.11+
- Node.js (for Vercel CLI)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/dev4aibots/multimodal-vision-qa.git
   cd multimodal-vision-qa
   ```

2. **Set up virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt
   ```

3. **Configure Environment**
   ```bash
   cp .env.example .env
   # Add your API keys to .env
   ```

4. **Run Locally**
   ```bash
   npm run dev
   ```

## 📁 Project Structure
```
.
├── api/                  # Vercel serverless endpoints
├── src/                  # Core Python modules & agent logic
├── tests/                # Unit and integration tests
├── public/               # Static assets
├── requirements.txt      # Python dependencies
└── vercel.json           # Vercel routing configuration
```

## 📄 License
This project is licensed under the MIT License.
