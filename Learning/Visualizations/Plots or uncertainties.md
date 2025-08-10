


![[Biostatsquid - EASY violin plots and boxplots - simple explanation with examples _8NGYsNeBS_Y - 983x553 - 2m31s_.png|457x257]]

![[Biostatsquid - EASY violin plots and boxplots - simple explanation with examples _8NGYsNeBS_Y - 981x552 - 2m38s_.png|450x253]]


interquartile range is less sensitive to outliers than the range
only considers the variability of the 50% of the middle data
![[Biostatsquid - EASY violin plots and boxplots - simple explanation with examples _8NGYsNeBS_Y - 981x552 - 3m28s_.png|536x302]]

# Boxplot Basics
**Quartiles**:
- **Q1 (Lower Quartile)**: 25% of data falls below this point.
- **Q3 (Upper Quartile)**: 75% of data falls below this point.
- **IQR (Interquartile Range)** = Q3 − Q1 → represents the spread of the middle 50% of the data.
- **IQR is more robust than range** as it is less sensitive to outliers.
- **Whiskers** extend to the smallest and largest values **within 1.5 × IQR**.

- **Outliers** beyond the whiskers are plotted as **dots**.

The mean
The dispersion


📊 **Interpreting a Boxplot:**
- **Central Tendency**: The **median line** shows where the middle of the data lies.
    
- **Spread**/ dispersion:
    - **IQR**: length of the box.
    - **Range**: from minimum to maximum or whisker endpoints.
![[Biostatsquid - EASY violin plots and boxplots - simple explanation with examples _8NGYsNeBS_Y - 981x552 - 4m24s_.png|361x203]]

- **Skewness**:
    - Symmetric: Median in the middle; whiskers even.
    - Right-skewed (positive): Median near bottom; longer upper whisker.
    - Left-skewed (negative): Median near top; longer lower whisker.
![[Biostatsquid - EASY violin plots and boxplots - simple explanation with examples _8NGYsNeBS_Y - 981x552 - 4m59s_.png|319x150]]

- **Outliers**:
    - Points beyond **1.5 × IQR** from Q1 or Q3.


## ⚖️ **Comparing Groups with Boxplots:**

- Compare **median** lines across groups.
![[Biostatsquid - EASY violin plots and boxplots - simple explanation with examples _8NGYsNeBS_Y - 981x552 - 6m32s_.png|341x177]]
- Compare **IQRs** (box lengths) to assess spread.
![[Biostatsquid - EASY violin plots and boxplots - simple explanation with examples _8NGYsNeBS_Y - 981x552 - 6m59s_.png|300x169]]

![[Biostatsquid - EASY violin plots and boxplots - simple explanation with examples _8NGYsNeBS_Y - 981x552 - 7m09s_.png|297x167]]
- Compare **ranges** using whisker lengths.
- Look for **outliers** in each group.

- Assess **symmetry/skewness** visually.
![[Biostatsquid - EASY violin plots and boxplots - simple explanation with examples _8NGYsNeBS_Y - 981x552 - 8m00s_.png|304x171]]
## **Violin Plots = Boxplot + Density Plot**

### 🎯 **Purpose:**

- Combines the summary power of boxplots with the **shape** of data distribution via a **rotated density plot**.
    
### 📌 **What You See in a Violin Plot:**

- **Wider areas** = more data (higher density).
- **Narrower areas** = fewer data points (lower density).
- Can show **bimodal**, **skewed**, or **normal** distributions clearly.
- Still includes median and IQR markers.


![[Biostatsquid - EASY violin plots and boxplots - simple explanation with examples _8NGYsNeBS_Y - 981x552 - 8m46s_.png|394x222]]



----

# Density distribution plots 

![[Biostatsquid - How to interpret density plots - simple explanation with examples! _CbqoxkkJyzY - 981x552 - 0m34s_.png]]


To visualize the distribution of continuous variables



# 🔍 Six Key Points to Interpret a Density Plot

Here are six key points to consider when interpreting a density plot, helping you to extract meaningful insights from your data distributions:

## 1. Shape

