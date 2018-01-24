# assignment-1
PDSB

## Get the files
Q1. Download the following data files from the internet using the curl command: http://eaton-lab.org/pdsb/test.fastq.gz and http://eaton-lab.org/pdsb/iris-data-dirty.csv. Use the less or zless commands to look at the files. Then use the head command to print the first 5 lines from each file as output.
A1. Get the file from the internet using curl (with -O to suppress the output from the screen). 
Sources:
- for curl syntax: https://www.thegeekstuff.com/2012/07/wget-curl 

Code block:
```bash
> curl -O http://eaton-lab.org/pdsb/test.fastq.gz
> zless test.fastq.gz
> gunzip test.fastq.gz
> head -5 test.fastq
```
Output:
```bash
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  220k  100  220k    0     0  1572k      0 --:--:-- --:--:-- --:--:-- 1760k

@29154_superba.1 GRC13_0027_FC:4:1:12560:1179 length=74
TGCAGGAAGGAGATTTTCGNACGTAGTGNNNNNNNNNNNNNNGCCNTGGATNNANNNGTGTGCGTGAAGAANAN
+29154_superba.1 GRC13_0027_FC:4:1:12560:1179 length=74
IIIIIIIGIIIIIIFFFFF#EEFE<?################################################
@29154_superba.2 GRC13_0027_FC:4:1:15976:1183 length=74
```

Code block:
```bash
curl -O http://eaton-lab.org/pdsb/iris-data-dirty.csv
zless iris-data-dirty.csv
head -5 iris-data-dirty.csv
```
Output:
```bash
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  4549  100  4549    0     0   143k      0 --:--:-- --:--:-- --:--:--  296k

5.1,3.5,1.4,0.2,Iris-setosa
4.9,3.0,1.4,0.2,Iris-setosa
4.7,3.2,1.3,0.2,Iris-setosa
4.6,3.1,1.5,0.2,Iris-setosa
5.0,3.6,1.4,0.2,Iris-setosa
```


## Clean the data
Q1. Use grep, uniq, sed. Check that all of the species names are spelled correctly in the file iris-data-dirty.csv. Also check for missing values stored as NA. Create a new file where mispelled names are replaced with the correct values, and lines with NA are excluded, and save it as iris-data-clean.csv. Use cut, sort and uniq to list the number of data values there are for each species in the new cleaned data file.
A1.
Sources
Code block
Code block - copied answer

## Summarize sequence data file
Q1. Find how many lines in the data file test.fastq.gz start with "TGCAG" and end with "GAG"
A1.
Sources
Code block
Code block - copied answer

## Summarize sequence data file
Q1. Write a for-loop to separate the reads from the file test.fastq.gz based on the taxon name in the label, and write the reads to separately named files in the new directory called sorted_reads/. The answer to this question will require more than a single line. See the lecture materials about using variables in for-loops. This will also be tricky because each read in the data file spans four lines (this is a standard genetic sequence file format), so for each read that you correctly identify you must grab the line with the sequence data below it, as well as the repeat label after that, and the quality information line after that. For a hint, see additional options for the grep command that can be used to select multiple lines.
A1.
Sources
Code block
Code block - copied answer
