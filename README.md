# MLAWS_course

## Introduction

This is my assignment and project for the Machine Learning Cloud  course I took in my master degree at University of illinois at Urbana Champain, focusing on Building a machine learning pipeline on AWS. The assignments focus on using AWS services. The project aims to predict whether a review is helpful and Identify the most representative review using textual analysis, metadata engineering, and machine learning.

## Data Source

The dataset used in this project is the [Amazon Fine Food Reviews](https://www.kaggle.com/datasets/snap/amazon-fine-food-reviews) from Kaggle. It contains Amazon product reviews, including fields such as review text, timestamp, rating score, and helpfulness (numerator and denominator).

⚠️ Note: The original CSV file (Reviews.csv) is 286.97 MB and exceeds GitHub’s 100 MB upload limit, so it is not included in this repository. Please download it manually from Kaggle if needed.


## Tools and technical skills

- **Python**
- **technical skills for assignment**:
 AWS service: S3, Recognition, Sagemaker
 
- **technical skills for project**
1. Data Preprocessing: Text cleaning (stopword removal, lemmatization), TF-IDF vectorization, dimensionality reduction (TruncatedSVD), and standardization using StandardScaler.
2. Semantic Analysis: Used a pre-trained Sentence-BERT model (all-MiniLM-L6-v2) to compute cosine similarity between reviews for representativeness scoring.
3. Modeling: Applied XGBoost Classifier to predict HelpfulBinary using combined textual and metadata features. Addressed class imbalance using scale_pos_weight.
4. Cloud Infrastructure: Utilized AWS S3 for data storage and SageMaker for training and model management.
5. Evaluation: Compared model performance using Accuracy, F1-Score, Confusion Matrix. Analyzed helpfulness across representative, random, and all reviews.


## Repository Structure

```plaintext
MLAWS_course/
│
├── README.md
├── AWS_Rekognition/ – Folder containing one assignment using AWS Rekognition and S3.
│   ├── data/
│   ├── notebooks/ contains .ipynb and .pdf versions of the code for easy review.   
│        ├── cv_pipeline.ipynb
│        ├── cv_pipeline.pdf
│        ├── screenshots/  – Folder contains screenshots used by notebooks
│   └── report/   – Folder containing the project report details in .pdf format.
│
├── AWS_Sagemaker/  –  Folder containing one assignment using AWS Sagemaker and S3.
│   ├── data/
│   ├── notebooks/  – contains .ipynb, .html, and .pdf versions of the code for easy review.   
│        ├── YiHsuan_SageMaker_regression.html
│        ├── YiHsuan_SageMaker_regression.ipynb
│        ├── YiHsuan_SageMaker_regression.pdf
│   └── requirements.txt – Only lists packages used in this assignment
│
├── NLP_project/ – Folder containing my project using AWS service.
│   ├── data/
│        ├── cosine_avg_sim_results.csv  – Output of my part (average cosine similarity per review)
│   ├── notebooks/ – contains .ipynb, .html, and .pdf versions of the code for easy review.   
│        ├── YiHsuan_code_final.html
│        ├── YiHsuan_code_final.ipynb
│        ├── YiHsuan_code_final.pdf
│   ├── report/ – Folder containing the project report and presentation details in .pdf format.
│        ├── Final_Presentation.pdf – The slides we presented. I worked on the second part of the this PPT.
│        ├── Group_10_Final_Report_MLC.pdf  – The report we submitted. I worked on the third part of the this report.
│   └── requirements.txt – Only lists packages used in this NLP project

```

## Usage

You can open any notebook in the `notebooks/` folders to review the work. PDF and HTML versions are also available for easier preview.
To install dependencies:
```bash
pip install -r requirements.txt
```

## Contact Information

For any further questions or collaboration opportunities, please reach out to me at:
- Email: [yguo8395@gmail.com](mailto:yguo8395@gmail.com)
- LinkedIn: [Iris Kuo](https://www.linkedin.com/in/yi-hsuan-kuo-835b00268/)
- GitHub: [Iris Kuo](https://github.com/Iris910531)
