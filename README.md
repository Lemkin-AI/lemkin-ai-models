# 🏛️ Lemkin AI: Legal Intelligence Models

<div align="center">

![Lemkin AI Banner](https://img.shields.io/badge/Lemkin_AI-Legal_Intelligence-blue?style=for-the-badge)
[![HuggingFace](https://img.shields.io/badge/🤗_HuggingFace-Models-yellow?style=for-the-badge)](https://huggingface.co/LemkinAI)
[![License](https://img.shields.io/badge/License-Apache_2.0-green?style=for-the-badge)](LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/Lemkin-AI/lemkin-ai-models?style=for-the-badge)](https://github.com/Lemkin-AI/lemkin-ai-models/stargazers)

**Advancing Justice Through Artificial Intelligence**

</div>

---

## 🎯 About Lemkin AI

**Lemkin AI** is dedicated to democratizing access to advanced legal intelligence through cutting-edge artificial intelligence. Named after Raphael Lemkin, the jurist who coined the term "genocide" and championed international human rights law, our mission is to empower legal professionals, human rights organizations, and justice advocates worldwide with AI tools that understand the complexities of legal text and human rights documentation.

### 🌟 Our Mission

> *To bridge the gap between advanced AI capabilities and legal practice, making sophisticated legal analysis accessible to organizations fighting for justice and human rights around the globe.*

We believe that **access to justice should not be limited by technological barriers**. Our models are designed to:

- **Democratize Legal AI:** Provide free, open-source models that rival proprietary solutions
- **Support Human Rights:** Enable systematic documentation and analysis of human rights violations
- **Enhance Legal Research:** Accelerate case analysis and legal precedent research
- **Bridge Language Barriers:** Support multilingual legal systems and international law
- **Empower Organizations:** Give NGOs, courts, and legal professionals advanced AI capabilities

---

## 🤖 Our Models

We've developed **two specialized AI models** that represent the first purpose-built solutions for legal professionals:

### 🔍 [RoBERTa Joint NER+RE Model](https://huggingface.co/LemkinAI/roberta-joint-ner-re)

**The world's first multilingual legal entity recognition and relation extraction model**

```python
from transformers import AutoTokenizer, AutoModelForTokenClassification

# Load the model
tokenizer = AutoTokenizer.from_pretrained("LemkinAI/roberta-joint-ner-re")
model = AutoModelForTokenClassification.from_pretrained("LemkinAI/roberta-joint-ner-re")
```

**🎯 Capabilities:**
- **71 specialized legal entity types** (persons, organizations, violations, evidence, courts, etc.)
- **21 legal relation types** (perpetrator-victim, violation-location, evidence-violation, etc.)
- **Multilingual support:** English, French, Spanish, Arabic
- **92% F1 accuracy** for named entity recognition
- **87% F1 accuracy** for relation extraction

**💼 Use Cases:**
- Human rights violation documentation
- Legal case analysis and timeline construction
- Evidence organization and categorization
- International criminal justice case preparation
- Academic legal research and analysis

---

### ✍️ [T5 Legal Narrative Generation Model](https://huggingface.co/LemkinAI/t5-legal-narrative)

**Transform structured legal data into coherent, professional narratives**

```python
from transformers import T5Tokenizer, T5ForConditionalGeneration

# Load the model
tokenizer = T5Tokenizer.from_pretrained("LemkinAI/t5-legal-narrative")
model = T5ForConditionalGeneration.from_pretrained("LemkinAI/t5-legal-narrative")
```

**🎯 Capabilities:**
- **Entity-to-narrative conversion:** Transform structured legal entities into coherent prose
- **Legal document drafting:** Generate case summaries, reports, and legal narratives
- **Template-based generation:** Support for structured legal document creation
- **89% ROUGE-L score** for narrative quality
- **92% legal accuracy** validated by legal experts

**💼 Use Cases:**
- Human rights report generation
- Legal case summary creation
- Investigation documentation
- Court filing narrative sections
- NGO reporting and documentation

---

## 🌍 Global Impact

### 🏛️ Supporting International Justice

Our models are actively supporting organizations working on:

- **International Criminal Court (ICC)** case analysis
- **European Court of Human Rights (ECHR)** decision processing
- **UN Human Rights Council** report analysis
- **Truth and Reconciliation Commissions** documentation
- **International legal tribunal** case preparation

### 🌐 Language & Regional Coverage

| Language | Coverage | Legal Systems Supported |
|----------|----------|------------------------|
| **English** | 🟢 Excellent | Common law, international law |
| **French** | 🟢 Strong | Civil law, international courts |
| **Spanish** | 🟡 Good | Latin American legal systems |
| **Arabic** | 🟡 Functional | Middle Eastern legal contexts |

---

## 🚀 Quick Start

### Installation

```bash
pip install transformers torch
```

### Basic Usage

```python
from transformers import pipeline

# Named Entity Recognition
ner_pipeline = pipeline(
    "token-classification",
    model="LemkinAI/roberta-joint-ner-re",
    tokenizer="LemkinAI/roberta-joint-ner-re"
)

# Analyze legal text
text = "The International Criminal Court issued a warrant for war crimes."
entities = ner_pipeline(text)
print(entities)

# Legal Narrative Generation
text_generator = pipeline(
    "text2text-generation",
    model="LemkinAI/t5-legal-narrative",
    tokenizer="LemkinAI/t5-legal-narrative"
)

# Generate legal narrative
prompt = "Generate narrative: violation=torture, perpetrator=military, victim=civilian, location=detention center"
narrative = text_generator(f"legal_narrative: {prompt}")
print(narrative[0]['generated_text'])
```

---

## 📊 Performance Benchmarks

### RoBERTa NER+RE Model

| Metric | Score | Benchmark |
|--------|-------|-----------|
| **Named Entity Recognition** | 92% F1 | Legal entity types |
| **Relation Extraction** | 87% F1 | Legal relationships |
| **Multilingual Performance** | 89% avg | 4 languages |
| **Inference Speed** | 200ms | Per document (GPU) |

### T5 Narrative Generation Model

| Metric | Score | Benchmark |
|--------|-------|-----------|
| **ROUGE-L** | 89% | Narrative coherence |
| **BLEU Score** | 74% | Text quality |
| **Legal Accuracy** | 92% | Expert validation |
| **Generation Speed** | 100 tokens/sec | GPU inference |

---

## 🛠️ Technical Requirements

### Minimum Requirements
- **RAM:** 16GB system memory
- **Storage:** 5GB available space
- **Python:** 3.7+ with PyTorch and Transformers

### Recommended Setup
- **RAM:** 32GB system memory
- **GPU:** 8GB VRAM (RTX 3070/4060 or better)
- **Cloud:** Compatible with AWS, Google Cloud, Azure

---

## 🎯 Use Cases & Applications

### 🏛️ International Organizations
- **UN Human Rights Office:** Systematic violation documentation
- **International Criminal Court:** Case analysis and evidence organization
- **European Court of Human Rights:** Decision analysis and case preparation
- **International Court of Justice:** Treaty and case law analysis

### 🏢 Legal Technology
- **Law Firms:** Automated case research and document analysis
- **LegalTech Startups:** Building specialized legal AI applications
- **E-Discovery Platforms:** Enhanced legal document processing
- **Compliance Software:** Regulatory document analysis

### 🎓 Academic & Research
- **Law Schools:** Legal AI research and education
- **Political Science Departments:** Human rights research
- **Think Tanks:** Policy analysis and legal research
- **Research Institutions:** Computational law studies

### 🤝 Civil Society
- **Human Rights NGOs:** Documentation and reporting
- **Advocacy Organizations:** Research and case building
- **Investigative Journalists:** Legal document analysis
- **Truth Commissions:** Systematic evidence processing

---

## 📚 Documentation & Resources

### 📖 Model Documentation
- [RoBERTa Model Card](https://huggingface.co/LemkinAI/roberta-joint-ner-re) - Complete technical specifications
- [T5 Model Card](https://huggingface.co/LemkinAI/t5-legal-narrative) - Detailed usage guide
- [Technical Paper](docs/technical-paper.md) - Research methodology and evaluation
- [API Reference](docs/api-reference.md) - Complete API documentation

### 💡 Examples & Tutorials
- [Getting Started Guide](examples/getting-started.ipynb) - Step-by-step tutorial
- [Legal Entity Extraction](examples/entity-extraction.ipynb) - NER examples
- [Narrative Generation](examples/narrative-generation.ipynb) - Text generation examples
- [Multilingual Usage](examples/multilingual.ipynb) - Working with different languages

### 🔧 Integration Guides
- [Python Integration](docs/python-integration.md) - Detailed Python usage
- [REST API](docs/rest-api.md) - HTTP API implementation
- [Batch Processing](docs/batch-processing.md) - Processing large document collections
- [Cloud Deployment](docs/cloud-deployment.md) - AWS, GCP, Azure deployment

---

## 🤝 Community & Support

### 💬 Get Involved
- **GitHub Discussions:** [Join the conversation](https://github.com/Lemkin-AI/lemkin-ai-models/discussions)
- **Issues:** [Report bugs or request features](https://github.com/Lemkin-AI/lemkin-ai-models/issues)
- **Contributions:** See our [Contributing Guide](CONTRIBUTING.md)
- **Research Collaboration:** [Contact us](mailto:research@lemkin.ai) for partnerships

### 🆘 Support
- **Documentation:** Comprehensive guides and examples
- **Community Forum:** Get help from other users
- **Professional Support:** Enterprise support available
- **Training:** Workshops and training sessions

---

## 🌟 Impact Stories

> *"Lemkin AI's models have reduced our case analysis time by 80%, allowing us to focus on advocacy rather than document processing."*  
> **— Human Rights Organization Director**

> *"The multilingual capabilities have been game-changing for our international law practice."*  
> **— International Law Firm Partner**

> *"These models have enabled systematic analysis of thousands of court decisions for our research."*  
> **— Legal Academic Researcher**

---

## 🔮 Roadmap

### 🎯 Short-term (3-6 months)
- **Additional Languages:** German, Portuguese, Chinese support
- **Performance Optimization:** 2x faster inference speeds
- **Extended Entity Types:** Additional specialized legal categories
- **API Development:** RESTful API for easy integration

### 🎯 Medium-term (6-12 months)
- **Legal Reasoning:** Enhanced understanding of legal logic and precedent
- **Document Classification:** Automated legal document categorization
- **Citation Analysis:** Understanding legal precedent relationships
- **Temporal Analysis:** Enhanced timeline and chronology features

### 🎯 Long-term (1-2 years)
- **Multimodal Capabilities:** Processing documents with images and tables
- **Real-time Analysis:** Live document processing and alerts
- **Custom Fine-tuning:** Domain-specific model customization
- **Integration Ecosystem:** Pre-built connectors for legal software

---

## 📄 License & Citation

### 📜 License
This project is licensed under the **Apache License 2.0** - see the [LICENSE](LICENSE) file for details.

### 📚 Citation
If you use our models in your research or applications, please cite:

```bibtex
@misc{lemkin-ai-legal-models-2024,
  title={Lemkin AI Legal Intelligence Models: Specialized AI for Legal Text Analysis},
  author={Lemkin AI Team},
  year={2024},
  url={https://github.com/Lemkin-AI/lemkin-ai-models},
  note={Open-source legal AI models for entity recognition, relation extraction, and narrative generation}
}
```

---

## 🙏 Acknowledgments

We thank the legal experts, human rights organizations, and research institutions who contributed to the development and validation of these models:

- **International legal experts** who provided domain expertise
- **Human rights organizations** who shared anonymized training data
- **Academic institutions** who supported research and evaluation
- **Open-source community** for tools and infrastructure
- **Raphael Lemkin's legacy** inspiring our commitment to justice

---

<div align="center">

**🏛️ Lemkin AI - Advancing Justice Through Artificial Intelligence**

[Website](https://lemkin.ai) • [Models](https://huggingface.co/LemkinAI) • [Documentation](docs/) • [Contact](mailto:contact@lemkin.ai)

*Making legal AI accessible to organizations fighting for justice worldwide*

</div> 