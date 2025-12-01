

Data analytics means **examining raw data to find meaningful conclusions**, patterns, or decisions.

### **Why do we use it?**

To answer questions like:

- _Why did sales drop?_
    
- _Which customers are likely to leave?_
    
- _Which ad campaign gives the best ROI?_
    

### **Primary Goals**

|Goal|Meaning|
|---|---|
|Describe|What happened? (Past)|
|Diagnose|Why did it happen?|
|Predict|What will happen?|
|Prescribe|What should be done?|

### **Types / Roles**

|Role|Purpose|Example|
|---|---|---|
|Descriptive|Summarize past|Monthly sales report|
|Diagnostic|Find cause|Why sales dropped?|
|Predictive|Forecast future|Stock prediction using ML|
|Prescriptive|Suggest actions|Best pricing strategy|

---

## **2️⃣ Data Science vs Data Analytics**

|Feature|Data Science|Data Analytics|
|---|---|---|
|Focus|Future predictions & automation|Understanding past & present|
|Tools|ML, AI, Deep Learning|Statistics, Excel, SQL, BI|
|Output|Models & algorithms|Reports, dashboards|
|Example|Build churn prediction model|Find why churn increased|

---

## **3️⃣ Identification of Variables**

A **variable** is anything that can change or vary.

|Type|Meaning|Example|
|---|---|---|
|Qualitative (Categorical)|Describes categories|Gender, Eye color|
|Quantitative (Numeric)|Number-based|Age, Salary|

Further classification:

**Quantitative →**

- **Discrete**: counted values (e.g., number of children)
    
- **Continuous**: measured values (e.g., height, weight)
    

---

## **4️⃣ Measurement Scales**

Measurement scale tells **how data is measured**.

|Scale|Nature|Example|Math Allowed|
|---|---|---|---|
|Nominal|Labels only|Gender|Count only|
|Ordinal|Rank order|Grades (A>B>C)|Order, but no difference meaning|
|Interval|Numeric, no true zero|Temperature °C|Add/Subtract|
|Ratio|Numeric, real zero|Salary, weight|All operations|

**Interval vs Ratio** difference:

- Temperature **0°C ≠ no temperature** (interval)
    
- Weight **0 kg = no weight** (ratio)
    

---

## **5️⃣ Summary Measures**

These are **statistical values** that summarize large datasets.

They include:

- Central tendency (center)
    
- Dispersion (spread)
    
- Shape (distribution)
    

---

## **6️⃣ Measures of Central Tendency**

### 📌 (a) Mean (Average)

Mean=∑Xn\text{Mean} = \frac{\sum X}{n}Mean=n∑X​


Pros: Easy + uses all data  
Cons: **Affected by extreme values (outliers)**

Example:  
Data = {5, 10, 12, 100}  
Mean = 127/4 = **31.75** (not representative)

---

### 📌 (b) Median (Middle value)

Order the data → pick middle value.  
Better when **outliers exist**

Example:  
{5, 10, 12, 100} → median = (10+12)/2 = **11**

---

### 📌 (c) Mode (Most frequent value)

Useful for **categorical data**.

Example:  
{red, red, blue, green} → mode = **red**

---

### 📌 (d) Geometric Mean

Used for **growth rate or returns**.

G=(X1×X2×...×Xn)1/nG = (X_1 \times X_2 \times ... \times X_n)^{1/n}G=(X1​×X2​×...×Xn​)1/n

Example:  
Returns = +10%, –10%  
GM < AM → Realistic growth

---

### 📌 (e) Percentiles

Divides data into **100 parts**  
90th percentile = 90% values below it

---

### 📌 (f) Quartiles

Split data into **4 equal parts**

- Q1 = 25%
    
- Q2 = 50% (median)
    
- Q3 = 75%
    

---

## **7️⃣ Measures of Dispersion (Spread of Data)**

### 📌 (a) Range

Range=Max−Min\text{Range} = \text{Max} - \text{Min}Range=Max−Min

### 📌 (b) Variance

Measures average **spread from mean**

S2=∑(X−Xˉ)2n−1S^2 = \frac{\sum (X - \bar{X})^2}{n-1}S2=n−1∑(X−Xˉ)2​

### 📌 (c) Standard Deviation (σ)

Square root of variance  
**Most important measure of spread**

S=S2S = \sqrt{S^2}S=S2​

Interpretation:  
Higher SD = more variation

### 📌 (d) MAD

Average absolute deviation  
Useful when data has **outliers**

### 📌 (e) Coefficient of Variation (CV)

CV=SXˉ×100CV = \frac{S}{\bar{X}} \times 100CV=XˉS​×100

Used to compare **different units** (e.g., heights vs weights)

---

## **8️⃣ Covariance**

Tells direction of relationship between two variables:

>0:move together (positive)>0 : \text{move together (positive)}>0:move together (positive) <0:move opposite (negative)<0 : \text{move opposite (negative)}<0:move opposite (negative)

---

## **9️⃣ Correlation**

Measures **strength + direction** of relation  
Value always between **–1 and +1**

|Value|Meaning|
|---|---|
|+1|Perfect positive|
|–1|Perfect negative|
|0|No relation|

---

## **🔟 Shape Measures**

### (a) Skewness

|Type|Meaning|
|---|---|
|Positive|Tail on right|
|Negative|Tail on left|
|Zero|Symmetric|

### (b) Kurtosis

|Type|Meaning|
|---|---|
|Leptokurtic|Tall & thin|
|Platykurtic|Flat|
|Mesokurtic|Normal|

---

## **1️⃣1️⃣ Normal Distribution**

Bell-curve distribution  
Mean = Median = Mode  
Symmetric

---

## **1️⃣2️⃣ Empirical Rule**

Used only for **normal distribution**

|Range|% of data|
|---|---|
|µ ± 1σ|68%|
|µ ± 2σ|95%|
|µ ± 3σ|99.7%|

---

## **1️⃣3️⃣ EDA & Box Plot**

Box plot shows

- Median
    
- Quartiles
    
- Outliers  
    Detected using **1.5×IQR rule**
    

---

# 🎉 Completed — Full Teaching Done

Let me know if you want:

☑ numerical examples  
☑ real-life dataset practice  
☑ Python / Excel formulas  
☑ quizzes / revision notes  
☑ flashcards


