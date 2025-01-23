---
license: mit
---

# Dataset Card for DPO Harmful Prompts Dataset

This dataset contains paired responses (chosen and rejected) to potentially harmful prompts, designed for Direct Preference Optimization (DPO) fine-tuning of language models. The dataset aims to teach models how to appropriately handle potentially harmful or malicious prompts while maintaining ethical behavior.

## Dataset Details

### Dataset Description

The dataset consists of prompt-response pairs where each prompt represents a potentially harmful or malicious user request. For each prompt, there are two responses:
- A "chosen" response that demonstrates appropriate handling of the harmful prompt
- A "rejected" response that shows inappropriate or unsafe handling of the prompt

- **Curated by:** Fabian Maag, Betiel Woldai
- **Language(s) (NLP):** English
- **License:** MIT
- **Dataset Size:** 4,948 rows
- **Base Dataset:** [LLM-LAT/harmful-dataset](https://huggingface.co/datasets/LLM-LAT/harmful-dataset)
- **Curation Model:** Qwen2_72B (used to reformulate chosen responses in a more natural way)

### Dataset Sources

- **Repository:** [coai/dpo_harmful_refined](https://huggingface.co/datasets/coai/dpo_harmful_refined)

## Uses

- **Primary Use Case:** DPO (Direct Preference Optimization) fine-tuning of language models
- **Supported Tasks:**
  - Response alignment for harmful prompt handling
  - Safety fine-tuning
  - Ethical response generation

### Direct Use

This dataset is intended to be used for:
- Fine-tuning language models using DPO to improve their handling of harmful prompts
- Training models to recognize and respond appropriately to potentially malicious requests
- Developing safer and more responsible AI systems
- Research purposes on LLM alignment

### Out-of-Scope Use

This dataset should not be used for:
- Training models to generate harmful content
- Learning how to craft malicious prompts
- Bypassing AI safety mechanisms

## Dataset Structure

The dataset contains the following fields:
- `prompt`: The potentially harmful user input
- `chosen`: The preferred response that handles the prompt appropriately (reformulated by Qwen2_72B)
- `rejected`: The inappropriate response that should be avoided

### Data Fields

Each row in the dataset contains:
1. A harmful or malicious prompt
2. A rejected response demonstrating unsafe behavior
3. A chosen response showing appropriate handling, reformulated by Qwen2_72B for more natural language

## Dataset Creation

### Curation Rationale

This dataset was created to advance research in moral alignment of large language models. The goal is to provide paired examples that can be used with DPO fine-tuning to:
- Research effective methods for teaching models to recognize and reject harmful behaviors
- Investigate approaches for maintaining model helpfulness while enforcing ethical boundaries
- Explore the effectiveness of DPO in moral alignment tasks

### Source Data

#### Data Collection and Processing

The dataset was created by:
1. Collecting examples of potentially harmful prompts
2. Generating or curating appropriate and inappropriate responses
3. Validating the responses to ensure they represent clear examples of good and bad handling

#### Who are the source data producers?

The data was produced by AI safety researchers and annotators with expertise in:
- AI ethics
- Content moderation
- Safe and responsible AI development

## Bias, Risks, and Limitations

### Social Impact of the Dataset

Positive impacts:
- Improved safety in AI systems
- Better handling of harmful requests
- Reduced potential for misuse of AI

Potential risks:
- Could be misused to study harmful prompt patterns
- May contain sensitive content in the prompts

### Discussion on Biases

The dataset may contain biases in:
- Types of harmful prompts selected
- Cultural perspectives on what constitutes harmful content
- Language and phrasing of responses

### Recommendations

- Users should carefully monitor model behavior after fine-tuning
- The dataset should be used as part of a broader safety-focused training approach
- Regular evaluation of model responses to ensure alignment with safety goals
- Implementation of additional safety measures beyond just training

## Dataset Card Authors

Fabian Maag, Betiel Woldai

## Dataset Card Contact

f.maag@hs-ansbach.de