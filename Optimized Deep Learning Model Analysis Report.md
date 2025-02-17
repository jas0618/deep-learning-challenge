## **Overview**

This analysis aims to develop a deep learning model capable of predicting the success of charity applications based on key features. The dataset undergoes thorough preprocessing to enhance model performance, with the ultimate goal of achieving a predictive accuracy greater than **75%**.

---

## **Results**

### **Data Preprocessing**

* **Target Variable:**  
  * The model's target variable is **"IS\_SUCCESSFUL"**, which indicates whether a charity application was approved.  
* **Feature Variables:**  
  * All relevant columns, excluding ID-related variables and the target variable, serve as features. The most significant ones include:  
    * **APPLICATION\_TYPE** – Type of application submitted.  
    * **AFFILIATION** – Organization’s affiliation type.  
    * **CLASSIFICATION** – Assigned nonprofit classification.  
    * **USE\_CASE** – Purpose for which funding is requested.  
    * **ORGANIZATION** – Type of organization.  
    * **STATUS** – Application status.  
    * **INCOME\_AMT** – Income category of the organization.  
    * **SPECIAL\_CONSIDERATIONS** – Special considerations (if applicable).  
    * **ASK\_AMT** – Requested funding amount.  
* **Removed Variables:**  
  * **"EIN"** and **"NAME"** were excluded as they do not contribute to predictive accuracy.

---

### **Model Development and Evaluation**

* **Neural Network Architecture:**  
  * The model comprises **four hidden layers**, structured as follows:  
    * **Layer 1**: 512 neurons, ReLU activation.  
    * **Layer 2**: 256 neurons, ReLU activation.  
    * **Layer 3**: 128 neurons, ReLU activation.  
    * **Layer 4**: 64 neurons, ReLU activation.  
    * **Output Layer**: 1 neuron, Sigmoid activation (for binary classification).  
  * **ReLU** was chosen for hidden layers due to its efficiency in deep networks, while **Sigmoid** was applied to the output layer to generate probability-based predictions.  
* **Performance Results:**  
  * The initial model failed to exceed the **75% accuracy threshold**.  
  * After optimizations, the model successfully surpassed **75% accuracy**.  
* **Key Enhancements to Improve Performance:**  
  * **Feature Engineering:** Removed non-contributing variables (`EIN`, `NAME`).  
  * **Data Normalization:** Standardized numerical features using `StandardScaler`.  
  * **Enhanced Model Complexity:** Increased the number of neurons and layers for better learning.  
  * **Batch Normalization:** Implemented after each hidden layer to improve stability and speed up convergence.  
  * **Dropout Regularization:** Prevented overfitting by randomly deactivating neurons during training.  
  * **Optimized Learning Rate:** Used `Adam` optimizer with a reduced learning rate (`0.0002`).  
  * **Early Stopping & Learning Rate Scheduling:** Prevented overfitting and dynamically adjusted the learning rate for efficient learning.

---

## **Summary and Recommendations**

### **Final Results**

* After multiple refinements, the deep learning model **achieved over 75% accuracy**, meeting the target benchmark.  
* Careful preprocessing and model adjustments significantly contributed to improving predictive performance.  
* Applying regularization techniques (dropout, batch normalization) helped prevent overfitting.  
* Adjusting the learning rate allowed the model to converge more effectively.

---

### **Conclusion**

The deep learning model successfully **exceeded 75% accuracy** after systematic optimizations. Future work could explore **XGBoost, Random Forest, or AutoML solutions** for even greater performance, efficiency, and interpretability.

