# Resume Matcher

**Resume Matcher** is a web-based application built using Flask that compares job descriptions with multiple resumes to find the most relevant matches. The system uses the **TF-IDF (Term Frequency-Inverse Document Frequency)** method for vectorization and **cosine similarity** to calculate the similarity scores between the job description and each uploaded resume.

## Key Features:
- **Upload multiple resumes**: Supports `.pdf`, `.docx`, and `.txt` resume formats.
- **Job description input**: Users can enter or paste the job description to which the resumes will be compared.
- **Similarity score**: Uses **cosine similarity** to measure how closely each resume matches the job description.
- **Top Matches**: Displays the top 5 matching resumes with their respective similarity scores.

## Technologies Used:
- **Backend**: Flask (Python)
- **Frontend**: HTML, Bootstrap (for responsive design)
- **NLP Processing**: TF-IDF vectorization using `scikit-learn` and cosine similarity to measure textual similarity
- **File Handling**: `docx2txt` for `.docx` files, `PyPDF2` for `.pdf` files

## How It Works:
1. The user inputs the job description in a text area.
2. The user uploads multiple resume files.
3. The application processes each resume, extracts text, and vectorizes both the job description and resumes using TF-IDF.
4. Cosine similarity scores are calculated for each resume in relation to the job description.
5. The top 5 resumes with the highest similarity scores are displayed as output.

## Setup Instructions:
1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/resumematcher.git
    ```
2. Navigate to the project directory:
    ```bash
    cd resumematcher
    ```
3. Create a virtual environment and activate it:
    ```bash
    python -m venv venv
    ```
    - **Windows**: `venv\Scripts\activate`
    - **macOS/Linux**: `source venv/bin/activate`
4. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```
5. Run the Flask app:
    ```bash
    flask run
    ```
6. Open a browser and go to `http://127.0.0.1:5000/`.

## Future Enhancements:
- Add support for additional file formats.
- Improve UI/UX with more detailed result visualizations.
- Implement user authentication and resume history.

---

