# Samuel-Association-Mini

## 📌 Project: Association Rule Mining with Simulated Data

### 🎯 Objective
To simulate basic shopping transactions and uncover patterns using association rule mining with the Apriori algorithm.

---

## ✅ Step 1: Simulated Transaction Data

- Created 10 fake transactions using a pool of 8 items:
  - `Bread`, `Milk`, `Eggs`, `Butter`, `Cheese`, `Apples`, `Bananas`, `Cereal`
- Each transaction contained 2–5 randomly selected items.

**The simulated transactions:**  
Transaction 1: ['Milk', 'Bread', 'Cheese']  
Transaction 2: ['Eggs', 'Butter', 'Cereal', 'Bananas']  
Transaction 3: ['Milk', 'Eggs']  
Transaction 4: ['Cheese', 'Bananas', 'Apples', 'Milk']  
Transaction 5: ['Bread', 'Eggs', 'Butter']  
Transaction 6: ['Milk', 'Cereal', 'Apples']  
Transaction 7: ['Bananas', 'Cereal']  
Transaction 8: ['Eggs', 'Cheese', 'Bread']  
Transaction 9: ['Apples', 'Bananas']  
Transaction 10: ['Butter', 'Milk', 'Bread']  

---

## ✅ Step 2: Apriori Analysis

- Used `TransactionEncoder` from `mlxtend` to one-hot encode the transactions.
- Applied the Apriori algorithm with:
  - `min_support = 0.3` (30%)

**Result:** Identified frequent itemsets that appear in at least 30% of all transactions.

---

## ✅ Step 3: Association Rule Generation

- Generated association rules using:
  - `metric = 'confidence'`
  - `min_threshold = 0.7` (70%)
- Extracted rules from the frequent itemsets.

### 🔝 Top 2 Rules:
| Antecedent | Consequent | Confidence |
|------------|------------|------------|
| Bananas    | Bread      | 0.80       |
| Eggs       | Bananas    | 0.75       |

---

## 🧠 Rule Interpretation

**Rule Chosen:**  
> If a customer buys **Bananas**, they are **80% likely** to also buy **Bread**.

**Real-Life Meaning:**  
> "Shoppers who pick up **Bananas** usually add **Bread** to their cart as well. This means that in 8 out of 10 cases, Bananas and Bread are purchased together. Retailers can use this insight to place these items close to each other or bundle them in promotions."

---

## 💾 Files Included

- `association_mining.ipynb` — Jupyter Notebook with full code and results.
- `README.md` — This file with summary and explanation.

---

## 🚀 How to Run

1. Clone this repo:
   ```bash
   git clone https://github.com/yourusername/samuel-association-mini.git
2. Install required libraries:
```python
pip install pandas mlxtend
```
3. Run the notebook:
Open association_mining.ipynb and run all cells.
