Data Mining Assignment 2

---------------------
Table of contents
---------------------
1. Introduction
2. Prerequisites
3. Constraints
4. Approach writeup
5. Execution
6. Output files
7. Web links


1)Introduction
---------------
-The objective of the assignment is to analyse population of "LANGUAGE SPEAKERS" information data of INDIA and its Union territories., like number of only one language speakers,exactly two language speakers, three or more language speakers,
male-female number of language speakers ratio and so on..

-This assignment also demands Datapreprocessing, DataCleaning, and so on called as Data Mining.

2)Prerequisites
-----------------
Technical : Python,Numpy,Pandas,scipy must be installed and the Linux environment to run .sh script files.
	    in LINUX BASH SHELL -- "openpyxl","xlrd","jupyter-nbconvert" are required., if not already installed.


3)Constraints
--------------

1. Data files are not pulled directly from api link as sometimes the website isn't functional.
    -   Instead downloaded files are used.
    - All the input files are provided in the folder.


4)Approach write-up
---------------------
      - This assignment demands 10 questions including the requirement of this "README" file.
      - Population(male/female/both) speaking only one language = Total population(CENSUS) - Population speaking two languages(Language files)
      - Population(male/female/both) speaking exactly two languages = Population speaking two languages(Language files) - Population speaking three languages(Language files)
      - Population(male/female/both) speaking three languages =Population speaking three languages(Language files)

Files Used 
-------------
 Q1 ->   - Files used: 1)"Census2011data.xlsx" 
		       2) C18: "DDW-C18-0000.xlsx"
        -  Total Population is taken from census file and language speakers count are taken from C18 file.

 Q2 ->   - Files used: 1)"Census2011data.xlsx" 
		       2) C18: "DDW-C18-0000.xlsx"        
           - Total Population of male and female is taken from census file and language speakers count of male and female are taken from C18 file.
           - P-value is calculated using the scipy stats' ttest_1samp.
 
 Q3 ->      - Files used: 1)"Census2011data.xlsx" 
			  2) C18: "DDW-C18-0000.xlsx" 
           - Population of urban and rural is taken from census file and language numbers of urban and rural are taken from C18 file.   
           - P-value is calculated using the scipy stats' ttest_1samp.     

 Q4a ->     - Files used: 1) C18: "DDW-C18-0000.xlsx" 
           - Output contains 6 rows displaying top-3 states (higher to lower ratio) first and then worst-3 states (lower to higher ratio) 

 Q4b ->     - Files used: 1)"Census2011data.xlsx" 
			  2) C18: "DDW-C18-0000.xlsx" 
           - Output contains 6 rows displaying top-3 states (higher to lower ratio) first and then worst-3 states (lower to higher ratio) 

 Q5 ->      - Files used: 1) C14: "DDW-0000C-14-India.xls" 
			  2) C18: "DDW-C18-0000.xlsx" 
           - C14 is used for population of different age groups. 
             C18 is used for language speakers in different age aroups.
           - Age groups in C14 are clubbed to match with agegroups of C18.

 Q6 ->      - Files used: 1) C08="DDW-0000C-08.xlsx"             (# In the Input Excel file provided, last redundant empty column is deleted)
			  2) C19="DDW-C19-0000.xlsx"
           - C8 is used for population of different literacy groups. C19 is used for language speakers in different literacy aroups.
           - Literacy groups in C8 are clubbed to match with literacy groups of C19.

 Q7 ->     - Files used: 1)C17 folder containing individual data files for each state/ut.
			  - STATES are clubbed into 6 regions - North,West,Central,East,South,North-East.
           
 Q8 ->      - Files used: 1)C14: "DDW-0000C-14-India.xls" 
			  2) C18: "DDW-C18-0000.xlsx" 
           - C14 is used for male and female population in different age groups. C18 is used for male and female language speakers in different age aroups.
           - Age groups in C14 clubbed to match with agegroups of C18.

 Q9 ->     - Files used: 1)C08="DDW-0000C-08.xlsx"               (# In the Input Excel file provided, last redundant empty column is deleted)
			 2) C19="DDW-C19-0000.xlsx"
           - C8 is used for male and female population of different literacy groups. C19 is used for male and female language speakers in different literacy aroups.
           - Literacy groups in C8 are clubbed to match with agegroups of C19.



5)How to execute
-------------------
Individual .sh files for each question are created as list below:(file names doesn't include quotations)
Q1. "percent-india.sh"
Q2. "gender-india.sh"
Q3. "geography-india.sh"
Q4. a)"3-to-2-ratio.sh"
    b)"2-to-1-ratio.sh"
Q5.  "age-india.sh"
Q6.  "literacy-india.sh"
Q7.  "region-india.sh"
Q8.  "age-gender.sh."
Q9.  "literacy-gender.sh"

Note: "assign2.sh" runs entire Assignment-2, it conisists of all above shell files execution.

6)Output Files      (TOTAL OP files =19)
---------------
Q1 -> percent-india.csv

Q2 -> gender-india-a.csv     -     (Mono language)
      gender-india-b.csv     -    (Bi language)
      gender-india-b.csv     -    (Tri language)

Q3 -> geography-india-a.csv    -      (Mono language)
      geography-india-b.csv    -     (Bi language)
      geography-india-b.csv    -     (Tri language)

Q4 -> a)3-to-2-ratio.csv 
      b)2-to-1-ratio.csv

Q5 -> age-india.csv

Q6 -> literacy-india.csv

Q7 -> region-india-a.csv   -       (MOTHER TONGUE SPEAKERS)
      region-india-b.csv   -      (MOTHER TONGUE + Bilanguage +Trilanguage)

Q8 -> age-gender-a.csv   -         (Tri language)
      age-gender-b.csv   -        (Bi language)
      age-gender-c.csv   -          (Mono language)

Q9 -> literacy-gender-a.csv -      (Tri language)
      literacy-gender-b.csv -      (Bi language)
      literacy-gender-c.csv -      (Mono language)


[Note-- All the input files are provided in the folder only]


7)Web Links
-------------
LANGUAGE DATA --> : https://censusindia.gov.in/2011Census/Language_MTs.html
CENSUS DATA: http://censusindia.gov.in/pca/DDW_PCA0000_2011_Indiastatedist.xlsx

INDIVIDUALFILES
---------------
C08: https://censusindia.gov.in/2011census/C-series/C-08/DDW-0000C-08.xlsx     
C14: https://censusindia.gov.in/2011census/C-series/c-14/DDW-0000C-14.xls
C16: https://censusindia.gov.in/2011census/C-16/DDW-C16-STMT-MDDS-0000.XLSX
C17: https://censusindia.gov.in/2011census/C-17.html
C18: https://censusindia.gov.in/2011Census/Language-2011/DDW-C18-0000.xlsx
C19: https://censusindia.gov.in/2011Census/Language-2011/DDW-C19-0000.xlsx

