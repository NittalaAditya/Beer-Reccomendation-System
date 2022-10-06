# Beer-Reccomendation-System

The objective of this project is to create the building blocks of a crowdsourced recommender system. It should accept user inputs in the form of desired attributes of a product and come up with 3 recommendations. 

# TASK-A
* We have scraped about 6k beer review comments from the below website 
https://www.beeradvocate.com/beer/top-rated/

# Task B. 
Assuming that a customer, who will be using this recommender system, has specified 3 attributes in a product. E.g., one website describes multiple attributes of beer like :

•	Aggressive (Boldly assertive aroma and/or taste) 
•	Balanced: Malt and hops in similar proportions; equal representation of malt sweetness and hop bitterness in the flavor — especially at the finish
•	Complex: Multidimensional; many flavors and sensations on the palate
•	Crisp: Highly carbonated; effervescent
•	Fruity: Flavors reminiscent of various fruits or Hoppy: Herbal, earthy, spicy, or citric aromas and flavors of hops or Malty: Grainy, caramel-like; can be sweet or dry
•	Robust: Rich and full-bodied


# Task C. 
We have performed a similarity analysis using cosine similarity (without word embeddings) with the 3 attributes specified by the customer and the reviews. 
The similarity script accepts as input a file with the product attributes, and calculate similarity scores (between 0 and 1) between these attributes and each review. 

# Task D. 
For every review, perform a sentiment analysis (using VADER). 

# Task E. 
Create an evaluation score for each beer that uses both similarity and sentiment scores. E.g., total score  = average of (similarity score + sentiment score) or a multiplicative model.  
Now recommend 3 products to the customer. 

# Task F. 
Comparison of the above results with a scenario where we use word vectors (e.g., the spaCy package with medium sized pretrained word vectors) instead of the plain vanilla bag-of-words cosine similarity?

# Task G. 
How would our recommendations differ if we ignored the similarity and feature sentiment scores and simply chose the 3 highest rated products from your entire dataset? Would these products meet the requirements of the user looking for recommendations? Why or why not? 

# Task H.
Using the top four attributes of beer (from word frequency analysis), we calculate the lifts between these attributes and any 10 beers in your data. We choose one beer, and find the most similar beer (among the remaining 9) using the lift values.
