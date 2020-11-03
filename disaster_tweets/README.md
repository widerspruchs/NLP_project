# Kaggle - Disaster tweets

This project aims to develop different text classfiers using various methods and compare their results. There are 3 models that were created:
- TF-IDF + meta data + Random Forest
- BERT (only texts) sequence classifier
- BERT + meta data sequence classifier 

# 1.TF-IDF classfier
There are 3 main parts in this modelling:
- Preprocessing: clean text, impute missing values, text noramlization, stemming,...
- Feature engineering: create new variables from tweets meta data to give additional information to the model. Furthermore, transform text into weights matrix with TF-IDF to attribute scores at tokens.
- Machine learning: train a classifier with a simple algorithm (Random Forest).
Notebook: disaster_tweets_basic_classifier.ipynb

# 2. Fine-tuned BERT classifier
The main idea is to use the almighty BERT. Transfer learning is the one of the most powerful methods to devlelop a classifier with a moderate amount of data. Use of hugging face's packaged pre-trained BERT uncased model (12 layers) to fine-tune with the tweets data to obtain a classifier. 
Notebook: disaster_tweets_bert

# 3. BERT + meta data classifier
To improve BERT srequence classifier fine-tuned, the idea is to use some meta data (same meta data created with basic methods) to hope to give additional information while training and predicting. To accelerate the training process, a colab notebook was used. 

# Data analysis
Data exploration and data analysis were done to get insights about the relation between variables and target values.  Some visualization and simple statistics were done to let me to create meta data columns to be used in some methods. This was very first analysis, the study should be iterated to be have deep insights over data and extract useful information to be used in modelling.

# Results:
|       Method        |  f1 score on test set|
|---------------------|----------------------|
|  TF-IDF + meta data |  0.74685             |
|  BERT               |  0.81428             |   
|  BET + meta data    |  0.81244             |  

The f1 score is directly calculated at each submission on Kaggle.


# Notes
## Improvements
These works were realized in a very limited time. There are multiple possibilities to imporove the performance of these model such as:
- Preprocessing: enrich cleaning processes (use of regex to detect slangs)
- Feature engineering: select and keep only useful meta data instead of using all created meta data.
- Machine learning: hyperparameter tuning to set adapated parameters to gain in performance. Increase the number of epochs for BERT to train deeply the models.

## Other information
Notes: some parts were ispired by some works listed in above.
Thank you for these wonderful works that they've shared:

...