# The decision to split data into train/valid/test or just train/test

The decision to split data into **train/valid/test** or just **train/test** depends on the goal of the experiment, model complexity, and the availability of data:

## Train/Valid/Test Split:
- Use this split when you need to tune hyperparameters or select the best model.
- The **training set** is used to train the model, the **validation set** is used to evaluate the model during training to tune hyperparameters and avoid overfitting, and the **test set** is used for final model evaluation.
- This approach is often necessary when you're trying to ensure that the model generalizes well on unseen data and are actively trying different models or hyperparameters.

**Example:**
- Training set: 70-80% of data
- Validation set: 10-15% of data
- Test set: 10-15% of data

## Train/Test Split:
- Use this split when you're not tuning any hyperparameters or when you have a predefined model and only want to evaluate its performance.
- The **training set** is used for training, and the **test set** is used to assess final model performance.
- This is often employed when you have simpler models or a well-defined set of hyperparameters and you want to focus on general performance without needing validation during training.

**Example:**
- Training set: 80-90% of data
- Test set: 10-20% of data

## Key Considerations:
- If your model or task is complex, or if you plan to fine-tune model parameters, a **validation set** is essential.
- If data is limited, you may prefer to use **cross-validation** instead of a dedicated validation set, particularly in the case of a **train/test** split.
