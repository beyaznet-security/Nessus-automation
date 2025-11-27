1. Application Production Purpose
Nessus scan results consist of large and complex datasets, making data processing challenging.

Manual cleaning of unnecessary or invalid data is labor-intensive.

Need for transitioning to a semi-automated system for reporting activities.

Requirement to properly filter and organize data.

Need to structure outputs in a more organized manner to facilitate analysis and archiving.

2. Application Workflow
Step 1: Nessus scan results are loaded as an Excel file (nessus.xlsx).

Step 2: Data in the Excel file is separated according to headers (Plugin ID, Risk, Host, Protocol, Port, Name).

Step 3: Risk levels with "None" values are filtered out, and a new Excel file (filtered_nessus.xlsx) is created with valid data.

Step 4: Using the filtered data, folders for each scan result and data.txt files containing IP and port information are created within these folders.

Step 5: Data for each vulnerability is stored systematically in the relevant folders.

3. Running the Application
First, an export in .csv format must be obtained from the Nessus application. The following items should be selected in the report section:

Plugin ID

Risk

Host

Protocol

Port

Name

Before running the application, ensure that the content of the nessus.xlsx file in the same directory contains the above data.

Before running the application, execute the command: pip install openpyxl

The application may produce errors with .csv files. The file content should be copied to an .xlsx file.

Finally, run the file via command line with: python application.py

4. Application Benefits
Organized Data Storage: Creates folders and files for each vulnerability, archiving results in a systematic manner.

Time Savings: Eliminates the need for manual processing of large datasets and provides preliminary support for reporting activities.

Error Reduction: Minimizes human error through automation.

Ease of Use: Organizing data in Excel and text file formats offers significant convenience for sharing and analysis.
