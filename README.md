# DSC180A-FinalProject
[Multiclass-Classification](https://github.com/Cyl200215/DSC180-LiarHackthon/blob/main/Liar%20Classification.ipynb), code to preprocess datasets and train multiclass classcifer
In this notebook, it contains all classification models that I did base on my factuality factors.

To Run GenAI.ipynb, please download below nltk:
```python
nltk.download('stopwords')
nltk.download('wordnet')
nltk.download('averaged_perceptron_tagger')
```

# DSC180-LiarHackthon

## Files
1. [Liar Classification.ipynb](https://github.com/Cyl200215/DSC180-LiarHackthon/blob/main/Liar%20Classification.ipynb), code to preprocess datasets and train multiclass classcifer.
In this notebook, it contains the Liar Hackthon 
2. [politifact_plus_data.csv](https://github.com/Cyl200215/DSC180-LiarHackthon/blob/main/politifact_plus_data.csv), data newly scraped from Politifact
3. [train2.tsv, test2.tsv, val2.tsv](https://github.com/Cyl200215/DSC180-LiarHackthon/blob/main/test2.tsv), data originally from Liar-Plus dataset. 

## Dataset 
Dataset **politifact_plus_data** is around 890 newly scrapped data from **Politifact.com**. The dataset contains label, statement, and justification from the TRUTH-O-METER on Politifact. Justification is scraped from the summary of the fact linked article. <br>

Dataset **test2.tsv, train2.tsv, val2.tsv** comes from the [Liar-Plus dataset](https://github.com/Tariq60/LIAR-PLUS). <br>

Total of 11129 data were used to train the 6 label classification model. <br>

## Model 
Reference to [Triple Branch BERT Siamese Network](https://github.com/manideep2510/siamese-BERT-fake-news-detection-LIAR). <br>

Instead of using three branches of BERT model, I connected only two branch of BERT model for faster process. The two branch uses column **statement** and **justification** to tokenize and predict the labels.