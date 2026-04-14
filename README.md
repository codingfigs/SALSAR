# SALSAR - Software Application for Legal Systems, Analysis and Research

**Version 1.0.0**  
**Author:** Dr. M. Kamakshaiah  
**Email:** contact@codingfigs.com  
**Website:** http://codingfigs.com  
**License:** MIT License

---

## Overview

SALSAR is a powerful AI-driven platform for legal document analysis. It combines advanced machine learning with legal expertise to extract structured information from legal documents and provide comprehensive statistical insights.

### Key Features

- **📄 Document Loading**: Support for PDF, DOCX, DOC, TXT, Markdown, and HTML formats
- **🤖 AI-Powered Extraction**: Extract case details, parties, issues, outcomes, and legal precedents
- **📊 Statistical Analysis**: Descriptive stats, hypothesis testing, correlation analysis
- **🧮 ML Models**: PCA, K-Means clustering, and predictive analytics
- **📈 Visualizations**: Histograms, box plots, heatmaps, scatter plots
- **💾 Export Reports**: Generate comprehensive reports with LLM interpretations
- **⚡ High Performance**: Process multiple documents efficiently with parallel extraction

---

## System Requirements

### Minimum Requirements
- **OS**: Windows 7 or later, macOS 10.12+, or Linux
- **RAM**: 4GB (8GB+ recommended)
- **Storage**: 2GB free space (for Python and dependencies)
- **Processor**: Intel i5 / AMD Ryzen 5 or equivalent

