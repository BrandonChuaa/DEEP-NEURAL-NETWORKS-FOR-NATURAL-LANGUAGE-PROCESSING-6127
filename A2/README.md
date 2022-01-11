# Assignment 2
- Machine translation using sequence-to-sequence with attention

# Dataset
- http://www.statmt.org/wmt14/training-parallel-ncv9.tgz

# Question 1
- 1) Run machine translation with sequence-to-sequence with attention with the dataset, with no (https://pytorch.org/tutorials/intermediate/seq2seq_translation_tutorial.html)
- 2) Revise the function filterPairs in the section “Loading data files”
    - filterPairs: filter sentence pairs whose length is less than MAX_LENGTH and which start with eng_prefixes (e.g. “I am”, “you are”)
- 3) Randomly split a dataset into 5 subsets (S1, …, S5). Run training/testing for 5 times as follows:
    - Select Si (i=1,…,5) as test dataset and the other 4 subsets as training dataset. Train a model with the training dataset and evaluate the model against the test dataset in terms of BLEU (BLEU-1, BLEU-2, BLEU-3).
    - Report the average of the 5 BLEU scores for each dataset
- 4) Rerun machine translation with sequence-to-sequence with attention without using the filters mentioned in point 2.
    - Note that the file has 4 parallel datasets (CS-EN, DE-EN, FR-EN, RUEN). Rerun the implementations for all the 4 datasets, English as target language

# Question 2
- The Attention Decoder of Tutorial 6 is different from the attention decoder of the lecture (Sequence-to-sequence with attention). Explain the difference.
- Modify the Attention Decoder of Tutorial 6 to the attention decoder of Lecture 6. Evaluate it for Question 3 of Tutorial 6 against the 4 parallel datasets aforementioned. Compare its evaluation results with the results from Question 2.a of this assignment, and discuss why.
- Replace the dot-product attention of Question 2.b.ii of this assignment to the following attention variants:
  - Multiplicative attention
  - Additive attention
- Compare evaluation results for Question 3 of Tutorial 6 with the results from Questions 1 and 2 of this assignment, and discuss why.
