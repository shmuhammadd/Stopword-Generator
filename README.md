# Stopword-Generator


This script calculates the most frequent words (stopwords) from multiple files and saves the overlapping stopwords among these files. This is useful in cases where you want to find common stopwords across various datasets.

Requirements:

Python 3.x
How to Run:

Clone the repository:
bash
Copy code
git clone [repository-url]
cd [repository-directory]
Execute the script by passing file or directory names as arguments:
Copy code
python stopword_generator.py file1.txt dir1/ file2.txt
You can pass any number of files and/or directories as arguments.
For directories, the script will recursively process all files within.
The resulting overlapping stopwords will be saved in data/generated_stopwords.txt.
Script Information:

The script starts by accepting file and directory names from the command-line arguments.
For each valid file, it tokenizes the text, calculates word frequencies, and identifies the top num_stopwords (default is 100).
For each directory, it recursively finds all files and processes them in the same way.
After processing all files, it identifies the overlapping stopwords among all the lists.
These overlapping stopwords are then saved to data/generated_stopwords.txt.
Notes:

Ensure that the data directory exists in the same location as the script before running, as the output file generated_stopwords.txt will be saved there.
The default number of stopwords extracted from each file is 100. To change this, modify the num_stopwords parameter in the generate_stopwords function.
Words are tokenized based on alphanumeric sequences, so punctuation is ignored.
