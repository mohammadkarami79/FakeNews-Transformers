# FakeNews-Transformers
This project focuses on detecting fake news using Transformer-based models such as BERT and CT-BERT. The models are trained using different approaches, including Fine-Tuning and Feature-Based methods, to assess their effectiveness in identifying fake news related to COVID-19.


Introduction
In this project, we investigate the effectiveness of Transformer-based models such as BERT and CT-BERT in detecting fake news, particularly related to COVID-19. The project explores different training strategies, including Fine-Tuning and Feature-Based methods, to determine the most effective approach for this task.

Models and Approaches
Fine-Tuning Approaches
BERT + Dense Layer: A fine-tuned BERT model with a dense output layer.
BERT + BiGRU: BERT with a BiGRU layer, followed by a dense output layer.
CT-BERT + BiGRU: Similar to the above, but using CT-BERT, pre-trained on COVID-19-related data.
Feature-Based Approaches
BERT + Dense Layer: The BERT layers are frozen, and only the dense layer is trained.
BERT + BiGRU: BERT with frozen layers, using a BiGRU and dense layer for training.
CT-BERT + BiGRU: CT-BERT with frozen layers, combined with a BiGRU and dense layer.
Dataset
The dataset consists of posts, comments, and news articles related to COVID-19, collected from platforms like Twitter and YouTube. These are labeled as real or fake to be used for model training and evaluation.

Preprocessing
Tokenization: Texts are tokenized using BERT's tokenizer.
Emoji Handling: Emojis are converted to text using the emoji library.
Truncation: Texts are truncated to a maximum length of 128 tokens.
Results
Fine-Tuning Results
BERT + BiGRU

Test Accuracy: 96.64%
F1-Score (Fake): 0.96
F1-Score (Real): 0.97
CT-BERT + BiGRU

Test Accuracy: 98.22%
F1-Score (Fake): 0.98
F1-Score (Real): 0.98
Feature-Based Results
BERT + BiGRU

Test Accuracy: 90.98%
F1-Score (Fake): 0.91
F1-Score (Real): 0.91
CT-BERT + BiGRU

Test Accuracy: 90.84%
F1-Score (Fake): 0.90
F1-Score (Real): 0.92
Analysis
CT-BERT generally outperforms BERT, especially in the fine-tuning approach.
The addition of BiGRU layers enhances the models' ability to capture long-term dependencies in text.
Fine-Tuning approaches tend to yield better results compared to Feature-Based methods, as all model layers are updated, leveraging the full potential of the pre-trained models.
How to Run
Clone the repository:
bash
Copy code
git clone <repository_url>
cd <repository_directory>
Install the required packages:
bash
Copy code
pip install -r requirements.txt
Run the training scripts: Navigate to the scripts/ directory and run the desired model training scripts.
View the results: After training, you can view the results and generated plots in the results/ directory.
Conclusion
This project demonstrates the effectiveness of Transformer-based models, particularly CT-BERT, in detecting fake news. The results indicate that fine-tuning models on domain-specific data (such as COVID-19) significantly enhances their performance. Additionally, the use of BiGRU layers helps capture contextual information, improving the accuracy of predictions. These findings highlight the importance of using appropriate architectures and training strategies for achieving optimal results in natural language processing tasks like fake news detection.

This README provides a comprehensive overview of the project, highlighting the key aspects and results. You can now use this README in your repository to give visitors and collaborators a clear understanding of the project and its outcomes.







