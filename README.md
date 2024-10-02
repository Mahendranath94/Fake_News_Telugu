# **Fake News Detection in Telugu using Transformer Models**
### **Overview**
This project focuses on detecting fake news in the Telugu language using transformer-based models. With the increasing spread of disinformation, especially in low-resource languages like Telugu, this study aims to contribute to the detection of fake and misleading news through fine-tuning pre-trained multilingual models. The models used in this project include mBERT, XLM-RoBERTa, IndicBERT, and MuRIL.

### **Objective**
The primary objective of this project is to detect fake and misleading news in Telugu by fine-tuning advanced transformer models on a custom dataset. This is an attempt to address the issue of data scarcity in low-resource languages, especially for Dravidian languages like Telugu.

### **Dataset**
The dataset was compiled from various Telugu news sources:

* **Factual (Not-Fake) news:** Scraped from [telugu.hindustantimes.com](https://telugu.hindustantimes.com/)
* **Fake and Misleading news**: Collected from [factly.in](https://factly.in/)
  
The dataset includes multiple domains such as business, sports, and cinema.
A total of 4548 sentences were collected and categorized into three classes: Fake (1906), Not-Fake (1906), and Misleading (736).
### **Preprocessing**
* Scraped data was cleaned by removing irrelevant symbols and extra information.
* The dataset was balanced by reducing the number of Not-Fake sentences to 1906.
* The final dataset contains essential attributes such as claim headlines, factuality descriptions, authors, and publication dates.
### **Models Used**
Four transformer models were used for fine-tuning:

* **mBERT**: Multilingual BERT trained on over 100 languages.
* **XLM-RoBERTa**: Enhanced BERT model for cross-lingual tasks.
* **IndicBERT**: ALBERT model optimized for 12 Indian languages.
* **MuRIL**: Multilingual model pre-trained on 17 Indian languages, specifically designed to handle code-switching, dialects, and transliterations.
### **Methodology**
**Fine-tuning:** Pre-trained models were fine-tuned using the HuggingFace transformers library.
* **Dataset split:** Training (80%), Validation (10%), Testing (10%).
* **Training parameters**: Batch size of 8, learning rate of 5e-5, 3-5 epochs, and weight decay of 0.01.
  
**Model architecture:** Tokenizers and sequence classification layers were set up for each model using the HuggingFace library.
Evaluation metrics: The models were evaluated using Accuracy and F1-Score.
### **Results**
After fine-tuning, the performance of the models was evaluated across various metrics:

* MuRIL achieved the best overall performance with an accuracy of 88.79% and an F1-Score of 88.57% after 3 epochs.
* mBERT also performed well with an accuracy of 88.79% and an F1-Score of 87.90% after 3 epochs.
* IndicBERT showed significant improvement after 5 epochs, reaching 86.81% accuracy and an F1-Score of 86.71%.
* XLM-RoBERTa performed slightly lower, with a maximum accuracy of 86.37% after 5 epochs.

### **Conclusion**
This project successfully demonstrates the application of transformer-based models for detecting fake news in the Telugu language. MuRIL showed the best performance overall, making it a promising tool for tackling misinformation in low-resource languages. The project also highlights the potential of fine-tuning pre-trained multilingual models for specific language tasks, even when data is limited.

### 🔗 **Paper Link**
Publication Paper : [Fake News Detection in Telugu Language using Transformers Models](https://ieeexplore.ieee.org/abstract/document/10580521)
