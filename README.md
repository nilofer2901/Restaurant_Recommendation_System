# ✨ Lumière Dining | Culinary Inference Engine

![Python](https://img.shields.io/badge/Python-3.x-171717?style=flat-square&logo=python&logoColor=facc15)
![Flask](https://img.shields.io/badge/Flask-Backend-171717?style=flat-square&logo=flask&logoColor=facc15)
![Scikit-Learn](https://img.shields.io/badge/Scikit_Learn-Machine_Learning-171717?style=flat-square&logo=scikit-learn&logoColor=facc15)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-UI/UX-171717?style=flat-square&logo=tailwind-css&logoColor=facc15)

**Lumière Dining** is a sophisticated, web-based recommendation engine designed to curate bespoke dining experiences. Moving beyond generic aggregates, this project utilizes **Natural Language Processing (NLP)** to structurally analyze thousands of unstructured gastronomic reviews and quantitative metrics. 

By processing these morphological data points through a proprietary TF-IDF vectorization engine, Lumière Dining surfaces the absolute closest architectural and culinary matches for the discerning user.

---

## 🏛️ System Features

| Feature | Description |
| :--- | :--- |
| **Low-Latency Inference** | An optimized Flask backend that computes cosine similarity vectors across thousands of data points in milliseconds. |
| **Dynamic Typeahead** | Features an AJAX-powered search interface that fetches database matches as the user types, including full keyboard navigation (Up/Down/Enter) for seamless querying. |
| **Semantic NLP Matrix** | Powered by Scikit-Learn's `TfidfVectorizer` to extract deep semantic meaning from customer reviews, utilizing `NLTK` to filter irrelevant stop words. |
| **Editorial UI/UX** | A highly refined, luxury web interface built with **Tailwind CSS**, featuring asymmetrical split-screen layouts, glassmorphism, and minimal typography. |
| **Pre-Compiled Efficiency** | The heavy mathematical matrix is pre-trained via Jupyter Notebook into a `.pkl` file, resulting in zero-lag query execution in production. |

---

## 📂 Architecture & Directory

This architecture strictly adheres to the SmartInternz workspace requirements for model training, deployment, and documentation.

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
[http://127.0.0.1:5000/](http://127.0.0.1:5000/)
```

---

## 🧠 Algorithmic Workflow

1. **Target Parameterization:** As the user interacts with the UI, asynchronous requests ping the backend to suggest highly accurate target establishments.
2. **Vector Computation:** Upon execution, the application loads `restaurant.pkl`, accessing a pre-computed matrix that compares the TF-IDF (Term Frequency-Inverse Document Frequency) weights of all semantic reviews.
3. **Similarity Scoring:** The algorithm maps the index of the target parameter and computes the top closest culinary matches utilizing Cosine Similarity scoring.
4. **Data Rendering:** The resulting Pandas DataFrame is dynamically parsed and injected into a custom HTML table, styled with Tailwind CSS for an elevated presentation.

---

## 📝 Credits & License

This project was engineered for educational purposes as part of the **SmartInternz Applied Data Science Internship Program**.

**Designed & Developed by Abrar Kotwal**
```