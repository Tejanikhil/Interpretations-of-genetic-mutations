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
Parent string = ACGGCTAGCCAGGCTAGACCAGT
substring = TAGCAAGG
As we can see here the substring is not present in the parent string but if we change the nucleotide A at index 4 in substring to C then it exactly match with the parent string. So, we say that the substring matches with the parent string with a distance of 1 nucleotide. This is acheived using the approximate string matching techniques. 
There are two different types of approximate string matching techniques
### 1. Hamming distance: 
Hamming distance is a type of approximate string matching technique that is used to find the number of substitutions to be made to a string in order to convert into a exact matched string. Hamming distance calculated the number of substitution made in the string but it fails to identify the insertions and deletions.
Consider two strings 
Parent string = ACDJMEKNTZ
Pattern       = TCDKMFKNTY
The hamming distance between the two strings can be calculated as follows

![image](https://user-images.githubusercontent.com/102232692/159976692-721d3582-b47e-45ce-ad8c-afc56325208c.png)

### 2. Edit distance or Leveinshtein distance: 
