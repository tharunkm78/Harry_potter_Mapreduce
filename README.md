# Harry Potter MapReduce Project

This project implements **MapReduce in Python** using **Google Colab** to analyze the Harry Potter books.

The project has two main tasks:

1. **Regular Word Count**  
   - Count all words in selected pages of the Harry Potter PDF.  
   - Uses a **MapReduce-style workflow**:
     - **Mapper**: splits text into `(word, 1)` pairs  
     - **Reducer**: sums the counts for each word  

2. **Non-English Word Count**  
   - Counts words that are **not in the English dictionary** (names, spells, places, etc.)  
   - Also uses MapReduce style with `(word, 1)` pairs.

---

## Files

- `harrypotter_mapreduce.ipynb` → Google Colab notebook with all code  
- `file1.txt` → Extracted pages for regular word count  
- `file2.txt` → Extracted pages for non-English word count  
- `README.md` → This file  

---

## Features

- Extracts specific pages from a PDF based on user input (birthdate, birth year).  
- Performs **MapReduce-style analysis** for both tasks.  
- Saves results to **CSV** or **Excel** files for easy viewing.  
- Demonstrates **map → shuffle → reduce workflow** even in single-machine Python.

---

## How to Run

1. Open `harrypotter_mapreduce.ipynb` in **Google Colab**.  
2. Make sure the PDF file (`harrypotter.pdf`) is in the same folder or uploaded to Colab.  
3. Run all cells in the notebook.  
4. Outputs will include:
   - Word counts for the first text file (all words).  
   - Non-English word counts for the second text file.  
   - Optional CSV or Excel files with results.

---

## Requirements

- Python 3.x  
- Libraries: `PyPDF2`, `pandas`, `spellchecker`  
- Install missing libraries in Colab using:

```python
!pip install PyPDF2 pandas pyspellchecker openpyxl
