# flaskfilerenamerv1
filerenamerflask
This script sets up a Flask web server that provides an endpoint /upload for uploading files. When a file is uploaded to this endpoint, the server extracts text from the file, generates a concise descriptive filename based on the content of the file using OpenAI's GPT-3.5 model, and returns the file with the new filename for download.

Here's a breakdown of what the script does:

Imports necessary modules including Flask, PDFPlumber (for PDF text extraction), OpenAI (for GPT-3.5 interaction), and Pandas (for handling Excel and CSV files).
Sets up a Flask application and enables Cross-Origin Resource Sharing (CORS) for requests from https://fileconvertify.com.
Defines a route /upload that handles POST requests for uploading files.
Within the upload_file function:
Retrieves the uploaded file from the request.
Saves the uploaded file temporarily.
Determines the file type based on its extension (PDF, DOCX, CSV, XLSX).
Extracts text from the file.
Calls the OpenAI API to generate a concise descriptive filename based on the extracted text.
Renames the temporary file with the new filename.
Responds with the new filename and a download URL.
