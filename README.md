# RAG-Bot: Document Question Answering with RAG

A beginner-friendly Retrieval-Augmented Generation (RAG) project that answers questions using information retrieved from a PDF document.

## What it does

- Extracts text from a PDF using `pypdf`.
- Splits the extracted text into overlapping chunks.
- Creates text embeddings with the Google Gemini API.
- Retrieves the top matching chunks using cosine similarity.
- Generates answers grounded in the retrieved text.
- Tests questions that are and are not answered by the document.
- Compares chunk sizes of 800 and 3000 characters.

## Technologies used

- Python
- Google Colab
- Google Gemini API (`google-genai`)
- NumPy
- pypdf
- Embeddings and cosine similarity
- Retrieval-Augmented Generation (RAG)

## Files

- `RAG_Bot.ipynb` — main Google Colab notebook.
- `requirements.txt` — Python packages used by the notebook.
- `.gitignore` — common files to keep out of version control.

## How to run

1. Open the notebook in Google Colab.
2. Upload the PDF used by the project. The notebook currently expects the file name `MRIT_Hostel_Rulebook.pdf`. If your PDF has a different name, update `pdf_path` in the notebook.
3. In Colab, open the **Secrets** panel (key icon) and add a secret named `GEMINI_API_KEYS`, matching the name used in the notebook.
4. Enable notebook access for that secret.
5. Run the notebook cells from top to bottom.

## API key safety

Do not write your actual API key directly in the notebook or README. Keep it in Colab Secrets. Before publishing, inspect notebook code and saved cell outputs to ensure no key or private information is visible.

## Notes

- The PDF is an input file and is not included in this repository. Only upload it if you have permission to share it publicly.
- Gemini API availability, model access, and usage limits may affect execution.
- The notebook's answer quality depends on the source PDF, chunk size, retrieved chunks, and model response.
