# Fine Tune SLM, Gemma Model

## Gemma Small Language Model Fine-Tuning:

- **Introduction:**
Fine-tuning large language models (LLMs) such as Gemma using specialized frameworks is 
crucial for enhancing model performance in specific domains or tasks. This report explores
the process and outcomes of fine-tuning the Gemma LLM using the TRL (Text Representation Learning) module.

## Methodology

- **Setup and Environment:**
Implemented fine-tuning using the SFTTrainer from the TRL module.
Utilized the Gemma tokenizer (GemmaTokenizer) and model configuration (LoraConfig) for 
compatibility and optimization.

- **Data Preparation:**
Prepared the dataset suitable for the fine-tuning task, ensuring it aligns with the 
objective of enhancing performance in a specific domain or task.

1. No. of data = 20

2. Data Details: `Dataset({
    	features: ['Ticket ID', 'Subject', 'Description', 'Status', 'Priority', 'Created', 'Assigned To'],
    	num_rows: 20
	})`

- **Fine-Tuning Process:**
Initialized the Gemma model (AutoModelForCausalLM) with pre-trained weights. Configured training 
parameters such as batch size, learning rate, and number of epochs based on experimental validation.

- **Training and Evaluation:**
Conducted fine-tuning iterations using the TRL SFTTrainer, optimizing Gemma's performance on the target dataset.
Evaluated the fine-tuned model's performance metrics including perplexity, accuracy, and any domain-specific metrics.

- **Traning Details:**

1. No. of iteration: 50
2. Used Supervised Fine Tuning (SFT) trainer
3. LoRA configuration with dimension = 8
4. Converted to 4-bit data type configuration
5. Model: `google/gemma-2b`, Google's Gemma model with 2B parameter
