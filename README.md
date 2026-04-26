# 🍽️ Food Discovery | Smart Restaurant Recommendation System

![Python](https://img.shields.io/badge/Python-3.x-171717?style=flat-square&logo=python&logoColor=facc15)
![Flask](https://img.shields.io/badge/Flask-Backend-171717?style=flat-square&logo=flask&logoColor=facc15)
![Scikit-Learn](https://img.shields.io/badge/Scikit_Learn-ML-171717?style=flat-square&logo=scikit-learn&logoColor=facc15)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-UI/UX-171717?style=flat-square&logo=tailwind-css&logoColor=facc15)

**Food Discovery** is an intelligent web-based restaurant recommendation system designed to help users discover the best dining options based on preferences and reviews.

The system uses **Natural Language Processing (NLP)** and **Machine Learning techniques** to analyze restaurant data and user reviews, delivering personalized and relevant recommendations in real time.

---

## 🏛️ System Features

| Feature | Description |
| :--- | :--- |
| **Fast Recommendation Engine** | Flask backend generates restaurant suggestions instantly using pre-trained models. |
| **Smart Search Interface** | Dynamic search system that suggests restaurants as users type. |
| **NLP-Based Analysis** | Uses TF-IDF vectorization to understand and analyze user reviews. |
| **Clean UI Design** | Modern responsive interface built using Tailwind CSS. |
| **Optimized Model Loading** | Pre-trained `.pkl` model ensures fast predictions. |

---

## 📂 Project Structure

```text
Restaurant_Recommendation_System/
│
├── Dataset/
│   └── zomato.csv.zip                         # Compressed raw analytical dataset
│
├── Document/
│   └── RESTAURANT_RECOMMENDATION_SYSTEM.docx  # Final Project Report
│
├── Model/
│   └── Restaurant_Recommendation_System.ipynb # Backup of analysis notebook
│
├── Flask/
│   ├── static/                                # Compiled CSS/JS assets
│   ├── templates/
│   │   ├── index.html                         # Editorial landing sequence
│   │   ├── web.html                           # Auto-complete query interface
│   │   └── result.html                        # Minimalist data output dashboard
│   │
│   ├── app1.py                                # Main Flask Application Server
│   ├── Restaurant_Recommendation_System.ipynb # Primary Training Script (EDA & Model)
│   ├── zomato.csv                             # Extracted raw dataset
│   ├── restaurant.pkl                         # Trained Model Matrix (Auto-generated)
│   └── restaurant1.csv                        # Cleaned Dataset (Auto-generated)
│
├── requirements.txt               
└── README.md  
```

---

## ⚙️ Initialization & Setup

### 1. Environment Preparation
Ensure Python 3.x is installed on your system. Install all required dependencies using the provided requirements file:
```bash
pip install -r requirements.txt
```

### 2. Matrix Training (Jupyter Notebook)
> **Note:** Before booting the web server, you must clean the raw dataset and generate the trained machine learning matrix.

1. Extract `zomato.csv.zip` and ensure `zomato.csv` is located inside the `Flask/` directory.
2. Open `Restaurant_Recommendation_System.ipynb` using Jupyter or VS Code.
3. Execute all cells sequentially to perform Exploratory Data Analysis (EDA) and train the NLP model.
4. Verify that `restaurant.pkl` and `restaurant1.csv` have successfully generated in your `Flask/` folder.

### 3. Server Deployment
Start the local Flask server by executing the main application script:
```bash
python app1.py
```

### 4. Access the Engine
Open your preferred web browser and navigate to the local server address:
```text
http://127.0.0.1:5000/
```

---

## 🧠 Algorithmic Workflow

1. **Target Parameterization:** As the user interacts with the UI, asynchronous requests ping the backend to suggest highly accurate target establishments.
2. **Vector Computation:** Upon execution, the application loads `restaurant.pkl`, accessing a pre-computed matrix that compares the TF-IDF (Term Frequency-Inverse Document Frequency) weights of all semantic reviews.
3. **Similarity Scoring:** The algorithm maps the index of the target parameter and computes the top closest culinary matches utilizing Cosine Similarity scoring.
4. **Data Rendering:** The resulting Pandas DataFrame is dynamically parsed and injected into a custom HTML table, styled with Tailwind CSS for an elevated presentation.

---

## 📝 Credits

**Designed & Developed by Nilofar Shaikh**
