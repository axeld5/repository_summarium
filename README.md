---
title: repository_summarium
app_file: app.py
sdk: gradio
sdk_version: 5.16.0
---
# Overview

This repo allows to generate summaries of code architecture from local folders or other github repository. 

# Project Setup & Usage

## Prerequisites
Before running this project, ensure you have the following:
- A **Mistral API Key**, stored in a `.env` file at the root of the repository.
- All required dependencies installed. You can install them using:
  ```bash
  pip install -r requirements.txt
  ```

## Running the File Summary
To generate file summaries, run the following command:
```bash
python main.py --mode <local|repo> --path_or_url <folder_path|github_url>
```
- `--mode local`  → Use this when summarizing files from a local folder.
- `--mode repo`   → Use this when summarizing files from a GitHub repository.
- `--path_or_url` → Provide the local folder path or GitHub URL accordingly.

## Viewing Summaries in a Readable Format
To display the summaries in a user-friendly format, launch the Gradio interface using:
```bash
python app.py --gradio
```
This will start a Gradio web interface for easy viewing of file summaries.

---

For any issues or contributions, feel free to open an issue or submit a pull request!

## Repository Summary (Generated by this code)

The repository contains scripts and tools for summarizing the contents of a local folder or a GitHub repository. The key components include:

1. **`app.py`**: Provides a Gradio-based interface for loading and viewing saved summaries and summary trees. It includes functions to list and load saved summaries, and to interact with summary trees.

2. **`main.py`**: The main script that processes and summarizes a local folder or a GitHub repository. It handles command-line arguments, clones repositories, builds folder trees, generates summaries, and saves the results.

3. **`README.md`**: Instructions for running the repository, including requirements and command-line arguments for executing summarizations and viewing them using Gradio.

4. **`requirements.txt`**: Lists the dependencies needed to run the repository.

5. **Subfolder `example_repos`**: Contains saved summary files in both text and JSON formats.

6. **Subfolder `functions`**: Contains multiple Python scripts for various functionalities:
   - **`files_exclusion.py`**: Defines exclusion rules and handles `.gitignore` patterns.
   - **`folder_summarization.py`**: Generates summaries for folders.
   - **`folder_tree.py`**: Builds and flattens the folder tree structure.
   - **`genai_summary.py`**: Generates summaries using the Mistral AI API.
   - **`process_file.py`**: Reads and processes file content for summarization.
   - **`utils.py`**: Provides utility functions for cloning repositories and summarizing them.
   - **`__init__.py`**: Indicates the directory is a Python package.

The repository is designed to clone a GitHub repository, build a folder tree while applying exclusion rules, process file contents, generate summaries using an AI model, and save the results for further use.