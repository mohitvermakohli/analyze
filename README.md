# Project Overview

This repository demonstrates a simple data processing workflow using Python, Pandas, and GitHub Actions. It takes an Excel file (`data.xlsx`), converts it to a CSV (`data.csv`), processes the CSV using a Python script (`execute.py`), and publishes the results as a JSON file (`result.json`) via GitHub Pages.

## Project Structure

*   `.github/workflows/ci.yml`: GitHub Actions workflow for continuous integration and deployment.
*   `data.xlsx`: The original Excel data file (not directly committed, but converted to `data.csv`).
*   `data.csv`: The converted CSV file, used as input for `execute.py`.
*   `execute.py`: A Python script that processes `data.csv` and outputs structured JSON.
*   `index.html`: A simple web page providing an overview of this project.
*   `LICENSE`: The MIT License for this project.
*   `README.md`: This file.

## Getting Started

### Prerequisites

*   Python 3.11+
*   Pandas 2.3+
*   Ruff (for linting)

### Local Setup

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/your-repo-name.git
    cd your-repo-name
    ```
2.  **Install dependencies:**
    ```bash
    pip install pandas ruff
    ```
3.  **Run the processing script:**
    ```bash
    python execute.py > result.json
    ```
    This will generate `result.json` in your local directory.

### Running Tests and Linting

To ensure code quality, you can run `ruff` locally:

```bash
ruff check .
```

## Continuous Integration and Deployment (CI/CD)

A GitHub Actions workflow (`.github/workflows/ci.yml`) is configured to automatically:

1.  **Lint Code**: Run `ruff` to check for code style and errors.
2.  **Execute Script**: Run `python execute.py` to process `data.csv` and generate `result.json`.
3.  **Publish Results**: Deploy `result.json` to GitHub Pages.

### Accessing Results

After a successful push to the `main` branch, the `result.json` file will be published and accessible via GitHub Pages. You can typically find it at a URL similar to:

`https://<YOUR_USERNAME>.github.io/<YOUR_REPOSITORY_NAME>/result.json`

(Replace `<YOUR_USERNAME>` and `<YOUR_REPOSITORY_NAME>` with your actual GitHub details.)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
