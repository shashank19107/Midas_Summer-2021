# Midas_Summer-2021
Link to the dataset: https://docs.google.com/spreadsheets/d/1pLv0fNE4WHokpJHUIs-FTVnmI9STgog05e658qEON0I/edit#gid=1396401268

Main Jupyter notebook: Task3-main.ipynb
For Just primary category: Midas_Task3.ipynb

Problem Description: You have to clean this data, In the product category tree separate all the categories, figure out the primary category, and then use the model to predict this.
If you want to remove some categories for lack of data, you are also free to do that, mention this with explanation and some visualization.

**Goal: To predict the product category.**

Show how you would **clean and process the data**: The data given to us was a set of product descriptons and we were required to predict the product category for the same. The base of the data given was the description. To make given description onto machine understanable format, we aim to clean the data by removing stop words, the words like a, an, the, by etc. which are often interpreted as noise by our NLP model and also here we saw that most frequent words are price, free, genuine, garantee which have no relation with the category of the product hence would result in increased noise and thereby reducing accuracy of our model. Hence we first identified them and then removed them from the raw data. 

The below image shows the distribution of most frequent words after removing regular stop words, Out of them multiple are not much useful for us hence we decided to remove many of them too.
![alt text](https://github.com/shashank19107/Midas_Summer-2021/blob/main/Assets/Screenshot%20from%202021-04-10%2020-25-42.png?raw=true)

**Visualising the Data:** Given categaries were in form of a tree, we extarcted them and stored them such that the categories that have a lot of products are given preference for training. This have helped us a lot because there were some categories having products less than 5. In training the model we have decided not to force-fit our model for these categories however this have not affected our accuracy very much. 

Now for the results:
These are for the prediction of primary category:
 Accuracy of approx 90%
![alt text](https://github.com/shashank19107/Midas_Summer-2021/blob/main/Assets/Screenshot%20from%202021-04-10%2022-00-41.png?raw=true)
