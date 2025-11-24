#    AI-Powered Guess the Number Game

This is a classic "Guess the Number" game implemented in Python, with a unique twist: it includes a **Linear Regression model** trained on specific data. Although the AI model's prediction is **not currently used** to influence the game logic or user experience, its presence demonstrates a basic integration of machine learning into a simple application.

---

##  Features

* **Classic Gameplay:** Guess a randomly generated number between 1 and 100.
* **Attempt Counter:** Tracks how many tries it takes to win.
* **Closeness Feedback:** Provides hints like "Too Low!", "Too High!", and "Very Close!" (if the guess is within 5 of the target).
* **Machine Learning Integration:** Trains a `LinearRegression` model using `numpy` and `scikit-learn`.

---

##  How the AI Model is Trained

The `train_model()` function creates and trains a simple linear regression model.

* **Input Data (`X`):** Numbers from 1 to 100 (`np.array(range(1, 101))`).
* **Target Data (`y`):** The absolute difference between the number and 50 (`abs(50 - i)`).
    * This means the model is trained to predict a **high value** for numbers far from 50 (like 1 or 100) and a **low value** for numbers close to 50.
* **Prediction (`prediction`):** The model calculates a prediction based on the user's guess, but this output is currently **not used** in the main game logic to provide hints, making the core game purely based on chance and basic comparison.



---

##  Setup and Installation

### Prerequisites

You need **Python 3.x** installed on your system.

### Dependencies

This script requires the following Python libraries:

* `numpy`
* `scikit-learn` (`sklearn`)

You can install the dependencies using `pip`:

```bash
pip install numpy scikit-learn
