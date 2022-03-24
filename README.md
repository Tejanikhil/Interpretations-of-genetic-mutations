This project is about mutation identification using different pattern matching techniques like hamming distance, edit distance(Leveinshtein distance) and color encodings. Generally there are two different types of string matching techniques which are exact and approximate string matching.

## 1. Exact String matching techniques: 
As the name says that these techniques are used to find a particular pattern present in the string. Using the exact string matching techniques one can find a sub-string present in a parent string. These techniques will not allow any mismatches like as shown below: 
Let, <br />
Parent String = ACGGCTAGCCAGGCTAGACCAGT
substring = AGGCT
If we want find out the position of substring prenet in the parent string or if we want to check whether the substring is present in the parent string or not.

## 2. Approximate string matching technique: 
As the name says that these techniques are used to find the string present inside the parent string allowing some mistakes. These techniques allows certain number of mismatches in the string like as show below: 
Let, <br />
Parent string = ACGGCTAGCCAGGCTAGACCAGT <br />
substring = TAGCAAGG <br />
As we can see here the substring is not present in the parent string but if we change the nucleotide A at index 4 in substring to C then it exactly match with the parent string. So, we say that the substring matches with the parent string with a distance of 1 nucleotide. This is acheived using the approximate string matching techniques. <br />
There are two different types of approximate string matching techniques
### 1. Hamming distance: 
Hamming distance is a type of approximate string matching technique that is used to find the number of substitutions to be made to a string in order to convert into a exact matched string. Hamming distance calculated the number of substitution made in the string but it fails to identify the insertions and deletions.
Consider two strings <br />
Parent string = ACDJMEKNTZ <br />
Pattern       = TCDKMFKNTY <br />
The hamming distance between the two strings can be calculated as follows

![image](https://user-images.githubusercontent.com/102232692/159976692-721d3582-b47e-45ce-ad8c-afc56325208c.png)

### 2. Edit distance or Leveinshtein distance: 
Edit distance also known as Leveinshtein distance as name says that it is the number of changes/edits to be made to a string inorder to convert into a required string. Unlike hamming distance edit distance is used to also to calculate the number of insertion, deletions and substitutions. The Edit distance can be calculated using a matrix called as DP matrix. <br />
Consider two strings <br />
Parent String = ATCTAGCTGA <br />
pattern       = ACGACG <br />

![image](https://user-images.githubusercontent.com/102232692/159977489-e1a3cc44-7899-4f60-938e-3c7ce912d9a8.png)

From the above figure the last element in the matrix represents the edit distance which means that 5 edits(may include insertions and deletions) has to be done to the pattern to convert it into parent string. <br />

### Color Encodings: 
Before analyzing the mutated gene with the approximate string-matching techniques, it is required to find whether the mutations in the gene is substitutions or a frameshift and whether the mutations are wide apart or occurred consecutively. Color encodings helps in completing this task by assigning different colors to each of the nucleotide and converting the nucleotide sequence into an image. In this method each nucleotide Adenine(A), Cytosine(C), Thymine(T), Guanine(G) is assigned with different colors like Adenine as blue, cytosine as red, Guanine as green and Thymine as yellow

![image](https://user-images.githubusercontent.com/102232692/159977871-e86ffeb3-f82c-4719-acdb-ab61260b8d2a.png)

Using the binary operation between the reference and mutated gene one can find out the index position of mutations visually. If the mutations at a point suddenly increases means that there must be a frame shift mutation.

### Linking Color encodings, hamming distance, edit distance
Observing the color encodings one can conclude whether the mutations are substitution or frame shift mutations. If the observed mutations are substitutions throughout the genome, then using the concept of hamming distance the positions of substitutions are extracted and followed by identifying them as missense/nonsense/silence mutations by encoding them into proteins. If the observed mutations are frame shift mutations, then using the concept of leveinshtein distance (edit distance) the number of insertions, deletions, substitutions are calculated.
