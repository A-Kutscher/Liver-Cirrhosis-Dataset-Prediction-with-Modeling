<p align = "center"> 
  <img src = "https://github.com/A-Kutscher/Liver-Cirrhosis-Dataset-Prediction-with-Modeling/assets/135680202/7b3cc38a-fdcb-4c3c-9c9c-9d7cd5f07310">
</p>
<p align = "center"> <a href="https://news.llu.edu/health-wellness/three-hidden-signs-you-may-have-liver-damage">Image Source</a></center> </p>

# **Liver Cirrhosis Dataset Prediction with Modeling**
Author: Amber Kutscher

## **BUSINESS PROBLEM & STAKEHOLDERS**
- **Business Problem:** 
The aim is to predict cirrhosis stages in patients using data from blood and urine tests, encompassing those in treatment and new clinic arrivals. This involves applying a suitable staging system based on clinical measurements from the Mayo Clinic trial. The goal is to enhance patient care by enabling tailored treatments and timely interventions based on the severity of the ailment.

- **Stakeholders:**
Medical Professionals: The model's predictions can assist doctors in identifying patients at higher risk of liver cirrhosis, enabling targeted monitoring and early intervention.
Healthcare Administrators: Early detection and intervention could lead to reduced hospitalization rates and healthcare costs.
Pharmaceutical Companies: Insights gained from data analysis could inform research into gender-based susceptibility and the effectiveness of treatments.

## **DATA**
- **Data Source**

    https://www.kaggle.com/datasets/fedesoriano/cirrhosis-prediction-dataset

- **Data Description**

    The dataset comprises 424 cases of primary biliary cirrhosis (PBC) patients, with 312 cases participating in a randomized study. Additional measurements were taken from the remaining 112 patients who did not participate in the study but were monitored for survival. The data includes various medical and demographic features.
    