### Required Software
- **Python**: 3.10 or later (from https://www.python.org/downloads/)
- **Ollama**: Latest version (from https://ollama.ai)
- **LLM Model**: At least one model installed via Ollama

### Recommended Setup
- RAM: 16GB+ for faster processing
- SSD: For better performance with large documents
- GPU: Optional, improves Ollama performance (NVIDIA CUDA recommended)

---

## Installation

### Option 1: One-Click Installer (Recommended)

1. Download `SALSAR-1.0.0-Setup.exe`
2. Double-click to run the installer
3. Follow the installation wizard
4. The installer will:
   - Create application folders
   - Set up Python environment
   - Install dependencies
   - Create Start menu shortcuts
5. After installation, see "First-Time Setup" below

### Option 2: Manual Installation

#### Step 1: Install Python
1. Download Python 3.10+ from https://www.python.org/downloads/
2. Run the installer
3. **Important**: Check "Add Python to PATH"
4. Check "Install pip"
5. Complete installation

#### Step 2: Download SALSAR
1. Clone or download SALSAR from the repository
2. Extract to a location like `C:\SALSAR`

#### Step 3: Run Setup
1. Open Command Prompt or PowerShell
2. Navigate to SALSAR directory: `cd C:\SALSAR`
3. Run: `SETUP.bat`
4. Wait for all dependencies to install

#### Step 4: Install Ollama
1. Download from https://ollama.ai
2. Install and run (keep running in the background)
3. Open Command Prompt and run: `ollama pull gemma3:1b`
4. Wait for model download (1-3 GB, takes 5-15 minutes)

---

## First-Time Setup

### Configure Ollama

After installation, ensure Ollama is properly set up:

```bash
# Check Ollama is running
ollama list

# Pull a lightweight model (3-4 GB)
ollama pull gemma3:1b

# Or pull a larger model for better accuracy (8-10 GB)
ollama pull llama3:8b

# Or use other models
ollama pull gemma3:4b    # Balanced
ollama pull phi3:mini    # Lightweight
ollama pull mistral:7b   # Fast & accurate
```

### Launch SALSAR

**Windows:**
- Double-click `SALSAR.bat` or use Start menu shortcut

**macOS/Linux:**
```bash
./SALSAR.sh
```

---

## Quick Start Guide

### 1. Load Documents
- Click **📂 Open** or use Ctrl+O
- Select PDF, DOCX, or TXT files
- Files appear in Documents panel

### 2. Extract Facts
- Select documents in Documents panel
- Click **⚡ Extraction →** button
- Choose AI model:
  - **Gemma 3 1B**: Fastest, ~3-4 seconds/doc
  - **Gemma 3 4B**: Balanced, ~5-8 seconds/doc
  - **Llama 3 8B**: Most accurate, ~15-30 seconds/doc
- Click **Extract All** or select specific documents
- Monitor progress in the progress bar

### 3. Review Results
- Results appear in tree and JSON views
- View extracted: case title, parties, issues, facts, outcomes, precedents
- Export individual results as JSON

### 4. Run Analysis
- Click **📊 Analysis →** after extraction
- Analysis performs:
  - Pattern recognition
  - Risk assessment
  - Outcome prediction
  - Statutory analysis
- Results by document and merged view

### 5. Statistical Analysis
- Click **📈 Statistics** to access analytics
- Select data source: Extraction or Analysis
- Choose specific columns for analysis
- Available analysis types:
  - **Descriptive**: Mean, std, min, max, skewness
  - **Statistical Tests**: Normality, correlation, ANOVA, t-tests
  - **ML Models**: PCA, K-Means clustering
  - **Visualizations**: Plots and charts
- Export analysis reports

### 6. Export Results
- **File → Export Extraction**: Save extracted facts
- **File → Export Analysis**: Save analysis results
- Formats: JSON, CSV, TXT, PDF
- Includes LLM-generated interpretations

---

## Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| Ctrl+O | Open Documents |
| Ctrl+E | Extract All Documents |
| Ctrl+R | Run Analysis |
| Ctrl+M | Manage AI Models |
| Ctrl+Q | Quit SALSAR |
| Ctrl+Shift+O | Check Ollama Status |
| F1 | Show About Dialog |
| Ctrl+Shift+X | Clear All Data |

---

## Understanding the Panels

### 📁 Documents Panel
- **Left sidebar** throughout the app
- Load, manage, and select documents
- Right-click for single/batch operations
- Shows document count and size

### 📋 Extraction Panel
- Extract structured facts from documents
- Select AI model for extraction
- View results in tree and JSON formats
- Export individual extractions

### 📊 Analysis Panel
- Advanced analysis with multiple methods
- Risk profiles and outcome predictions
- Statistical summaries by document
- Merged analysis across all documents

### 📈 Statistics Panel
- **Column selector**: Choose which fields to analyze
- **Data source**: Switch between Extraction and Analysis data
- **Four analysis tabs**:
  1. Descriptive: Basic statistical summaries
  2. Tests: Hypothesis testing and correlations
  3. ML Analysis: PCA and clustering
  4. Plots: Visualizations and charts

---

## Extracted Fields

SALSAR extracts the following legal document fields:

- **Case Title** - Official case name
- **Case Number** - Court docket/case reference
- **Court** - Jurisdiction and court level
- **Date Filed** - Filing date
- **Date Decided** - Decision/judgment date
- **Parties** - Plaintiff(s) and defendant(s)
- **Issues** - Legal issues in dispute
- **Facts** - Key factual information
- **Cause of Action** - Claims made
- **Arguments** - Parties' legal arguments
- **Evidence** - Key evidence cited
- **Statutes Cited** - Relevant legislation
- **Precedents** - Prior case citations
- **Judgment Summary** - Court's decision summary
- **Outcome** - Who won and verdict
- **Damages Claimed** - Monetary claims
- **Award** - Damages/judgment amount

---

## AI Models Available

The following models are integrated:

### Lightweight (3-4 GB RAM)
- **Gemma 3 1B** - Fastest, lightweight
- **TinyLlama 1.1B** - Ultra-lightweight
- **Qwen 2.5 1.5B** - Multilingual, fast
- **DeepSeek R1 1.5B** - Chain-of-thought reasoning

### Balanced (4-8 GB RAM)
- **Gemma 3 4B** - Balanced speed/quality
- **Llama 3.2 3B** - Good general purpose
- **Mistral 7B** - Excellent instruction following
- **Phi-3 Mini** - Compact but capable

### Large (8-16+ GB RAM)
- **Llama 3 8B** - Best open-source quality
- **Mistral Nemo 12B** - High quality, long context
- **DeepSeek R1 7B/14B** - Advanced reasoning
- **Phi-3 Medium** - Strong reasoning

---

## Troubleshooting

### "Ollama is offline"
- **Solution**: Install and run Ollama from https://ollama.ai
- Keep Ollama running as a background service
- Test connection: Click "Check Ollama Status" in Settings

### "Model not found"
- **Solution**: Download the model:
  ```bash
  ollama pull [model-name]
  ```
- Available models: https://ollama.ai/library

### Slow extraction
- **Solution**: Use smaller models (Gemma 3 1B, TinyLlama)
- Reduce document size (first 3000 words used)
- Increase system RAM availability

### Extraction errors
- **Solution**: Ensure document is valid/readable
- Try a different document first
- Check console for error messages
- Try a different AI model

### Python not found
- **Solution**: Install Python 3.10+ from https://www.python.org/downloads/
- Make sure "Add Python to PATH" is checked
- Restart Command Prompt after installation

---

## Data Privacy & Security

- **Local Processing**: SALSAR processes documents on your machine only
- **No Cloud Upload**: By default, documents stay on your computer
- **Ollama Configuration**: Check Ollama settings for network configuration
- **User Responsibility**: 
  - Secure your installation
  - Protect sensitive documents
  - Comply with data protection laws (GDPR, CCPA, etc.)

---

## Important Disclaimer

### ⚠️ NOT LEGAL ADVICE
This software is an analytical tool for document review only. **It does NOT provide legal advice.** Professional legal consultation is mandatory.

### Limitations
- AI may misinterpret complex legal language
- Extractions must be verified against source documents
- Accuracy depends on document quality and AI model selected
- Users are responsible for all legal decisions

### Liability
The author accepts **NO LIABILITY** for any damages, losses, or consequences from using SALSAR. See LICENSE.txt for complete terms.

---

## Building the Installer

To create a new installer:

1. Install InnoSetup 6.2+ from https://jrsoftware.org/isdl.php
2. Customize SALSAR.iss if needed
3. Run: `build_installer.bat`
4. Installer created in `build\` folder

---

## Support & Contact

- **Issues/Bugs**: Check documentation first
- **Email**: contact@codingfigs.com
- **Website**: http://codingfigs.com
- **License**: MIT - See LICENSE.txt

---

## Contributing

SALSAR is open source. Contributions welcome!

- Report bugs and suggest features
- Submit pull requests with improvements
- Improve documentation and translations
- Share feedback and use cases

---

## Changelog

### Version 1.0.0 (Current)
- Initial public release
- AI-powered extraction
- Statistical analysis
- ML analysis with clustering
- Comprehensive visualizations
- Export reports functionality
- Multi-model support

---

## License

MIT License © 2025 Dr. M. Kamakshaiah

SALSAR is free and open source software. See LICENSE.txt for complete license text and detailed disclaimer.

---

**Last Updated**: April 2026  
**Version**: 1.0.0  
**Status**: Stable Production Release
