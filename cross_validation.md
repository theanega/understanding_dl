# Cross validation

My mother has this hypothesis: Spanish people who don't cook tortilla de patata with onion is because they either don't like onions or they don't like cooking. So, let's gather data to try to confirm the hypothesis. The dataset contains information of the 47 million people who live in Spain. For every citizen, we have the following variables: name, tortilla_onion (1 if they like it wiht onion, 0 if they don't put onion - this is the target variable, the ground truth), cooking_like (1 if the person likes to cook, 0 if they don't), onion_like ( 1 if the person likes onion, 0 if they don't). We build a model to classify Spanish people into the two groups (tortilla with onion and tortilla without onion) based on the two  variables (likes to cook and likes onions). Cool, we have built the model. 

Now you ask yourself: does this model work on other datasets? Can it classify italians based on their tortilla with onion preference? In order words: does our model generalize? We test the model on Italians. Then we ask ourselves: does it realy generalize? Italians are not really representative of the whole world's population. Maybe the Italians are too similar to Spanish. Okay you repeat with French. Then with Portuguese, Greeks, English and Russians. What about the other nationalities? Is there a way we can test if our models generalizes (in general...) across all nationalities without having to test it on every single one of them?

Yes. 

---

One way to answer this question is to split your dataset into training and test. You train the model with your training sdta and test it on the test data. 

Let's imagine we have an infinite dataset. We can easily divide the dataset into train and test data becuase we have so much that the test subset willbe repesentative enough of the whole dataset to obtain an accurate performance estimate.