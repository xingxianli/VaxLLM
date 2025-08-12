# VaxLLM

VaxLLM (Vaccine Large Language Model) is a fine-tuned Large Language Model (LLM) designed to **classify** and **annotate** PubMed articles related to *Brucella* vaccines. It automatically extracts structured vaccine-related metadata from abstracts and full-texts, enabling downstream integration into databases such as **VIOLIN**. The VaxLLM annotation involves extracting the itemized information of vaccine antigen, vaccine formulation, host species used as animal model, and experiment performed to investigate the vaccine.

## Key Features

- **Abstract Classification**  
  Determines whether a given PubMed abstract contains sufficient vaccine formulation details to be considered vaccine-related.

- **Structured Annotation**  
  Extracts key fields:
  - Vaccine Introduction
  - Vaccine Type
  - Vaccine Antigen
  - Vaccine Formulation
  - Host Species Used as Laboratory Animal Model
  - Experiment Used to Investigate the Vaccine
  - Vaccine Efficacy
  - Immume Response
  - Article Results

- **Full-text Extraction Support**  
  Enhances abstract-level annotations with additional details from full-text articles.
  https://github.com/Hegroup-Bioinformatics/PaperToData

- **PubTator Integration**  
  Adds gene, disease, and other biomedical annotations for enriched metadata.

- **Export to Excel**  
  Clean, structured outputs ready for manual review or database ingestion.

## Workflow

End-to-End Pipeline:

Abstract Retrieval → PubMed keyword search (PMIDs, metadata, abstracts)

Abstract Classification → VaxLLM determines if article is vaccine-related

Annotation → Extracts vaccine details into structured fields

Full-text Retrieval (optional) → PMC full-text fetching

Full-text Extraction → Enrich annotations with additional details

PubTator Integration → Adds biomedical entities (genes, diseases, etc.)

Data Harmonization → Standardize fields via Data Harmonizer

Export to database → Convert Excel sheet to database format

## Model Details
- **Developed by:** Xingxian Li at He Group, University of Michigan
- **License:** MIT
- **Finetuned from model:** Meta-Llama-3-8B-Instruct
- **Task Supported**: Text Generation
- **Specialized Domain**: Brucella vaccine-related content
- **Model Type**: Fine-tuned Language Model


## Sample Codes

Sample code to use VaxLLM: [use_VaxLLM](https://github.com/xingxianli/VaxLLM/blob/main/use_VaxLLM.ipynb)

Sample data provided: [brucella_articles.txt](https://github.com/xingxianli/VaxLLM/blob/main/brucella_articles.txt)

Sample code to clean VaxLLM results: [clean_result.ipynb](https://github.com/xingxianli/VaxLLM/blob/main/clean_result.ipynb)

Sample output: [VaxLLM_results.xlsx](https://github.com/xingxianli/VaxLLM/blob/main/VaxLLM_results.xlsx)
