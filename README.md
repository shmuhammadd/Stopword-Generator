---

# Stopword Generator

This script calculates the most frequent words (stopwords) from multiple files and saves the overlapping stopwords among these files. This is useful in cases where you want to find common stopwords across various datasets.

## Requirements:

- Python 3.x

## How to Run:

1. **Clone the repository**:

   ```bash
   git clone [repository-url]
   cd [repository-directory]
   ```

2. **Execute the script** by passing file or directory names as arguments:

   ```bash
   python stopword_generator.py file1.txt dir1/ file2.txt
   ```

   - You can pass any number of files and/or directories as arguments.
   - For directories, the script will recursively process all files within.

3. **Check the Results**:

   The resulting overlapping stopwords will be saved in `data/generated_stopwords.txt`.

## Script Details:

- The script starts by accepting file and directory names from the command-line arguments.
- For each valid file, it:
  
  ```python
  tokenizes the text, calculates word frequencies, and identifies the top num_stopwords (default is 100).
  ```

- For each directory, it:

  ```python
  recursively finds all files and processes them in the same way.
  ```

- After processing all files, it identifies the overlapping stopwords among all the lists.
- These overlapping stopwords are then saved to `data/generated_stopwords.txt`.

## Notes:

- Ensure that the `data` directory exists in the same location as the script before running, as the output file `generated_stopwords.txt` will be saved there.
- Words are tokenized based on alphanumeric sequences, so punctuation is ignored.

---
