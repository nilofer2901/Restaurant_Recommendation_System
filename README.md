```
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

```

Food_Discovery/
│
├── Dataset/
│   └── zomato.csv.zip
│
├── Document/
│   └── FOOD_DISCOVERY_REPORT.docx
│
├── Model/
│   └── Food_Discovery_Model.ipynb
│
├── Flask/
│   ├── static/
│   ├── templates/
│   │   ├── index.html
│   │   ├── web.html
│   │   └── result.html
│   │
│   ├── app1.py
│   ├── zomato.csv
│   ├── restaurant.pkl
│   └── restaurant_cleaned.csv
│
├── requirements.txt
└── README.md

````

---

## ⚙️ Setup Instructions

### 1. Install Dependencies
```bash
pip install -r requirements.txt
````

---

### 2. Train Model (Notebook)

* Extract `zomato.csv.zip`
* Place dataset inside `Flask/` folder
* Open `Food_Discovery_Model.ipynb`
* Run all cells
* Ensure `restaurant.pkl` is generated

---

### 3. Run Flask App

```bash
python app1.py
```

---

### 4. Open in Browser

```
http://127.0.0.1:5000/
```

---

## 🧠 How It Works

1. User enters a restaurant name or preference
2. System converts text into numerical vectors using TF-IDF
3. Cosine similarity is calculated between all restaurants
4. Top matching restaurants are selected
5. Results are displayed in a structured UI

---

## 🎯 Objective

The goal of **Food Discovery** is to simplify restaurant selection by providing intelligent, data-driven recommendations instead of random suggestions.

---

## 👩‍💻 Developer

**Nilofar Shaikh**
