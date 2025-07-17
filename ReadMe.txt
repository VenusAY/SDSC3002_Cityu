This README file provides instructions on how to run the code for generating predictions using the Singular Value Decomposition (SVD) model in a recommender system context.

Below is the Python packages used in my code:
- numpy
- pandas
- scikit-surprise

You can install them using pip by running the command:
```
pip install numpy pandas scikit-surprise
```

## Files Used
- training.txt
- testing.txt

## Running the Code
1. Place the code provided(SDSC 3002 Assignment3-Final.ipynb) in a Python file
2. Place the `training.txt` and `testing.txt` files in the same directory as your Python script.
3. Press restart and rull all


## Output
After running the script, it will:
- Perform 10-fold cross-validation on the training data to estimate the Root Mean Square Error (RMSE) of the model.
- Train the SVD model on the full training dataset.
- Predict the ratings for the testing dataset and save them in a new file `prediction.txt`, which will contain the predicted ratings in the format `user,item,rating`.

## Notes
- The SVD model is a matrix factorization technique often used for dimensionality reduction and is suitable for building recommender systems.
- The ratings are predicted by the model by learning latent factors that represent user and item interactions.
-The run time is pretty long, please wait patiently.

If you encounter any issues or have questions, please refer to the documentation of the `scikit-surprise` library or contact the script author.
