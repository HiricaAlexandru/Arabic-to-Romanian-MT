Official paper for **Arabic to Romanian Machine Translation: A Case Study on Distant Language Pairs.**

The `evaluation_dataset` folder contains the test dataset used in the paper. It comprises a mix of out-of-domain (OOD) documents, a standard benchmark dataset, and in-domain training data.  

### Dataset Overview

| Document              | Source        | Sentences |
|-----------------------|--------------|-----------|
| Saudi-Romania Econ.   | State AGT.   | 189       |
| Geneva Convention     | UN           | 330       |
| Children Rights       | UN           | 217       |
| Economic Rights       | UN           | 124       |
| Human Rights          | UN           | 79        |
| Refugee Status        | UN           | 177       |
| Saudi Embassy         | X           | 86        |
| **Total OOD**         |              | **1202**  |
| FLORES+               | Huggingface  | 997       |
| In-Domain             | Training Data| 2100      |
| **Grand Total**       | -            | **4299**  |

The `code` folder contains all the notebooks used in creating the paper's experiments