The overall form of the density curve provides insights into the distribution's characteristics:

* **Symmetric:** Indicates an even spread of data around a central point.
* **Skewed:**
    * **Right/Positive Skew:** The tail extends more towards the right, suggesting a presence of higher extreme values.
    * **Left/Negative Skew:** The tail extends more towards the left, indicating a presence of lower extreme values.
* **Modality:** Refers to the number of prominent peaks in the distribution:
    * **Unimodal:** Possesses a single, distinct peak.
    * **Bimodal:** Exhibits two distinct peaks.
    * **Multimodal:** Shows multiple peaks, often suggesting the presence of distinct subgroups or clusters within the data.
![[Biostatsquid - How to interpret density plots - simple explanation with examples! _CbqoxkkJyzY - 981x552 - 2m44s_.png|355x200]]

![[Biostatsquid - How to interpret density plots - simple explanation with examples! _CbqoxkkJyzY - 981x552 - 2m53s_.png|361x203]]


    🧠 **Example:**
    TP53 expression in a cell population might show:
    * A peak for cells with deleted TP53.
    * A peak for normal expression.
    * A peak for overexpression (e.g., due to DNA duplication).

## 2. Central Tendency

The central tendency of the data is represented by the peak(s) of the curve. The location of the peak directly indicates the **mode**, which is the most frequently occurring value in the dataset.

![[Biostatsquid - How to interpret density plots - simple explanation with examples! _CbqoxkkJyzY - 981x552 - 3m47s_.png|398x224]]

![[Biostatsquid - How to interpret density plots - simple explanation with examples! _CbqoxkkJyzY - 981x552 - 3m45s_.png|397x223]]

## 3. Variability

The spread or dispersion of the data is measured by the **width of the curve**:

* **Wide curve:** Suggests high variability, meaning the data points are more spread out.
* **Narrow curve:** Indicates low variability, meaning the data points are clustered closely together.
![[Biostatsquid - How to interpret density plots - simple explanation with examples! _CbqoxkkJyzY - 981x552 - 4m10s_.png|460x259]]
## 4. Tails

The "tails" of a density plot are the regions extending outwards from the main body of the distribution. These represent the **extreme (outlier) values** in your dataset:

* **Long tails** imply a higher probability of encountering outliers.
* Identifying long tails can be crucial for **quality control**, such as filtering errors in sequencing data.
![[Biostatsquid - How to interpret density plots - simple explanation with examples! _CbqoxkkJyzY - 981x552 - 4m42s_.png|378x213]]

## 5. Area Under the Curve (AUC)

The area under the curve (AUC) within a specific range represents the **probability of values falling within that range**.

* The **total area under the entire curve is always 1 (or 100%)**, as it encompasses all possible probabilities.
* For example:
    * Area under curve < 41 = ~70% probability.
    * Area between 40 and 41 = ~19% probability.
* The curve itself never goes below the x-axis, as probability cannot be negative.
![[Biostatsquid - How to interpret density plots - simple explanation with examples! _CbqoxkkJyzY - 981x552 - 5m28s_.png|388x218]]

![[Biostatsquid - How to interpret density plots - simple explanation with examples! _CbqoxkkJyzY - 981x552 - 5m44s_.png|390x219]]

## 6. Comparison of Groups

Density plots are highly effective for comparing distributions across different groups or conditions:

* **Overlay multiple density plots** to visually compare distributions across:
    * **Conditions** (e.g., normal vs. cancer tissue).
    * **Groups** (e.g., treatment vs. control).
* When comparing, focus on differences in:
    * **Shape**
    * **Central tendency**
    * **Variability**


![[Biostatsquid - How to interpret density plots - simple explanation with examples! _CbqoxkkJyzY - 981x552 - 6m30s_.png|469x264]]


----


<iframe width="560" height="315" src="https://www.youtube.com/embed/0tLF83IxwdY?si=4cAx3yEJdI090A_1" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


<iframe width="560" height="315" src="https://www.youtube.com/embed/aNFDEYERCb0?si=yL6Pn-A7WwswofKd" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>








