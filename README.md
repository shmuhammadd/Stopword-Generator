---

# Stopword Generator

Creating stopwords from a single dataset can often be misleading, as it may cause domain-specific words to appear more frequently than they would in general language use. For instance, if you solely rely on the Bible for generating stopwords, words like "God" might appear frequently, even though they aren't considered generic stopwords in everyday language.

Recognizing this challenge, our script is designed to work with multiple datasets from varied domains, such as religion, news, literature, and more. It first identifies the stopwords specific to each domain and then pinpoints the overlapping words among them. By leveraging datasets from diverse domains, our approach ensures a robust and comprehensive set of stopwords, less biased by domain-specific terms.

In essence, this method offers a more holistic view of language, capturing the stopwords that are truly representative of the language without being overly influenced by the specificities of any single domain.


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
