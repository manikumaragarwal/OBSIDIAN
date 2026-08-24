
Tags: [[CODING]]

---
# Fine-tuning models
1. Pre-training 
	- Most expensive.
	- Many GPU/TPU hours needed. 
	- Feed model lots of general data
	- LLM demonstrates reasonable level of Language Understanding.
2. **Fine-tuning** (Instruction-tuning / Supervised fine-tuning **SFT**)
	- LLM trained on *Task-specific datasets*

	1. Instruction-tuning / instruction following : 
		- LLM given input as instructions
		- ex - summarize this text, write a poem, etc. 
	2. Dialogue-tuning :
		- fine-tuning on conversational data
	3. Safety tuning : 
		- 