# Genetic Mutation Identification Project

This project focuses on identifying mutations using various pattern matching techniques, including Hamming distance, edit distance (Levenshtein distance), and color encodings. It explores both exact and approximate string matching techniques.

## 1. Exact String Matching Techniques

Exact string matching techniques identify specific patterns within a string without allowing any mismatches.

Example:
Parent String: ACGGCTAGCCAGGCTAGACCAGT
Substring: AGGCT

## 2. Approximate String Matching Techniques

Approximate string matching techniques allow some mismatches in the string.

Example:
Parent String: ACGGCTAGCCAGGCTAGACCAGT
Substring: TAGCAAGG

### i. Hamming Distance

Hamming distance calculates the number of substitutions needed to convert one string into another but fails to identify insertions and deletions.

Example:
Parent String: ACDJMEKNTZ
Pattern: TCDKMFKNTY

![Hamming Distance](https://user-images.githubusercontent.com/102232692/159976692-721d3582-b47e-45ce-ad8c-afc56325208c.png)

### ii. Edit Distance or Levenshtein Distance

Edit distance calculates the number of changes needed to convert one string into another, including insertions, deletions, and substitutions.

Example:
Parent String: ATCTAGCTGA
Pattern: ACGACG

![Edit Distance](https://user-images.githubusercontent.com/102232692/159977489-e1a3cc44-7899-4f60-938e-3c7ce912d9a8.png)

### Color Encodings

Color encodings assign different colors to each nucleotide (A, C, T, G) to visualize mutations in the gene. This helps identify substitutions, frame shifts, and the proximity of mutations.

![Color Encodings](https://user-images.githubusercontent.com/102232692/159977871-e86ffeb3-f82c-4719-acdb-ab61260b8d2a.png)

By analyzing color encodings, Hamming distance, and edit distance, one can determine the type and location of mutations, aiding in the understanding and diagnosis of genetic disorders.
