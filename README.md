# ReceiptQA: A Comprehensive Dataset for Receipt Understanding and Question Answering

ReceiptQA is a large-scale dataset specifically designed to support and advance research in receipt understanding through question-answering (QA) tasks. This dataset offers a wide range of questions derived from real-world receipt images, addressing diverse challenges such as text extraction, layout understanding, and numerical reasoning. ReceiptQA provides a benchmark for evaluating and improving models for receipt-based QA tasks.


## Example of Receipts
<p align="center">
  <img src="images/example1.jpg" alt="Image 1" width="300"/>
  <img src="images/example2.jpg" alt="Image 2" width="300"/>
</p>
## Dataset Overview
ReceiptQA consists of 3,500 receipt images paired with 171,000 question-answer pairs, constructed using two complementary approaches:

1. **LLM-Generated Subset:** 70,000 QA pairs generated by GPT-4o, validated by human annotators to ensure accuracy and relevance.
2. **Human-Created Subset:** 101,000 QA pairs crafted manually, including both answerable and unanswerable questions for diverse evaluation.

### Key Features:
- Covers five domains: Retail, Food Services, Supermarkets, Fashion, and Medical.
- Includes both straightforward and complex questions.
- Offers a comprehensive benchmark for receipt-specific QA tasks.

### Dataset Statistics
| Domain          | Receipts | Human QA Pairs | LLM QA Pairs |
|-----------------|----------|----------------|--------------|
| Retail          | 800      | 23,200         | 16,000       |
| Food Services   | 700      | 20,300         | 14,000       |
| Supermarkets    | 700      | 20,300         | 14,000       |
| Fashion         | 650      | 18,850         | 13,000       |
| coffe shop        | 650      | 18,850         | 13,000       |
| **Total**       | **3,500**| **101,935**    | **70,000**   |

### Example of Data

Here is a sample of the data structure used in the ReceiptQA dataset:

```json
{
  "question": "What is the total amount for this receipt?",
  "answer": "559.99 L.E"
},
{
  "question": "What is the name of item 1?",
  "answer": "Pullover PU-SOK1175"
},
{
  "question": "What is the transaction number?",
  "answer": "29786"
},
{
  "question": "How many items were purchased?",
  "answer": "2"
}

## Requirements
```bash
# Install required libraries for inference
pip install torch==1.10.0
pip install transformers==4.5.0
pip install datasets==2.3.0
pip install Pillow
```



## Download Links

### Full Dataset
- **Train Set :** [Download](https://example.com/train.json)
- **Validation Set :** [Download](https://example.com/val.json)
- **Test Set :** [Download](https://example.com/test.json)


## Using ReceiptQA
To use ReceiptQA for training or evaluation, follow these steps:

### Step 1: Clone the Repository
```bash
git clone https://github.com/your-repo/ReceiptQA](https://github.com/MahmoudElsayedMahmoud/ReceiptQA-A-Comprehensive-Dataset-for-Receipt-Understanding-and-Question-Answering
cd ReceiptQA
```

### Step 2: Download the Dataset
Download the dataset using the links provided above and place it in the `data/` directory.


## Evaluation Metrics
ReceiptQA provides the following metrics for evaluating QA models:
- **Exact Match (EM):** Measures if the predicted answer exactly matches the ground truth.
- **F1 Score:** Evaluates the overlap between the predicted and ground truth answers.
- **Precision:** Measures the accuracy of the predictions.
- **Recall:** Measures the ability to retrieve relevant answers.
- **Answer Containment:** Checks if the ground truth answer is included in the predicted response.

## Models Benchmarked
ReceiptQA has been used to evaluate state-of-the-art models, including:
- **GPT-4**
- **Llama3.2 (11B)**
- **Gemni 2.0**
- **Phi 3.5 Vision**
- **InternVL2 (4B/8B)**
- **LLaVA 7B**



## Citation
If you use ReceiptQA in your research, please cite our paper:
```
Will be publish soon !!
```



## Contact
For questions or feedback, please contact:
- Mahmoud Abdalla: [mahmoudelsayed@chungbuk.ac.kr](mailto:mahmoudelsayed@chungbuk.ac.kr)
- GitHub Issues: [Submit an issue](https://github.com/your-repo/ReceiptQA/issues)
