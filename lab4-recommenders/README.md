# Lab 4 - Recommender systems

## Resources

* rec_latent.ipynb contains the code shown in the lecture for a recommender system based on latent features
* item_features.csv, user_features.csv and user_ratings.csv contain the data used in the lecture
* jester-data-1.csv contains the data needed for this lab (the Jokes dataset)
* helper_function.ipynb contains a function that will help you with the exercises below, together with an example of use
* movies_latent_factors.xslx is a spreadsheet with two sheets:
	* The Items sheet contains the feature values for 100 items and 15 latent factors
	* The Users sheet contains the feature values for 20 users and those 15 latent factors.
	* Have a look here to find out how to load this file: [https://www.statology.org/pandas-read-excel/](https://www.statology.org/pandas-read-excel/)


## Lab Exercises

- [ ] Create a folder called lab4
- [ ] Create a notebook called *my_recommender.ipynb*

In the Jupyter notebook you created
- [ ] Load the data from ``jester-data-1.csv'',
    * The data is from [http://eigentaste.berkeley.edu/dataset/](http://eigentaste.berkeley.edu/dataset/) and it contains the ratings of 100 jokes from 11,190 users
	* Check the dataset description to figure out which value you should replace with NaNs (the cells for which we don't have a rating). This is the **test set**. 
	* To replace values when you load, you can find help here: [https://stackoverflow.com/questions/29247712/how-to-replace-a-value-in-pandas-with-nan](https://stackoverflow.com/questions/29247712/how-to-replace-a-value-in-pandas-with-nan)
	* There's a column you need to remove because it doesn't contain ratings. Check the description of the dataset and figure out which one. Then drop it.
- [ ] Make sure you've done the steps above properly and your dataset has been loaded properly or your answers to the quiz won't be correct!!
- [ ] Use pandas to find the best- and the worst-rated jokes (i.e., highest average rating and lowest average rating)
- [ ] **Modify** and use the helper function provided in the helper_function notebook (or create your own) to label 10% of the dataset cells that are not NaNs as 99. This is your **validation set**. Keep the the actual values of the cells so you can use them later (as done in the example of the helper_function notebook). 
- [ ] Use latent factor modeling (with 2 latent factors) to infer the hidden ratings of the users (they are labeled as "99" in the dataset) on the training set. You will have to modify at least one line in the provided sgd() function for this (and probably 2, depending on your variable names).
	* Iterations in sgd will take a long time to run: you can (and should) use low numbers. Try something like 10.
	* You can interrupt at any point the execution of this function, because the values are updated in each iteration, so if you interrupt execution you can use the latent_user_preferences and latent_item_features.
- [ ] Calculate the performance (e.g., MSE) of the algorithm on the **validation dataset**
- [ ] OPTIONAL: Repeat the two points above changing hyper-parameters (i.e., learning rate, number of iterations of SGD, number of latent factors, etc.) as needed to get good results (you can create multiple validation sets if you want, and run a bootstrap!)
- [ ] Make predictions for the **test dataset**.
- [ ] Open the quiz on moodle. After you've done it, make sure you save all the code you used in Github!







