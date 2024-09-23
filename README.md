# 📊 **AloDokter Sentiment Analysis with Indonesian Language Reviews**

I performed **scraping** on Google Play Store reviews for the **AloDokter** app, where the reviews are written in **Indonesian**. Given the limited availability of libraries or models specifically tailored for the Indonesian language, I conducted a series of experiments to explore sentiment analysis for this dataset.

---

## 🔬 **Experiments Overview**

### **INA v.1: Sentiment Analysis with TextBlob** 
- **Method**: Used the **TextBlob** library, which is primarily built for **English**.
- **Result**: 
  - Out of **25k reviews**, only a few were successfully labeled for sentiment polarity.
  - Most reviews could not be labeled due to TextBlob’s limitations for **non-English** texts.
  
📉 **Conclusion**: TextBlob is not suitable for Indonesian-language sentiment analysis.

---

### **INA v.2: Zero Shot Learning with IndoBERT** 
- **Method**: Applied **Zero Shot Learning** using **IndoBERT** in an **unsupervised** learning.
- **Dataset**: Used **3k reviews**.
- **Accuracy**: Achieved **34%**, showing that the model was not very accurate in predicting labels.
  
⚙️ **Tip for Improvement**: Enhancing the **quality of label descriptions** or using a **better pre-trained model** can significantly boost accuracy.

---

### **INA v.3: Fine-Tuned IndoBERT (Supervised Learning)** 
- **Method**: Fine-tuned **IndoBERT** in a **supervised** learning.
- **Dataset**: Manually labeled **150 reviews**:
  - **50 Positive (0)** 
  - **50 Neutral (1)** 
  - **50 Negative (2)**
  - Training/testing split of **80:20**.
- **Accuracy**: Achieved **63.33%** accuracy.
  
🛠 **Next Steps**:
  - The model was then used to label an additional **3k reviews** automatically.
  - The model performed well for **negative sentiments** but struggled with **neutral** and **positive** sentiments due to ambiguous data and limited training.

⚙️ **Tip for Improvement**: Increasing the size of the **labeled dataset** and reducing **ambiguous data** can further enhance the model's performance.

---

## 🎯 **Final Thoughts**

This project demonstrates the challenges and potential solutions for **Indonesian-language** sentiment analysis using different models and approaches. Future iterations will focus on improving accuracy and handling more complex sentiment detection.

---
