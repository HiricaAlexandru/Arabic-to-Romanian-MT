Official paper for **Arabic to Romanian Machine Translation: A Case Study on Distant Language Pairs.**

The `evaluation_dataset` folder contains the test dataset used in the paper. It comprises a mix of out-of-domain (OOD) documents, a standard benchmark dataset, and in-domain training data.  

## Dataset Overview

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


## Evaluation Results

### Out-of-Domain

| Model                         | MetricX | CometKiwi | AutoRank |
|-------------------------------|---------|-----------|----------|
| Human                         | --      | 0.019     | --       |
| Gemini-flash-002              | -0.624  | 1.100     | 2.699    |
| GPT-4                         | -0.624  | 1.472     | 2.807    |
| Fine-tuned RoLLama3.1-8b      | -0.573  | 2.890     | 3.733    |
| Fine-tuned RoMistral-7b       | -0.557  | 2.926     | 3.905    |
| Pre-trained RoLLama3.1-8b     | -0.530  | 3.764     | 4.421    |
| Jais+Transf                   | -0.529  | 4.036     | 4.513    |
| Pre-trained NLLB-600M         | -0.535  | 4.443     | 4.577    |
| Fine-tuned NLLB-600M          | -0.537  | 4.703     | 4.638    |
| Transf (Dialects removed)     | -0.535  | 5.554     | 4.908    |
| Pre-trained RoMistral-7b      | -0.486  | 4.471     | 5.067    |
| Transf (Duplicates removed)   | -0.495  | 5.017     | 5.140    |
| Transf (Gemini filter)        | -0.477  | 5.099     | 5.350    |
| Transf (Lealla filter)        | -0.469  | 5.265     | 5.473    |

---

### FLORES+

| Model                         | MetricX | CometKiwi | AutoRank |
|-------------------------------|---------|-----------|----------|
| Human                         | --      | 0.022     | --       |
| GPT-4                         | -0.736  | 0.986     | 1.551    |
| Gemini-flash-002              | -0.729  | 0.958     | 1.614    |
| Fine-tuned RoLLama3.1-8b      | -0.664  | 1.979     | 2.559    |
| Fine-tuned RoMistral-7b       | -0.653  | 2.496     | 2.823    |
| Pre-trained RoLLama3.1-8b     | -0.644  | 2.606     | 2.950    |
| Transf (Duplicates removed)   | -0.633  | 2.922     | 3.148    |
| Transf (Lealla filter)        | -0.632  | 3.114     | 3.216    |
| Fine-tuned NLLB-600M          | -0.628  | 3.045     | 3.242    |
| Jais+Transf                   | -0.603  | 2.720     | 3.394    |
| Pre-trained NLLB-600M         | -0.617  | 3.336     | 3.435    |
| Transf (Gemini filter)        | -0.615  | 3.309     | 3.442    |
| Transf (Dialects removed)     | -0.610  | 3.260     | 3.478    |
| Pre-trained RoMistral-7b      | -0.534  | 4.597     | 4.632    |

---

### In-Domain

| Model                         | MetricX | CometKiwi | AutoRank |
|-------------------------------|---------|-----------|----------|
| Human                         | --      | 0.033     | --       |
| GPT-4                         | -0.693  | 1.415     | 2.110    |
| Gemini-flash-002              | -0.681  | 1.409     | 2.227    |
| Transf (Duplicates removed)   | -0.625  | 1.798     | 2.894    |
| Transf (Lealla filter)        | -0.620  | 1.849     | 2.963    |
| Transf (Dialects removed)     | -0.618  | 1.865     | 2.989    |
| Fine-tuned RoMistral-7b       | -0.623  | 2.089     | 3.005    |
| Transf (Gemini filter)        | -0.616  | 1.874     | 3.011    |
| Fine-tuned NLLB-600M          | -0.611  | 2.081     | 3.117    |
| Pre-trained NLLB-600M         | -0.600  | 2.241     | 3.280    |
| Fine-tuned RoLLama3.1-8b      | -0.586  | 2.871     | 3.600    |
| Pre-trained RoLLama3.1-8b     | -0.584  | 3.097     | 3.689    |
| Pre-trained RoMistral-7b      | -0.531  | 3.954     | 4.474    |
| Jais+Transf                   | -0.140  | 18.700    | 12.745   |

---


The `code` folder contains all the notebooks used in creating the paper's experiments


The `XCOMET-XL Error Analysis Results` folder contains the results and statistics of the error analysis performed in the paper using [XCOMET-XL](https://huggingface.co/Unbabel/XCOMET-XL) 
