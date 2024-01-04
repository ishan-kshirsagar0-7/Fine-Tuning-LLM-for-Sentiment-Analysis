# Fine-Tuning LLM for Sentiment Analysis

## Introduction

This Jupyter notebook demonstrates the fine-tuning process of a sentiment analysis model using advanced techniques such as Low-Rank Adaptation (LoRA) and Parameter-Efficient Fine Tuning (PEFT). Utilizing a pre-trained DistilBERT model, we optimize it for the specific task of discerning positive from negative sentiments in textual data.

## Methodology

We employed LoRA, a technique that introduces a low-rank matrix to existing pre-trained model weights, allowing for efficient adaptation with minimal additional parameters. This approach is part of the broader PEFT strategy, which seeks to fine-tune models without the computational expense of traditional methods. PEFT enables us to refine the model's responses while preserving its original capabilities, ensuring that it remains lightweight and performant.

## Outputs

![error](https://i.ibb.co/84FNzfs/untrained.jpg)

![error](https://i.ibb.co/s6tphx8/trained.jpg)

## Key Steps

**1. Library Installation**: We set up the environment with the necessary libraries for handling datasets, transformers and PEFT.\
**2. Model Initialization**: A DistilBERT model was loaded as a baseline for further fine-tuning.\
**3. Data Preparation**: The IMDB Reviews dataset was chosen for training, providing a matrix of positive and negative sentiments.\
**4. Tokenization**: Text data was tokenized using the LLM tokenizer to convert sentences into tokens.\
**5. LoRA Configuration**: We configured LoRA specific parameters like intrinsic rank & adaptation learning rates for fine-tuning.\
**6. Training**: The model was fine tuned with the set hyperparameters, using the Trainer module for managing the training loop.\
**7. Evaluation**: The model's performance was assessed before and after fine-tuning, showing the impact of LoRA and PEFT.\

## Results

Post-training, the model showed a significant improvement in its ability to correctly classify sentiments. The fine-tuning process with LoRA and PEFT not only enhanced accuracy but also ensured that the model remained efficient and quick to adapt.

## Conclusion

The application of LoRA and PEFT techniques for fine-tuning presents an effective pathway to enhance large language models for specific tasks without the overhead of extensive resource utilization.
