# Intrusion-Detection-System
Welcome to my Intrusion Detection System (IDS) project utilizing the big data capabilities of Apache Spark. This repository contains code for three main components of the system:

1. **Baseline Model**: A baseline model for data analysis and comparison to measure the performance improvements achieved by the binary and multiclass classification models.

2. **Binary Classification Model**: A binary classification model to detect and classify network intrusions as either normal or malicious.

3. **Multiclass Classification Model**: A multiclass classification model to categorize network intrusions into various predefined attack types.

## Getting Started

### Prerequisites

To run and experiment with the code in this repository, you'll need the following:

- Apache Spark (version 3.4.1)
- Python
- Hadoop
- Java JDK
- Anaconda (optional but recommended)
- Jupyter Labs (optional but recommended)

**Usage**
Navigate to the specific folder for the component you want to use (e.g., baseline-model, binary-classification, or multiclass-classification).

Open and run the Jupyter Notebook or Python script associated with the component you wish to work with.

Follow the instructions and comments within the code to analyze and experiment with the dataset and model.

**Data**
The data used in this project is not included in this repository due to its size. You can obtain the dataset from https://cloudstor.aarnet.edu.au/plus/index.php/s/2DhnLGDdEECo4ys?path=%2FUNSW-NB15%20-%20CSV%20Files and place it in the data directory within each component's folder.

**Results**

![image](https://github.com/adekola-byte/Intrusion-Detection-System/assets/143772258/024d57c7-f1f9-4f26-b513-9667a16919d6)

The results above were obtained from the binary classification baseline model before the proposed approach was tested

![image](https://github.com/adekola-byte/Intrusion-Detection-System/assets/143772258/7cd3cca5-de56-4a41-a27d-8b2d4e05de5e)

The results above were obtained from the Multiclass classification baseline model before the proposed approach was tested

![image](https://github.com/adekola-byte/Intrusion-Detection-System/assets/143772258/d618eeaa-dd69-44c6-8ef8-4065252d89dd)

The results above were obtained from the binary classification model of the proposed approach.

![image](https://github.com/adekola-byte/Intrusion-Detection-System/assets/143772258/be106aff-7405-4738-8ddc-04dc03b49641)

The results above were obtained from the binary classification  model after using features that were identified as the most important by decision trees

![image](https://github.com/adekola-byte/Intrusion-Detection-System/assets/143772258/db2dea5c-ce31-49cd-8be3-4f57eb565fe6)

The results above were obtained from the Multi class classification model of the proposed approach.

![image](https://github.com/adekola-byte/Intrusion-Detection-System/assets/143772258/7a406e10-5f99-4ea7-86bb-4ac67990ac9a)

The results above were obtained from the Multi class classification model after using features that were identified as the most important by decision trees

Upon retraining the model using the identified relevant features, the Decision trees model performed better with a significant reduction of the False Alarm Rate from 0.113133  to 0.023492 which is a 79.24% reduction in the False Alarm Rate, and a notable increase of the F1 Score from 0.848809 to 0.97368 signifying a 14.7% improvement. The random Forest Model however did not show any significant changes after retraining. The F1 Score reduced slightly from 0.972862 to 0.976227 while the False Alarm Rate increased from 0.024702 to 0.021888 signifying a 11.39% improvement. These findings hold major significance as it provides insight into a possible solution for reducing False Alarm rates in intrusion detection system which usually poses a major challenge. In addition, the proposed method also showed better performance than the initial base model which indicates the efficiency of our proposed feature selection method.

![image](https://github.com/adekola-byte/Intrusion-Detection-System/assets/143772258/780d54e4-60e9-4e89-a103-94fc438f238e)

Comparing the proposed solution for Binary classification to other existing solutions

![image](https://github.com/adekola-byte/Intrusion-Detection-System/assets/143772258/d1e75d30-392c-4285-8499-1ca31d351aa7)

Comparing the proposed solution for Multiclass classification to other existing solutions

**Conclusion**

The proposed PySpark-based approach demonstrates strengths in terms of AUC scores and False Alarm Rates for most of the models under comparison. However, the pre-existing pandas solution by Maji (2020) excels in F1 Scores for a greater number of models.

PySpark leverages a distributed processing framework, enabling the distribution of computations across multiple nodes or machines within a cluster. This distributed framework offers the potential to enhance model convergence and performance, particularly when handling large-scale and complex datasets. Traditional machine learning tasks on a single machine may face limitations due to memory and processing power constraints. In contrast, PySpark's distributed processing divides the workload into smaller chunks, distributing them to different nodes for parallel execution.

PySpark also incorporates optimization techniques tailored for distributed computing environments, aiming to minimize data movement across nodes. In the case of imbalanced datasets, where minority class instances are crucial, reducing excessive data shuffling helps prevent the loss of information and speeds up model convergence.

The reduction in data shuffling and optimized resource allocation may lead to a decrease in the False Alarm Rate (FAR), a critical consideration in imbalanced dataset scenarios. PySpark's optimization strategies manage resource allocation dynamically, allocating more resources to tasks requiring intensive computation. This dynamic allocation helps avoid resource bottlenecks, ultimately influencing model convergence and accuracy.

The influence of these optimization techniques in reducing computational bottlenecks and efficiently handling memory can contribute to higher AUC scores. A model that converges faster and utilizes resources more efficiently is likely to exhibit better discrimination power.

While the pandas approach achieved better F1 scores in more models, it's important to note that in cases where the dataset comfortably fits in memory, pandas can make the most of available resources, resulting in efficient execution of algorithms and potentially influencing F1 scores.

**Contact**

For any questions or feedback, please feel free to contact me at adekola-byte@outlook.com

Thank you for your interest in my Intrusion Detection System project. Look forward to your contributions and feedback!
