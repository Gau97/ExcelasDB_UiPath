# ExcelasDB_UiPath
1)Install UiPath.Database.Activities
2)Sequence -> Rename -> Annotation -> Connect to Start
Name : Excel as DB
Annotation : In this Sequence we will use excel as Database
3)Connect Activity
4) Configuration of Excel Connection
Click Configure Connection
In the Configuration wizard, Connection wizard
Select "Other" -> Data Provider : '.Net Framework Data Provider for ODBC'
Hit Okay
Use Connection String -> Build -> Machine Data Source
New -> User Data Source -> Microsoft Excel Driver -> Next
-> Data Source Name : EXCELRPA -> Select Workbook(Select the Input Excel File)
-> For Data manipulations uncheck Read only (Update/Delete/Insert)
Test Connection

Drop Down : System.Data.ODBC

Or USE the connection String as
"Provider=Microsoft.ACE.OleDb.12.0;Data Source='"+str_FilePath+"';Extended Properties='Excel 12.0 XML;HDR=YES';"
Provider as
"System.Data.OleDB"