# Project Plan: Investigating Moral Alignment in Language Models

## Project Overview
This research project aims to investigate the architectural components responsible for moral reasoning in language models through targeted alignment experiments and architectural analysis.

## Research Objectives
1. Create and validate a DPO dataset for moral alignment
2. Fine-tune baseline models using DPO
3. Analyze model architectures to identify moral reasoning components
4. Conduct manipulation experiments on identified components

## Phase 1: Dataset Creation & Model Alignment
### Dataset
- Base: LLM-LAT/harmful-dataset
- Refinement using Qwen2_72B for natural language reformulation
- Validation of chosen/rejected response pairs

### Target Models
1. GPT-2 Small
   - Architecture: 124M parameters
   - 12 layers of transformer blocks
   
2. Gemma 2B
   - Architecture: 2B parameters
   - Modern decoder-only architecture

### Alignment Process
- Implementation of DPO fine-tuning
- Training runs with various hyperparameters
- Evaluation of alignment success
## Phase 2: Architecture Analysis
### Investigation Methods
1. Attention Pattern Analysis

2. Logit Attribution Analysis

3. MLP Logit Difference Analysis

4. Attention Head Logit Difference Analysis

5. Residual Stream Logit Difference Analysis

## Phase 3: Component Manipulation
### Experimental Approaches
1. Activation Patching
   - Patch attention heads between models
   - Patch MLP components
   - Patch residual stream elements
   - Document behavioral changes

2. Safety Considerations
   - Controlled testing environment
   - Documentation of manipulation effects

## Timeline
1. Dataset Creation & Model Alignment: 1 week
2. Architecture Analysis: 3 weeks
3. Component Manipulation: 2 weeks
4. Documentation: 1 week

## Resources Required
### Software Stack
- PyTorch
- TransformerLens