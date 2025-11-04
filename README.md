# 🛳️ Titanic Survival Prediction - End-to-End Advanced Data Analysis & Prediction

![titanic](assets/titanic.png)

This project dives deep into the **Titanic Dataset** to uncover hidden insights about the passengers — who survived, why, and how different social, demographic, and ticket-based factors influenced survival chances.

The project walks through **data cleaning, feature engineering, exploratory data analysis (EDA)**, and finally **machine learning modeling** to predict survival probabilities.

---

## 📁 Dataset
The dataset used is the **Titanic-Dataset.csv**, which contains passenger details such as:
- Demographics (Age, Sex, Name, etc.)
- Travel information (Ticket, Fare, Cabin, Embarked)
- Survival status (0 = Did not survive, 1 = Survived)

---

## ⚙️ Steps Performed

### 1. **Data Cleaning & Preprocessing**
- Dropped unnecessary column `PassengerId`.
- Filled missing values in:
  - `Embarked` with **mode**.
  - `Age` with **median grouped by Title** of passengers extracted from `Name` feature.
  - `Deck` predicted using a **Random Forest Classifier**.
- Extracted meaningful information from:
  - `Name` → Extracted **Title (Mr, Mrs, Miss, etc.)**.
  - `Cabin` → Extracted **Deck**.
  - `Ticket` → Created **Ticket Group Size** to identify social context.
- Created new feature **Family_Size = 1 + Parch + SibSp**.
- Engineered **Social_Context (Grouping)** as:
  - Alone  
  - Small Family  
  - Large Family  
  - Group with Non-Family  
- Categorized passengers under 16 years as **child** in the `Sex` column.

---

### 2. **Feature Engineering Highlights**
| Feature | Description |
|----------|--------------|
| `Title` | Extracted from Name, grouped into 6 categories (Mr, Mrs, Miss, Master, Military, Other) |
| `Deck` | Extracted from Cabin and predicted missing values |
| `Family_Size` | Count of family members including passenger |
| `Grouping` | Identifies whether a person is Alone, in Family, or with Non-Family group |
| `Sex` | Categorized into male, female, child |
| `Fare` | Rounded to 2 decimal points |

---

## 📊 Exploratory Data Analysis (EDA)

Below are visual insights obtained from the data exploration:

### ⚫ Survival Distribution
Shows overall survival ratio.
  
![Survival Pie](assets/survival_pie.png)

---

### ⚫ Survival by Gender
Children and women had a higher survival rate compared to men.

![survival_gender](assets/survival_gender.jpg)

---

### ⚫ Deck-wise Survival Rate
Certain decks had higher chances of survival (upper decks).

![Decks](assets/Decks.png)

![survival_deck](assets/survival_deck.png)

---

### ⚫ Age vs Survival
Younger passengers and middle-aged adults survived more than elderly.

![agesurvival](assets/agesurvival.png)

---

### ⚫ Passenger Class vs Survival
Higher-class passengers had better survival odds.

![classsurvival](assets/classsurvival.png)

---

### ⚫ Grouping (Social Context) vs Survival
Small families had the highest survival rate, while large families struggled.

![groupingsurvival](assets/groupingsurvival.png)

---

### ⚫ Title vs Survival
Masters (young boys) and married women (Mrs) survived most.

![titlesurvival](assets/titlesurvival.png)

---

### ⚫ Fare vs Survival
Higher fare correlated with higher survival chances — money did matter!

![faresurvival1](assets/faresurvival1.png)
![faresurvival2](assets/faresurvival2.png)

---

## 🧠 Machine Learning Model

Three models were trained and compared:  

![comparison](assets/comparison.png)

Random Forestt Classifier provided **82.68%** accuracy with good balance of precision and recall.  


> Random Forest Classifier was chosen as the **final model** due to the best overall performance.


---

## 🧩 Tech Stack

- **Python** 🐍  
- **Pandas, NumPy** → Data Wrangling  
- **Seaborn, Matplotlib** → Visualization  
- **Scikit-learn** → Preprocessing & Modeling  
- **XGBoost** → Advanced Classification  

---

## 📈 Key Insights

- 💡 **Women and Children first** policy truly reflected in survival statistics.  
- 💡 **High fare and high class** passengers had better survival rates.  
- 💡 **Small families** survived more often than large ones.  
- 💡 **Deck and Title** had a significant correlation with survival.

---

## 🧾 Conclusion

After extensive **feature engineering, visualization, and modeling**, this project achieved a strong predictive performance with **Random Forest (Accuracy ≈ 82.68%)**.

This workflow demonstrates how combining **domain understanding**, **data cleaning**, and **machine learning** can bring clarity to historical datasets like the Titanic.

---

## 🧑‍💻 Author
**Md Mehedi Hassan**  
Data Scientist | Researcher
📧 mehedi3128.mhd@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/md-mehedi-hassan-65818b243) | [GitHub](https://github.com/Mehedi2154901019)

---

> ⭐ *If you like this project, don’t forget to give it a star!*
