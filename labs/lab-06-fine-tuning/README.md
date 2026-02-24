# Lab 06 — Fine-tuning

## Objective
Fine-tune a pre-trained model on domain-specific data to specialize it for industrial maintenance vocabulary and patterns.

## Concepts Covered
- Fine-tuning: adapting a pre-trained model to specific domain
- LoRA / QLoRA: parameter-efficient fine-tuning
- Dataset preparation: instruction/response format
- Evaluation: before/after comparison

## Enterprise Scenario
Fine-tune Mistral on maintenance tickets to improve:
- Ticket classification accuracy
- Understanding of domain-specific terminology
- Response quality for maintenance-related queries

## Steps
1. Prepare a training dataset from maintenance tickets (instruction/response pairs)
2. Format data for fine-tuning (Alpaca, ChatML, or ShareGPT format)
3. Configure LoRA/QLoRA hyperparameters
4. Run fine-tuning with Unsloth or PEFT
5. Evaluate on a held-out test set
6. Compare base model vs fine-tuned model on domain tasks

## Deliverable
Domain-specialized model for industrial maintenance.

## Tech Stack
- Unsloth or Hugging Face PEFT
- Mistral / Llama base model
- Python
