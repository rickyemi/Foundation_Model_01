# Foundation Model: Large Language Model For PubMed Abstract Categorization

<center><p float="center">
  <img src="https://healthjournalism.org/wp-content/uploads/2020/09/PubMed-300x265-1.png" width=650/>
</p></center>

## Problem Statement

### Business Context
- PubMed® comprises more than 36 million citations for biomedical literature from MEDLINE, life science journals, and online books. Citations may include links to full text content from PubMed Central and publisher websites. As of 23 May 2023, PubMed has more than 35 million citations and abstracts dating back to 1966, selectively to the year 1865, and very selectively to 1809. As of the same date, 24.6 million of PubMed's records are listed with their abstracts, and 26.8 million records have links to full-text versions (of which 10.9 million articles are available, full-text for free).[8] Over the last 10 years (ending 31 December 2019), an average of nearly one million new records were added each year.
### Problem Definition
-PubMed has been reported to include some articles published in predatory journals. MEDLINE and PubMed policies for the selection of journals for database inclusion are slightly different. Weaknesses in the criteria and procedures for indexing journals in PubMed Central may allow publications from predatory journals to leak into PubMed. 
- Despite the abundance of scientific articles available on PubMed, scientists often face challenges deriving key insights from these various data sources - primarily due to the huge volume of text data tends to be compute constraints.
### Objective
- To identify and extract subjective information from 3 medical article categories namely `Cancer Genomics`, `Covid` and `Diabetes`, and help the scientific community tag each article based on the domain terminologies.
### Data Source
 -  Abstracts were harvested from PubMed and stored in a xlsx format

### IDE
- google colab T4 GPU

### Code 

- `PubMed_Abstract_Categorization.ipynb` and `PubMed_Abstract_Categorization.py`

### Concepts Applied:
-LLaMA foundation model
- Prompt Engineering
  - A prompt contains any of the following elements:

        -  **Instruction** - a specific task or instruction you want the model to perform

        - **Context** - external information or additional context that can steer the model to better responses

        -  **Input Data **- the input or question that we are interested to find a response for

        -  **Output Indicator** - the type or format of the output.

#### Optimization Parameters 

    **max_tokens**: specifies the maximum number of tokens the model should generate in response to the prompt.

     **temperature**: controls the randomness of the generated response. A higher temperature value will result in a more random response, while a lower temperature value will result in a more predictable response.

     **top_p:** This parameter controls the diversity of the generated response by establishing a cumulative probability cutoff for token selection. A higher value of top_p will result in a more diverse response, while a lower value will result in a less diverse response.

    **top_k**: This parameter controls the maximum number of most-likely next tokens to consider when generating the response at each step.

    **repeat_penalty**: This parameter controls the penalty for repeating tokens in the generated response. A higher value of repeat_penalty will result in a lower probability of repeating tokens, while a lower value will result in a higher probability of repeating tokens.
