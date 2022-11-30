
## **Overview**

- Sentiment analysis of hotel reviews and restaurant reviews 
- Good, bad, and neutral reviews 
- Use BERT model to accurately determine sentiment of a review despite having some masked words and labels. 


## **Model and Dataset**

BERT 
  - Encoder only transformer
  - Masked language model - meaning it takes a piece of text with some removed tokens and then tries to correctly predict the masked tokens using the surrounding tokens in the piece of text. 
  - BERT also can also be used to perform sentiment classification.  
 
 ![image](https://user-images.githubusercontent.com/64801054/204862222-2cf6ebc2-43e7-424c-9174-35db4079fa9b.png)


Hotel Reviews data:
- Trip Advisor Hotel Review data set with 20,000 reviews
- positive reviews assigned value 2 if the rating is 4 or 5
- neutral reviews assigned value 1 if the rating is 3 
- negative reviews assigned value 0 if the rating is 1 or 2

New York Restaurants: 
- Trip Advisor Retaurant Reviews with over 500,000 reviews 
- contained restaurant name, review ID, date, full reviews and previews of reviews, restaurant URL, and author ID's
- positive reviews assigned value 2 if the rating is 4 or 5
- neutral reviews assigned value 1 if the rating is 3 
- negative reviews assigned value 0 if the rating is 1 or 2


## **Code Demos** 

Hotel Reviews example:

https://colab.research.google.com/drive/1L-hJF6PIoRGZuSltBQ2t6CBHagBSvu7X#scrollTo=hquaP0Q676Nz

https://github.com/anncam/Transformers/blob/main/transformers_hotel_reviews_bert.ipynb

New York Restaurants example:

https://colab.research.google.com/drive/1aRa-lPRxBpFY6Sc2glfkBzyx10gSPtoZ#scrollTo=-tUXrOlZC4AA

https://github.com/anncam/Transformers/blob/main/project/transformers_retaurant_reviews.ipynb

## **Critical Analysis** 
In the case of the restaurant reviews, I think this BERT model did a decent job of unmasking the reviews. I'm not sure if this actually would affect the predictive power ability of the model or not, but one thing that I noticed was that a lot of the most frequently used words appeared in both good and bad reviews. For example, the word "good" could be used in really any context and depending on what words are masked, the model might not be able to predict the correct sentiment or the correct words. Obviously there is a big differnce between "our experience at this restaurant was really good" and "overall we had a good time despite poor service". 

My next steps would be to improve the model accuracy by running the model on a larger subset of the restaurant reviews data or even the entire data set. 

## **Resources** 

BERT Model - Huggingface  
https://huggingface.co/docs/transformers/model_doc/bert

More about BERT models:
https://www.techtarget.com/searchenterpriseai/definition/BERT-language-model

"Formal Algorithms for Transformers" paper
https://arxiv.org/pdf/2207.09238.pdf

A more in depth sentiment analysis of the hotel reviews data:
https://www.kaggle.com/code/emirkocak/in-depth-series-sentiment-analysis-w-transformers/notebook

### **Sources**
Original project code: https://www.kaggle.com/code/charlessamuel/trip-advisor-hotel-reviews-bert/notebook

Data sources: 
https://www.kaggle.com/code/charlessamuel/trip-advisor-hotel-reviews-bert/notebook
https://www.kaggle.com/datasets/inigolopezrioboo/a-tripadvisor-dataset-for-nlp-tasks?select=New_York_reviews.csv

