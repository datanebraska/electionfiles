# electionfiles

Repository contains the input files, output files, database, and SSIS package used to generate appended data files from multiple worksheets within single excel spreadsheets.

Problem: Nebraska SOS provided by Precinct files, however results were seperated within single xls spreadsheet w/ Counties seperated on each tab/worksheet.  
Solution: Needed method to programatically append each tab into a single output file

NOTE:  Output files are in tab delimited format.

NOTE #2: TabName column should represent the name of the County the precinct belongs to.



1.  *.xls files sourced from Nebraska Secretary of State
     https://electionresults.nebraska.gov/

2.  Folder /ElectionCleaner/ contains the SQL Server SSIS package used to generate the appended output files

3.  Output_*.txt files contain appended tabs from original Precinct xls files.

4.  ElectionCleanup.bak file is a backup of the SQL Server database that contains tables and stored procedures used to append the data. DB was created in SQL Server 2019
