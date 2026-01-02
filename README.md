# Fine-tuning-Large-Language-Models-LLMs-
Sentiment Analysis with LoRA.
Project Summary

This project demonstrates fine-tuning a pre-trained language model for sentiment analysis using the Hugging Face ecosystem and LoRA (Low-Rank Adaptation) for efficient parameter tuning. The base model used is DistilBERT (distilbert-base-uncased), a lightweight version of BERT, which we adapted for binary sentiment classification on a dataset containing 1000 text entries labeled as positive or negative. The dataset is loaded from Hugging Face’s repository (shawhin/imdb-truncated) and is preprocessed using a tokenizer to convert text into input IDs and attention masks suitable for the model. Padding is handled with a data collator to allow batch training.

Instead of full fine-tuning, we applied LoRA, which updates only a small set of low-rank parameters in the model, reducing computational cost and memory requirements while still improving performance. The model is trained using the Hugging Face Trainer API, with a batch size of 4 and 10 epochs. Evaluation is done using the accuracy metric on a train/test split, and we can generate predictions for sample text to verify model behavior.

Notably, the training setup avoids extra services like Weights & Biases and does not include automatic evaluation strategy prompts, keeping the workflow simple and easy to reproduce. This project highlights how modern techniques like LoRA can make large language model fine-tuning accessible, efficient, and practical even for small datasets. It serves as a concise example of combining transformers, datasets, PEFT, and PyTorch in a real-world NLP task, suitable for educational purposes or as a starting point for more advanced sentiment analysis projects.
