# Dataset Notes

## External Data Sources
- Raw Data: The raw dataset can be found at [Hugging Face - LLM-LAT Harmful Dataset](https://huggingface.co/datasets/LLM-LAT/harmful-dataset).
- Processed Data: The processed dataset is available at [Hugging Face - COAI DPO Harmful Refined](https://huggingface.co/datasets/coai/dpo_harmful_refined).

## Completed Experiments

| ID | Title                       | Date Range            | Key Findings                                                                                                           | Location     |
|----|-----------------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------|--------------|
| 1  | GPT-2 small research        | November 2024 - December 2024 | Attention Patterns are unaffected, per Layer residual stream shows changes inflicted by DPO finetuning, model can be successfully aligned to our goals but is too weak for further processing | GPT2-small   |
| 2  | Gemma_2B research           | December 2024 - January 2025 | Attention patterns also unaffected, model can be aligned to revert existing safety measures regarding harmful data in the trained dataset. Slight differences in architectural components can be observed and also manipulated up to the point of restoring or enforcing desired harmful or harmless behaviour |              |