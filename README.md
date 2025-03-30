# Equitable AI for Dermatology, AJL Kaggle Competition


## **👥 Team Members**
| Name | GitHub Handle | Contribution |
| ----- | ----- | ----- |
| Bode Chiu | [@BootyChu](https://github.com/BootyChu) | Model Improvement |<br />
| Erica Xue | [@ericaxuee](https://github.com/ericaxuee) | Model Improvement |<br />
| Manoj Nath Yogi | [@manojnathyogi](https://github.com/manojnathyogi) | Data Visualization and Model Development | <br />
| Natalie Kao | [@nataliekao03](https://github.com/nataliekao03) | Model Improvement |<br />
| Smila Gala | [@Smila3](https://github.com/Smila3) | Initial EDA and updating README | <br />
| Sneha Nangunoori | [@snehanangunoori](https://github.com/snehanangunoori) | Model Development and Improvement | <br />
| Precious Onah | [preciousonah](https://github.com/preciousonah) | Model Improvement |<br />

---

## **🎯 Project Highlights**

* Developed the final model leveraging pre-trained architectures (ResNet, EfficientNet, ConvNeXt) to classify 16 different skin conditions across diverse skin tones on the Fitzpatrick scale.

* Attained an F1 score of 0.61, securing 13th place out of 74 teams on the final Kaggle leaderboard.

* Employed image generation and augmentation techniques to enhance dataset diversity and model generalization.

🔗 [Equitable AI for Dermatology | Kaggle Competition Page](https://www.kaggle.com/competitions/bttai-ajl-2025/overview)

---

## **👩🏽‍💻 Setup & Execution**

**How to run the Notebooks:**


* Clone the repository in the terminal of your preferred IDE
  ```bash
  git clone https://github.com/manojnathyogi/Equitable_AI_Dermatology-TeamGlycolic.git
  cd Equitable_AI_Dermatology-TeamGlycolic
  ```
* Make sure to download the datasets provided in the competition link, and paste them in the same directory as the notebooks
* These notebooks can run in IDEs like Visual Studio Code, but we recommend opening it in the Kaggle or Jupyter Notebook sites


---

## **🏗️ Project Overview**

- Our project was part of a Algorithmic Justic League (AJL) Kaggle competition linked to the Break Through Tech AI Program, aiming to advance AI-driven healthcare solutions.
- The challenge required us to develop a model capable of classifying 16 different skin conditions while ensuring fairness across diverse skin tones.
- The evaluation metric, weighted F1 score, emphasized the importance of balanced performance across all classes.
- Projects like this ensure more competent AI algorithms in the health field, as we so regularly see how misrepresented groups get misdiagnosed due to professionals only studying the majority in the past.
- When developing the model, we wanted to be more socially responsible and include those values related to representation and diversity in our project.
  
---

## **📊 Data Exploration**

* We used the dataset provided by AJL, which contains a wide variety of skin condition images. To train the model, we wanted to get an idea of what kind of conditions are more represented and think on how we could address this disparity. You can find the actual dataset in the competition page.
* Below you can find our bar charts and confussion matrix.

![Screenshot 2025-03-22 123240](https://github.com/user-attachments/assets/48341e7c-7d73-47fd-8ee3-6f6cc201f808)
![Screenshot 2025-03-22 123139](https://github.com/user-attachments/assets/7ba3c1c3-5d1f-414a-a7f2-89b57b3dc566)
![Screenshot 2025-03-22 123224](https://github.com/user-attachments/assets/a51729c1-f912-47bf-90b7-c6dd0a775b67)

---

## **🧠 Model Development**

**Describe (as applicable):**

* Model(s) used: DenseNet
* Feature selection and Hyperparameter tuning strategies
* Training setup (e.g., % of data for training/validation, evaluation metric, baseline performance)

---

## **📈 Results & Key Findings**

**Describe (as applicable):**

* Performance metrics (e.g., Kaggle Leaderboard score, F1-score)
* How your model performed overall
* How your model performed across different skin tones (AJL)
* Insights from evaluating model fairness (AJL)

**Potential visualizations to include:**

* Confusion matrix, precision-recall curve, feature importance plot, prediction distribution, outputs from fairness or explainability tools

---

## **🖼️ Impact Narrative**

**Answer the relevant questions below based on your competition:**

**AJL challenge:**

As Dr. Randi mentioned in her challenge overview, “Through poetry, art, and storytelling, you can reach others who might not know enough to understand what’s happening with the machine learning model or data visualizations, but might still be heavily impacted by this kind of work.”
As you answer the questions below, consider using not only text, but also illustrations, annotated visualizations, poetry, or other creative techniques to make your work accessible to a wider audience.
Check out [this guide](https://drive.google.com/file/d/1kYKaVNR\_l7Abx2kebs3AdDi6TlPviC3q/view) from the Algorithmic Justice League for inspiration!

1. What steps did you take to address [model fairness](https://haas.berkeley.edu/wp-content/uploads/What-is-fairness_-EGAL2.pdf)? (e.g., leveraging data augmentation techniques to account for training dataset imbalances; using a validation set to assess model performance across different skin tones)
2. What broader impact could your work have?

---

## **🚀 Next Steps & Future Improvements**

**Address the following:**

* What are some of the limitations of your model?<br />
  We had some difficulties with the model overfitting the data and inconsistencies with our results after running the model several times
* What would you do differently with more time/resources? <br />
  With more time and resources we could have researched better the reason behind the inconsistencies of our results and work around those
* What additional datasets or techniques would you explore? <br />
  We would explore different techniques related to ensemble models and other image-oriented EDA

---

## **📄 References & Additional Resources**

1. [Create custom Data Generator for TensorFlow](https://medium.com/analytics-vidhya/write-your-own-custom-data-generator-for-tensorflow-keras-1252b64e41c3)
2. [Sample Keras Image Classification Models](https://keras.io/examples/vision/image_classification_from_scratch/)
3. [Ensemble Model Tutorials](https://pytorch.org/tutorials/intermediate/ensembling.html)
4. [Fine-Tuning Resources part 1](http://restack.io/)
5. [Fine-Tuning Resources part 2](https://huggingface.co/docs/transformers/en/training)

---

