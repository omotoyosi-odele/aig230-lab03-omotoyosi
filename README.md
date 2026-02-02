
# AIG 230 – Lab 03
## Text Representation and Statistical Language Models

### Overview
This lab covers text feature extraction and statistical language modeling.

Working with:
- Bag-of-Words and TF-IDF
- Text similarity and classification
- Unigram, bigram, and trigram language models
- Perplexity-based evaluation

---
An analysis of 34 domain sentences (the corpus) using different out-of-vocabulary (OOV) thresholds (min_count) to determine the change in perplexity for unigram, bigram and trigram models.

Perplexity reduces slightly when min_count goes from 2 (2.354, 2.471, 2.640) to 3 (2.188, 2.219, 2.297), with the lowest being for unigram for both min_count. However, for min_count = 1, perplexity blows up to (226.259, 148.323, 147.143) and the lowest being for trigram, in this case.

This is because min_count = 3 has a smaller, but more robust vocabulary that reduces data sparsity for the frequent words, leading to better generalization. min_count = 2 strikes a balance by filtering out very rare words, but keeps more than min_count = 2. With min_count = 1, all the words that appear at least once make it into the vocabulary, causing it to be very large and sparse. This makes the model struggle to make meaningful predictions and gives a very high perplexity score.

I also defined a backoff function to recursively find the probability of an n-gram by falling back to (n-1)-grams if the current n-gram is unseen. This process continues until the unigram probability is reached. And then, the evaluate_perplexity_backoff function will use the new probability calculation to determine the perplexity.

---
