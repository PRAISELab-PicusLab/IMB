# ⚕️ IMD (Italian Medical Dataset) 🇮🇹

**IMD (Italian Medical Dataset)** is a cutting-edge resource for **Natural Language Processing (NLP)** in the medical domain, specifically designed to improve the accuracy and reliability of **Question Answering (QA)** models in the **Italian language**. The dataset is split into two primary components:

- **IMD-QA**: Questions and answers extracted from Italian medical forums, reflecting informal language used by patients and healthcare professionals.
- **IMD-MCQA**: Multiple-choice questions from Italian medical specialization exams, ideal for training models focused on structured and formal medical queries.

## 🌟 Key Features


## 📊 Dataset Statistics

| Statistic                        | IMD-QA                  | IMD-MCQA              |
|-----------------------------------|-------------------------|-----------------------|
| **# Questions and Answers**       | 782,644                 | 25,862                |
| **# Categories**                  | 77                      | 60                    |
| **Last Update**                   | July 2024               | July 2024             |
| **Total Answer Tokens**           | 40,370,381              | 9,321                 |
| **Unique Answer Vocabulary**      | 154,837                 | 1,234                 |
| **Total Question Tokens**         | 137,129,435             | 282,239               |
| **Unique Question Vocabulary**    | 1,397,929               | 19,214                |
| **Unique Total Vocabulary**       | 1,552,766               | 20,448                |

## 📏 Average & Max Lengths

| Statistic                        | IMD-QA                  | IMD-MCQA              |
|-----------------------------------|-------------------------|-----------------------|
| **Average Answer Length**         | 352.05 tokens           | 9.3 tokens            |
| **Max Answer Length**             | 9,817 tokens            | 21 tokens             |
| **Average Question Length**       | 1,056.77 tokens         | 10.91 tokens          |
| **Max Question Length**           | 13,390 tokens           | 124 tokens            |

## 🧹 Preprocessing

### IMD-QA 🧑‍⚕️

- **Data Cleaning**: Removal of incomplete or truncated questions, metadata (doctor signatures, timestamps), and textual inconsistencies while preserving the original medical intent.
- **Text Normalization & Answer Reformulation**: Answers were reformulated using **Llama3-Med42-8B**, a Large Language Model (LLM) fine-tuned for medical applications. The focus was on:
  - Eliminating redundancy and colloquial language.
  - Ensuring stylistic consistency across responses.
  - Enhancing readability and grammatical accuracy.
- **Anonymization**: The model identified and removed personally identifiable information (PII) such as patient names, doctor names, healthcare facilities, etc.

### IMD-MCQA 📝

- **Data Organization**: The dataset's multiple-choice questions were already structured, so the preprocessing mainly focused on standardizing the data format and ensuring consistency across entries.

## 🏷️ Data Categorization

The **IMD-QA** dataset was organized into major categories using **unsupervised topic modeling**. Techniques like **BERTopic**, **UMAP**, and **HDBSCAN** were used to group semantically similar questions into macro-categories. This approach enables flexible and interpretable categorization without rigid constraints.

### General Categories and Question Distribution

| **Category**                                           | **# Questions** |
|--------------------------------------------------------|-----------------|
| Urology, Andrology, and Male Health                    | 110,052         |
| Gastroenterology and Digestive Health                  | 104,449         |
| Mental Health                                          | 103,893         |
| General Medicine and General Surgery                   | 87,789          |
| Ophthalmology, Otorhinolaryngology, Dentistry, and Pneumology | 83,710       |
| Cardiology, Circulatory System, and Hematology         | 81,232          |
| Gynecology and Female Health                           | 65,792          |
| Orthopedics and Musculoskeletal System                 | 50,283          |
| Dermatology, Allergies, and Aesthetics                 | 49,288          |
| Neurology                                              | 46,704          |

## ⚙️ How to Use the Dataset

To use the dataset, simply download the repository and access the **CSV** or **JSON** files containing the questions and answers. Each file has been pre-processed to facilitate integration with NLP models, including those designed for **Question Answering**.

## 📜 License

This dataset is released under the [Insert License Name], allowing its use and modification for research purposes, in accordance with the terms outlined in the license.

## 🤝 Contributing

We welcome contributions to improve the dataset! To contribute, simply open a pull request or report issues on our [issue tracker](https://github.com/[Username]/IMD/issues). We look forward to your improvements!

## 📧 Contact

For further inquiries, contact us at: [email@example.com].

---

### 🌐 Notes

- **Data Cleaning & Anonymization**: Preprocessing steps have been applied to ensure privacy and data integrity while keeping the content relevant for medical applications.
- **Dataset Usage**: The dataset is intended for academic and research purposes only. It is not recommended for clinical decision-making or commercial use.
