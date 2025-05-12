# AffineGapAlignment

# Description
AffineGapAlignment is a Python implementation of the global alignment algorithm with affine gap penalties, commonly used in bioinformatics to align two DNA, RNA, or protein sequences in a biologically realistic way.

The algorithm uses three dynamic programming matrices to track different alignment states (gap in one sequence, match/mismatch, and transitions between them), allowing distinct penalties for gap opening and extension. This better models real biological events such as insertions and deletions.

# Features
* Performs global sequence alignment using affine gap penalties.
* Distinguishes between gap opening and gap extension penalties.
* Returns the alignment score and the aligned sequences.
* Pure Python implementation, no external dependencies.
* Suitable for education, experimentation, and small-scale sequence analysis.

# Function
affine_gap_alignment(match_reward, mismatch_penalty, gap_opening_penalty, gap_extension_penalty, v, w)
Purpose:
Computes the optimal global alignment of two sequences using affine penalties for gap opening and extension.

# Parameters:
* match_reward (int): Score for a match between characters.
* mismatch_penalty (int): Penalty for a mismatch.
* gap_opening_penalty (int): Penalty for starting a new gap.
* gap_extension_penalty (int): Penalty for extending an existing gap.
* v (str): First input sequence.
* w (str): Second input sequence.

# Returns:
```
alignment_score (int): The final alignment score.
aligned_v (str): The aligned version of the first sequence, including gaps.
aligned_w (str): The aligned version of the second sequence, including gaps.
```

# Example

```
match_reward = 1
mismatch_penalty = 5
gap_opening_penalty = 3
gap_extension_penalty = 1

v = "AGGTGGATCCTGTTGACGGTGCACCTGGTATTGCATGTGGATTGCACTTAAGCTCGTATCCGCCACAAGCACAACCCTCGTTGTCACGTG"
w = "AGGTGGATCCGATTGGCCTGGCAATCCTCATGTGGAGAACATTGCGCGCCTTATGCTTGTATCCGCACCCCAGATGTCACGTG"

alignment_score, aligned_v, aligned_w = affine_gap_alignment(
    match_reward, mismatch_penalty, gap_opening_penalty, gap_extension_penalty, v, w)

print(alignment_score)
print(aligned_v)
print(aligned_w)
```
# Output

-15
AGGTGGATCCTG-TTGACGGTGCACCTGG--TAT--TGCATGT-G-G---ATT----GCACTTAAGCTCGTATCCGCCACAAGCACAACCCTC-GTTGTCACGTG
AGGTGGATCC-GATT----G-G--CCTGGCA-ATCCT-CATGTGGAGAACATTGCGCGC-CTTATGCTTGTAT----C-C--G--C-ACCC-CAGATGTCACGTG

# Applications
* Comparative Genomics: Comparing gene or genome sequences between species.
* Protein Sequence Analysis: Evaluating functional similarity of proteins.
* Bioinformatics Education: Teaching alignment algorithms in classrooms and labs.

Requirements
*  Python 3.x
* No external libraries required

#  License
*  This project is licensed under the MIT License. See the LICENSE file for details.





