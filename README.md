# kmer_mask_em

Infer [seqOutBias](https://github.com/guertinlab/seqOutBias) k-mer masks by inferring a PWM (position weight matrix) from the output of `seqOutBias count ...` via Expectation Maximization, and then masking positions based on a threshold of the information content.

# Limitations
- k-mer mask used to get initial count table from `seqOutBias` must be a palindrome
- computationally heavy, as it requires multiples runs (done in parallel) to find a good global optimum
