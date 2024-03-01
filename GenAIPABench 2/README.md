# GenAIPABench: Benchmark for Generative AI-based Privacy Assistants

## Abstract
Privacy policies on websites can be complex and lengthy, making them challenging for users to understand. Privacy assistants, powered by generative AI (genAI), offer a solution by simplifying these policies. However, the reliability of genAI in delivering accurate information remains a concern. GenAIPABench is introduced as a benchmark to evaluate the effectiveness of genAI-based Privacy Assistants (GenAIPAs). It encompasses a set of privacy-related questions, metrics for evaluating responses, and a tool for generating privacy document prompts to test system robustness. The benchmark was applied to leading genAI systems—ChatGPT-4, Bard, and Bing AI—revealing significant potential, alongside challenges in managing complex queries, ensuring consistency, and verifying source accuracy.


## High-Level Overview of GenAIPABench

The included figure illustrates the workflow and components of GenAIPABench, a benchmark framework designed to evaluate Generative AI-based Privacy Assistants (GenAIPAs). The process starts with the privacy document input to the GenAIPA model. The evaluator then interacts with the model through a series of queries related to the privacy document, which could range from specific details in the privacy policy to requests for a summary of the document. The GenAIPA, represented by leading genAI systems such as ChatGPT-4, Google BARD, and Bing AI, generates responses to these queries.

The responses are then assessed using a set of defined metrics that include relevance, accuracy, clarity, completeness, and reference quality. This assessment produces a set of results that are stored and can be used for further analysis, such as summary analysis, robustness analysis, and privacy regulation analysis. The results are visualized in a matrix that scores the GenAIPA's performance on each metric for various questions, providing a clear and comprehensive overview of its capabilities and areas for improvement.
![Figure 1: A high-level overview of GenAIPABench](./arch.png)

## Citation

If you find our work useful, please cite our paper as follows:

```
@inproceedings{GenAIPABenchmark2024,
  title = {{A Benchmark for Generative AI-based Privacy Assistants}},
  author = {Hamid, Aamir and Samidi, Hemath Reddy and Finin, Tim and Pappachan, Primal and Yus, Roberto},
  booktitle = {},
  year = {2024},
}
```



## Repository Directory Structure

    └── GenAIPABench
        └──Annotated Answers
            └── Privacy Policy Answers
	             └── annotated_answers_Airbnb  	
	             └── annotated_answers_Facebook
	             └── annotated_answers_Spotify 	
	             └── annotated_answers_Twitter
	             └── annotated_answers_Uber
            └── Regulation Answers
	             └── annotated_answers_CCPA  	
	             └── annotated_answers_GDPR
        └──Generated Answers
            └── Bard
                └── Bard_FAQ
                └── Bard_user_generated
            └── BingAI
                └── BingAI_FAQ
                └── BingAI_user_generated
            └── ChatGPT-4
                └── ChatGPT-4_FAQ
                └── ChatGPT-4_user_generated
        └── Privacy Documents
            └── Privacy Policy
                └── Airbnb_document
                └── Facebook_document
                └── Spotify_document
                └── Twitter_document
                └── Uber_document
            └── Regulations
                └── CCPA_document
                └── gdpr_document
        └── Questions
            └── Privacy Questions
                 └── Questions   	
	             └── Questions (Paraphrased)  
            └── Regulation Questions 
	             └── Questions
        └──  Results
	        └── Results_Bard
	             └── Results_adaptive  	
	             └── Results_orig
                 └── Results_regulations
                 └── Results_robust
                 └── Results_summary
            └── Results_BingAI
	             └── Results_adaptive  	
	             └── Results_orig
                 └── Results_regulations
                 └── Results_robust
                 └── Results_summary
            └── Results_ChatGPT-4
                 └── Results_adaptive  	
	             └── Results_orig
                 └── Results_regulations
                 └── Results_robust
                 └── Results_summary


### Annotated Answers
- **Privacy Policy Answers**: CSV files containing annotated responses to privacy policy questions for the privacy policies gathered from Airbnb, Facebook, Uber, Spotify, and Twitter (`annotated_answers_Airbnb, annotated_answers_Facebook, annotated_answers_Spotify, annotated_answers_Twitter and annotated_answers_Uber)`).
- **Regulation Answers**: CSV files with annotated answers for the compiled GDPR and CCPA regulation questions (`annotated_answers_CCPA, annotated_answers_GDPR`).

### Generated Answers

These documents containes compilation of answers (responses) generated by GenAIPA models, including Bard, BingAI, and ChatGPT-4. The data is categorized based on the type of queries:

#### Categories of Queries

- **`FAQ`**: Responses to generalized quieries.
- **`user_generated`**: Responses to squeries based on specific individual concerns.



### Privacy Documents
Contains the text documents of gathered privacy policies of Airbnb, Facebook, Uber, Spotiy and Twitter (`Airbnb_document, Facebook_document, Spotify_document, Twitter_document and Uber_document)`) and word documents related to privacy regulations (`CCPA_document, GDPR_document`).

### Questions
#### Privacy Questions (`Privacy Questions, Privacy Questions (Paraphrased)`)
This directory houses CSV files with privacy questions meticulously curated to evaluate GenAIPAs on a wide range of privacy-related topics. These questions, anchored in the ISO/IEC 29100:2011 privacy framework, span eight categories to reflect both broad user concerns and specific individual queries. Each category includes questions labeled `f1`, `f2`, `f3` for generalized queries, and `u1` for queries based on specific individual concerns. These questions are designed to cover a spectrum of complexities, from straightforward queries to those that demand a deep dive into privacy practices and policies.

To further challenge the GenAIPAs' comprehension and response precision, the benchmark incorporates paraphrased versions of these questions. For the general queries (`f1`, `f2`, `f3`), one paraphrased variant for each is generated using AI tools to ensure diversity in phrasing while preserving the original intent. For the individual-specific query (`u1`), three manually selected paraphrased versions are provided to better simulate the variety of ways users may express similar concerns.

#### Questions on Regulations (`Regulation Questions`)
Contained within this directory are CSV files focused on privacy and data protection regulations, notably the GDPR and CCPA. A set of 12 questions, six per regulation, is provided to address key topics such as compliance obligations, penalties, definitions of personal and sensitive information, and the rights afforded to individuals under these laws. Paraphrased versions of these questions are also available to assess the GenAIPAs' ability to accurately interpret and respond to regulatory queries across different linguistic constructions.

This structured approach aims to rigorously evaluate GenAIPAs' proficiency in addressing the complex and nuanced aspects of privacy and data protection, mirroring the challenges presented by real-world scenarios of privacy concerns and regulatory compliance inquiries.

### Results
Includes data from experiments assessing the performance of GenAIPA models (Bard, BingAI, ChatGPT-4) in:
- **Adaptive Recall (`Results_adaptive`)**: Assessing the ability to recall privacy policy knowledge. 
- **Quality of Responses to Privacy Policy Questions (`Results_orig`)**: Evaluating response quality to direct and paraphrased questions.
- **Quality of Responses to Regulation Questions (`Results_regulations`)**: Analyzing responses to GDPR and CCPA questions.
- **Robustness (`Results_robust`)**: Testing response consistency to paraphrased questions.
- **Summary Quality(`Results_summary`)**: Examining the quality of privacy policy summaries.


This README provides a structured overview of the GenAIPABench repository, integrating the abstract, repository structure, and detailed explanations following the directory structure and flow.


