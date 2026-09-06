a# Evaluation – College Knowledge Assistant

## Evaluation Objective

The system is evaluated to check whether it retrieves relevant information from the college knowledge base and provides grounded answers instead of relying on unsupported information.

## Test Cases

| Test Case | Query | Expected Behaviour |
|---|---|---|
| TC01 | What percentage of attendance is required to be eligible for the final examination? | The assistant should answer that 75% attendance is required. |
| TC02 | What happens if a student's attendance is between 65% and 75%? | The assistant should explain that examination eligibility may require approval from the academic department. |
| TC03 | What happens if attendance is below 65%? | The assistant should explain that the student may be detained from the final examination according to college rules. |
| TC04 | What is the admission process of the college? | If the information is not present in the knowledge base, the assistant should say that it could not find the information. |
| TC05 | Ask a college-related question that is not covered by the available documents. | The assistant should avoid inventing an answer and return the knowledge-base fallback response. |

## Evaluation Criteria

The responses are evaluated using the following criteria:

1. **Retrieval Relevance** – Did the system retrieve information relevant to the question?
2. **Answer Correctness** – Does the response match the retrieved institutional information?
3. **Groundedness** – Is the answer based on the retrieved knowledge rather than unsupported model knowledge?
4. **Fallback Handling** – Does the assistant avoid making up information when the answer is unavailable?

## Sample Result

For the attendance question:

**Question:**  
What percentage of attendance is required to be eligible for the final examination?

**Expected Answer:**  
75% attendance is required to be eligible for the final examination.

**Result:**  
The workflow contains the attendance policy stating the 75% requirement, so this is a supported knowledge-base query.

## Evaluation Summary
The evaluation demonstrates that the assistant is designed to retrieve information from the college knowledge base before 
answering. For information that is not available in the retrieved documents, the system is instructed to provide a fallback 
response instead of generating an unsupported college-specific answer.

The evaluation demonstrates that the assistant is designed to retrieve information from the college knowledge base before answering. For information that is not available in the retrieved documents, the system is instructed to provide a fallback response instead of generating an unsupported college-specific answer.The evaluation demonstrates that the assistant is designed to retrieve information from the college knowledge base before answering. For information that is not available in the retrieved documents, the system is instructed to provide a fallback response instead of generating an unsupported college-specific answer.
