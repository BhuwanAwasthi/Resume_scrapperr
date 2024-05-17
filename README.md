## Resume Scraper Project

### Description
This project is a web application that allows users to upload resumes in PDF and DOCX formats. The application extracts email addresses and phone numbers from these resumes, processes the extracted data, and provides an option to download the results in an Excel file. Additionally, users can clear uploaded and output files through a designated route.

### Features
1. **Multi-format Support**:
   - Extracts text from PDF and DOCX files.
   
2. **Data Extraction**:
   - Extracts email addresses and phone numbers from resume text.
   - Cleans and validates extracted email addresses and phone numbers.
   
3. **File Upload**:
   - Users can upload multiple resume files at once through a user-friendly web interface.
   
4. **Data Output**:
   - Processes and outputs the extracted data into an Excel file for easy download.
   
5. **File Management**:
   - Provides a route to clear uploaded files and output data to manage storage space.

6. **Web Interface**:
   - Simple and intuitive web interface for uploading resumes built with Bootstrap for responsive design.

### How to Use
1. **Upload Page**:
   - Access the upload page at the root URL (`/`).
   - Use the provided form to select and upload multiple resume files.
   
2. **Process Files**:
   - The application processes the uploaded files to extract text, emails, and phone numbers.
   - Extracted data is saved into an Excel file and made available for download.
   
3. **Download Results**:
   - After processing, the application returns a link to download the resulting Excel file containing the extracted information.
   
4. **Clear Data**:
   - Navigate to `/clear` to delete all uploaded and output files, freeing up storage space.

### Running the Application
1. **Setup Environment**:
   - Ensure Python and required dependencies are installed.
   - Create the necessary directories (`uploads` and `output`) or let the application create them on first run.
   
2. **Install Dependencies**:
   ```bash
   pip install flask pdfplumber python-docx pandas
   ```
   
3. **Run the Application**:
   ```bash
   python app.py
   ```
   - The application will start on the default port 5000 or on a port specified in the environment variable `PORT`.

### File Structure
- **app.py**: The main application file containing all the routes and core functionality.
- **templates/upload.html**: HTML template for the file upload interface.
- **uploads/**: Directory where uploaded files are temporarily stored.
- **output/**: Directory where the output Excel file is saved.

### Sample Usage
- Visit `http://localhost:5000` to access the upload page.
- Select and upload resume files.
- After processing, download the resulting Excel file containing extracted emails and phone numbers.
- Optionally clear uploaded and output files by navigating to `http://localhost:5000/clear`.

### Additional Notes
- Make sure to handle different resume formats consistently to ensure reliable data extraction.
- Validate the formats of extracted emails and phone numbers before including them in the final output.
- Ensure the application is secure and can handle potential edge cases, such as large file uploads or invalid file formats.

Deployment: https://resume-scrapperr-1.onrender.com/ 