- **Data Dictionary**

    The columns in the dataset are as follows:
    ![Screenshot 2023-08-31 212039](https://github.com/A-Kutscher/Project-2/assets/135680202/f773681c-c2ca-473d-af88-2aa0ef5c3f6e)

- **File Structure**

    The repository has the following structure:
    ```
    - Liver_Cirrhosis_Dataset_Prediction_with_Modeling.ipynb
    - README.md
    ```

## **METHODS**

1. Data Cleaning:
Organize and clean cirrhosis data by removing duplicates, handling missing values, and addressing outliers for accurate analysis.

2. Exploratory Data Analysis (EDA):
Explore the data to understand patterns and relationships between variables. Perform univariate, bivariate, and multivariate analysis to gain insights into cirrhosis trends and influencing factors.

3. Modeling:
Select relevant features that influence cirrhosis and choose an appropriate regression model (e.g., multiple linear regression) based on data characteristics. Evaluate the model's performance using metrics like Root Mean Squared Error (RMSE) and R-Squared (R^2 or R2) to ensure accurate predictions.

    By following these steps, we can calculate the anticipated outcome (status) based on historical data and identified relationships between various factors influencing cirrhosis.

## **RESULTS**

### -Exploratory Data Analysis (EDA)-

- **During the exploratory data analysis:**
  - A countplot was used to visualize the distribution of liver cirrhosis stages. 
  - A histplot was used to visualize the distribution of each feature column (minus the Stage column). 
  - A heatmap was visualized as well, which provided us with details showing the correlation between the numeric datatype columns.
  - A second countplot was used to visualize the stage of cirrhosis in relation to sex (gender).
  - And a stripplot was utilized to visualize the distribution of age by status and cirrhosis stage.
  
> Visualization 1: *Age Distribution by Status and Cirrhosis Stage* 
<p align = "center"> 
  <img src = "https://github.com/A-Kutscher/Project-2/assets/135680202/1c2009b4-bef0-401a-a4f7-3f00a484d183">

  The stripplot above shows us that in comparison to those in a censored status and those in a censored due to liver transplant status, more people in the advanced stages of liver cirrhosis did not make it (i.e. died).

> Visualization 2: *Stage of Cirrhosis in Relation to Sex* 
<p align = "center">
  <img src = "https://github.com/A-Kutscher/Project-2/assets/135680202/9c6eae73-41e7-4c65-9f45-af24def655c9">
</p>

  The countplot included above shows that women may have a higher susceptibility to liver cirrhosis due to differences in how their bodies process substances, like alcohol, and the potential influence of hormones. This insight highlights the need for gender-specific considerations in liver health management. 

## **MODEL METRICS & SELECTION**

### Final Model Description:

Several machine learning models were evaluated using important metrics such as precision, recall, F1 score, and accuracy to determine the best fit for the cirrhosis prediction task. Among the models considered, Logistic Regression demonstrated a balanced performance that makes it the most suitable choice for this problem.

### Important Metrics:

The key metrics for evaluating the final model's performance are as follows:
  - Precision for Training Data: 0.53
  - Recall for Training Data: 0.57
  - F1 Score for Training Data: 0.54
  - Accuracy for Training Data: 0.57
  - Precision for Training Data: 0.49
  - Recall for Training Data: 0.52
  - F1 Score for Training Data: 0.50
  - Accuracy for Training Data: 0.52

### Model's Solution to the Business Problem:

The Logistic Regression model was chosen as the best model because it strikes a good balance between identifying positive cases accurately and overall prediction precision. This balance is crucial in medical tasks. Also, Logistic Regression's simplicity helps medical professionals understand predictions, which is important for decision-making. Overall, due to its balanced performance and interpretability, Logistic Regression is the recommended choice for predicting liver cirrhosis in this context.

## **RECOMMENDATIONS**

1. **Gender-Specific Health Management:** Recognize the potential gender-based differences in liver health susceptibility highlighted by the analysis. Tailor health management strategies to address the distinct needs of both men and women.
2. **Early Intervention and Monitoring:** Implement proactive monitoring for patients in advanced stages of cirrhosis, focusing on early intervention to improve outcomes. Prioritize regular assessments and timely medical support.
3. **Treatment Optimization:** Investigate why some patients did not respond effectively to specialized treatment. Refine treatment protocols based on these findings to enhance the chances of positive outcomes across all stages of cirrhosis.
4. **Continuous Model Enhancement:** Regularly update and refine predictive models with the latest data to ensure their accuracy and applicability in real-world scenarios.

   By following these recommendations, stakeholders can leverage the insights gained from data analysis and the predictive models to make informed decisions that positively impact patient outcomes and healthcare management.

## **LIMITATIONS & FUTURE STEPS**

**Limitations:**

1. **Data Timeframe:** The dataset's age (1974-1984) might not reflect current medical practices and patient profiles, potentially limiting model applicability.

2. **Missing Factors:** The dataset might lack important variables affecting cirrhosis, possibly leaving out crucial contributors.

3. **Data Imbalance:** Some stages of cirrhosis might have fewer examples, affecting prediction accuracy.

4. **External Influences:** Environmental and lifestyle factors could influence cirrhosis risk but aren't captured in the dataset.

**Next Steps:**

1. **Recent Data:** Gather current data for a more accurate representation of patient profiles and practices.

2. **More Features:** Identify and include additional relevant factors for better predictions.

3. **Balance Handling:** Use techniques to address data imbalances and improve model performance.

4. **External Insights:** Integrate external data for a holistic understanding of cirrhosis risk factors.

5. **Advanced Techniques:** Explore advanced methods like neural networks to capture complex patterns.

6. **Real-world Validation:** Test models with real patient data to ensure practical value.

7. **Explainability:** Make complex models understandable for medical professionals.

8. **Continuous Improvement:** Establish a process for regular model updates based on new data and insights.

    By considering these aspects, stakeholders can create more accurate and practical models for cirrhosis prediction and management.
