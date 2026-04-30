# Tokenizer Architecture in Cross-Lingual NER Transfer

## Overview
This project investigates how tokenizer design impacts **zero-shot cross-lingual Named Entity Recognition (NER)** for Indic languages, specifically Hindi and Bengali.

The study demonstrates that **tokenizer architecture plays a critical role in transfer performance**, in some cases outweighing the benefits of additional target-language pretraining.

---

## Key Highlights
- Controlled comparison across **6 multilingual transformer models**
- Focus on **WordPiece vs SentencePiece tokenization**
- Evaluation settings:
  - Zero-shot transfer (English → Indic languages)
  - Warm-start fine-tuning
- Introduction of **token fertility** as a metric to analyze tokenization quality

---

## Key Findings
- **WordPiece consistently outperforms SentencePiece** in zero-shot NER for Hindi and Bengali
- Increased target-language pretraining **does not guarantee better performance**
- Tokenization issues have the **largest impact in zero-shot scenarios**
- With minimal fine-tuning, **performance differences across models diminish**

---

## Models Evaluated
- mBERT  
- XLM-R  
- MuRIL  
- IndicBERT  
- IndicBERTv2  
- DistilBERT  

---

## Dataset
- **WikiANN** (Multilingual Named Entity Recognition)

### Languages
- **Source:** English  
- **Target:** Hindi, Bengali  

---

## Installation

Install required dependencies:

```bash
pip install transformers datasets seqeval torch
