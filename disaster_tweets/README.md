# Kaggle - Disaster tweets

This project is about try different text classfiers using various methods and compare the results:
- TF-IDF + meta data
- BERT (only texts)
- BERT + meta data

# 1.TF-IDF classfier
There are 3 main parts in this modelling:
- Preprocessing: clean text, impute missing values, text noramlization, stemming,...
- Feature engineering: create new variables from tweets meta data to give additional information to the model.  Transform text into weights matrix with TF-IDF
- Machine learning: train a classifier with a simple algorithm (Random Forest)

# 2. Fine-tuned BERT classifier
The main idea is to use the almighty BERT. Transfer learning is the one of the most powerful methods to devlelop a classifier with a moderate amount of data. Use of hugging face's packaged pre-trainge BERT uncased model (12 layers) to fine-tune with tweets data to obtain a classifier.

# 3. BERT + meta data classifier
Sometimes, it is useful to use meta data to improve performance because, it gives additional information. 



Notes: some parts were ispired by some works listed in above.
Thank you for these wonderful works that they've shared:
...