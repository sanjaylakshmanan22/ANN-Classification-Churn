```markdown
# Customer Churn Prediction App

An end-to-end Machine Learning web application built to predict bank customer churn using an Artificial Neural Network (ANN)[cite: 1, 2]. The application is built with **TensorFlow/Keras** for deep learning and deployed interactively via **Streamlit**[cite: 2, 4].

---

## Project Overview

Customer churn is a critical metric for businesses, especially in banking. This project uses historical customer data to predict whether a customer is likely to leave the bank (churn) or stay based on various demographic and financial attributes[cite: 1, 2]. 

* **Model Type:** Artificial Neural Network (ANN) with Sequential API[cite: 1]
* **Frontend/UI:** Streamlit Web App[cite: 2]
* **Frameworks & Libraries:** TensorFlow, Scikit-Learn, Pandas, NumPy[cite: 4]

---

## Dataset Features

The model is trained on the `Churn_Modelling.csv` dataset[cite: 1], containing features such as:
* **CreditScore:** Customer's credit score[cite: 1]
* **Geography:** Country of residence (France, Germany, Spain)[cite: 1, 2]
* **Gender:** Male or Female[cite: 1, 2]
* **Age & Tenure:** Age of the customer and number of years with the bank[cite: 1, 2]
* **Balance & Estimated Salary:** Account balance and estimated annual salary[cite: 1, 2]
* **NumOfProducts:** Number of bank products the customer uses[cite: 1, 2]
* **HasCrCard & IsActiveMember:** Binary indicators for credit card ownership and activity status[cite: 1, 2]
* **Exited:** Target variable (1 if the customer churned, 0 otherwise)[cite: 1]

---

## Project Structure

```text
├── Churn_Modelling.csv           # Original dataset
├── app.py                        # Streamlit web application script[cite: 2]
├── model.h5                      # Trained ANN model[cite: 2]
├── scaler.pkl                    # StandardScaler object for feature scaling[cite: 2]
├── label_encoder_gender.pkl      # Label encoder for Gender feature[cite: 2]
├── onehot_encoder_geo.pkl        # OneHot encoder for Geography feature[cite: 2]
└── requirements.txt              # Project dependencies[cite: 4]

```

---

## Installation & Setup

Follow these steps to run the project locally on your machine.

### 1. Clone the Repository

```bash
git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
cd your-repo-name

```

### 2. Create a Virtual Environment (Optional but Recommended)

```bash
python -m venv venv
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

```

### 3. Install Dependencies

Install all necessary packages listed in `requirements.txt`:

```bash
pip install -r requirements.txt

```

---

## Running the Application

To launch the Streamlit web interface locally, run:

```bash
streamlit run app.py

```

Open your browser and navigate to the local URL provided in the terminal (usually `http://localhost:8501`).

---

## Model Training & Architecture

The deep learning model was built using **TensorFlow/Keras** with the following components:

* **Input Layer:** Handles preprocessed and scaled numerical and encoded categorical features.


* **Hidden Layers:**
* Dense layer with 64 neurons and `ReLU` activation.


* Dense layer with 32 neurons and `ReLU` activation.




* **Output Layer:** Dense layer with 1 neuron and `Sigmoid` activation for binary classification (churn probability).


* **Callbacks:** Utilized **EarlyStopping** to prevent overfitting and **TensorBoard** for training visualization.



---

## Deployment

This project can be easily deployed on cloud platforms like **Streamlit Community Cloud**, **Render**, or **Hugging Face Spaces**:

1. Push all project files (`app.py`, `model.h5`, `*.pkl`, `requirements.txt`) to your GitHub repository.


2. Link your GitHub repository to [Streamlit Cloud](https://streamlit.io/cloud).
3. Set the main file path to `app.py`.
4. Deploy and access your live application via a public URL!

```

```
