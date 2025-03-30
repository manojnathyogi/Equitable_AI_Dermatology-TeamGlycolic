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

* Developed the final model leveraging transfer learning with pre-trained architectures (ResNet, EfficientNet, ConvNeXt) to classify 16 different skin conditions across diverse skin tones on the Fitzpatrick scale.

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
- The challenge required us to develop a model capable of classifying 21 different skin conditions while ensuring fairness across diverse skin tones.
- The evaluation metric, weighted F1 score, emphasized the importance of balanced performance across all classes.
- Projects like this ensure more competent AI algorithms in the health field, as we so regularly see how misrepresented groups get misdiagnosed due to professionals only studying the majority in the past.
- When developing the model, we wanted to be more socially responsible and include those values related to representation and diversity in our project.
  
---

## **📊 Data Exploration**

- We used the dataset provided by AJL, which is a subset of the FitzPatrick17k dataset, containing approximately 17,000 images depicting a variety of serious (e.g., melanoma) and cosmetic (e.g., acne) dermatological conditions. These images cover a range of skin tones, scored on the FitzPatrick skin tone scale (FST).  
  *FYI: The dataset is available on the competition page.*

- The dataset contains about 4,500 images representing 21 skin conditions out of the 100+ in the full FitzPatrick dataset.

- The Fitzpatrick scale ranges from 1 to 6, but we observed some rows containing an invalid value of -1, which is outside the expected range. To ensure data accuracy, we removed these rows from the dataset.

  ![Fitzpatrick Scale Distribution](https://github.com/user-attachments/assets/48341e7c-7d73-47fd-8ee3-6f6cc201f808)

---

- **Observation**: The Fitzpatrick scale and "Fitzpatrick_centaur" attributes show a moderate positive correlation but are not perfectly aligned.

- **Explanation**: Cultural differences in skin tone classification, as well as potential biases in data collection or subjectivity in manual assessments, may account for discrepancies between the two variables.

  ![Screenshot 2025-03-22 123139](https://github.com/user-attachments/assets/7ba3c1c3-5d1f-414a-a7f2-89b57b3dc566)

---

- Before training the model, we analyzed the distribution of skin conditions to identify any imbalances and explored strategies to mitigate them.

- To address the class imbalance issue, we implemented a strategy using a class weights dictionary, which was later fed into the model during training to ensure balanced learning across all classes.

  ![Label Distribution in Training Set](https://github.com/user-attachments/assets/a51729c1-f912-47bf-90b7-c6dd0a775b67)

- 
---

## **🧠 Model Development**

**Models Used:** 
- ResNet
- EfficientNet
- ConvNeXt

**Feature selection and Hyperparameter tuning strategies**

*Interation 1*
* As this is a computer vision problem, the features extracted from the dataset were limited to the image paths and the corresponding labels, which were encoded into integers.
* The core approach involved leveraging pre-trained image classification models as the base, and fine-tuning the model by adding dense layers and dropout layers to mitigate overfitting.
* To transition from the base model to the additional layers, we used GlobalAveragePooling2D(), which aggregates feature maps by averaging their values, reducing spatial dimensions and the risk of overfitting while maintaining key features for classification.

*Interation 2*
* We noticed that the model wasn’t effectively learning from our dataset, so we unfreezed some of the last layers of the pre-trained models. We then experimented with the optimal number of layers to unfreeze, balancing between retaining the knowledge learned from the ImageNet dataset and allowing the model to better adapt to our specific dataset.
* Initially, we considered increasing the number of epochs to give the model more time to learn patterns from the dataset. However, after a certain point, the validation accuracy plateaued, indicating that the learning rate was too low. As a result, we adjusted the learning rate from 1e-4 to 1e-3 to improve convergence.

*Iteration 3*
* After increasing the learning rate to 1e-3, the model started to overfit, learning the training data but failing to generalize well. To address this, we implemented a learning rate reduction callback, which dynamically reduces the learning rate when the validation accuracy begins to plateau.
* Additionally, for models with relatively fewer layers, such as ResNet50, we needed to train for more epochs to allow the model to effectively learn from the dataset.

**Training setup (e.g., % of data for training/validation, evaluation metric, baseline performance)**

* Training and validation data had a ratio of 80:20
* Training evaluation metric: Validation accuracy
* Baseline Performance: 0.3 - 0.4 

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

