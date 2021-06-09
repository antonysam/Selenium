## Introduction
```
Apache POI -> API has collections of java libraries (open source)
```
## Uses
```
used in Data Driven Testing to read, write and manipulate different MS files such as excel sheet, power point and word files
```
## Interface Hierarchy 
```
1)Every workbook has no of sheets
2)Every sheet has no of rows
3)Every row has no of cells
```
## Type of classes implements the interfacce
```
1)xls 
   HSSFWorkbook
   HSSFSheet
   HSSFRow
   HSSFCell

2)xlsx
   XSSFWorkbook
   XSSFSheet
   XSSFRow
   XSSFCell
 ```
 ## Package
 ```
 org.apache.poi.xssf.usemodel.* 
 ```
 ## Exception 
 ```
throws IOException
```
## Snippets

## To create a source file path
```
String filepath = "sourcepath";
```
## To create a Stream
```
FileInputStream inputstream = new FileInputStream(filepath);
```
## To access the workbook class(.xlsx)
```
XSSFWorkbook workbook = new XSSFWorkbook(inputstream);
```
## Using the workbooksheet get the sheet using the method .getSheet(sheetname) or .getSheetAt(sheetindex)
```
XSSFSheet sheet = workbook.getSheet("sheet name");

XSSFSheet sheet = workbook.getSheetAt(sheet Index);
```
## Types of methods to get the data 
```
1)Using For loop
2)Using Iterator method in Sheet sheet.iterator();
```
## using for loop reading the rows and coloumns
  ##   To get the count of row and coloumns
  ```
  int rows = sheet.getLastRowNum();
  int cols = sheet.getRow(rowno).getlastCellNum();
  ```
 ## Looping the rows and cells to read the data
 ## Iterates the rows based on the row count   
 ```
  for(int r=0; r<=sheet.getLastRowNum(); r++){
	     //to get the current row
           XSSFRow row =sheet.getRow(r);		   
		
		for(int c=0; c<sheet.getRow(rowno).getlastCellNum(); c++){
		  //To get the cells
		  XSSFCell cell= row.getCell(c);
		  
		  //To get the type of the cell in excel
		  cell.getCellType()
		
		//If the excel has multiple type of data then we can use Switch case
		
		Switch(cell.getCellType())
		{
		case STRING: 
		System.out.println(cell.getStringCellValue);
		break;
		
		case NUMERIC:
		System.out.println(cell.getNumericCellValue);
		break;
		
		case BOOLEAN:
		System.out.println(cell.getBooleanCellValue());
		break;
		
		//it is used when we provide the cell which has calculated based on the formula in the excel
		case FORMULA: 
		System.out.println(cell.getNumericCellValue());
		break;
		}
```
## Iterator interface
## add the sheet to the iterator
```
Iterator iterator = sheet.iterator();

while(iterator.hasnext())
  {
    XSSFRow row = (XSSFRow)iterator.next();
	
	//Iterating the cell have a cellIterator() method
	Iterator cellIterator = row.cellIterator();
	
	while(cellIterator.hasnext())
	{
	   XSSFCell cell = (XSSFCell) cellIterator.next();
	   
	   	Switch(cell.getCellType())
		{
		case STRING: 
		System.out.println(cell.getStringCellValue);
		break;
		
		case NUMERIC:
		System.out.println(cell.getNumericCellValue);
		break;
		
		case BOOLEAN:
		System.out.println(cell.getBooleanCellValue());
		break;
		
		//it is used when we provide the cell which has calculated based on the formula in the excel
		case FORMULA: 
		System.out.println(cell.getNumericCellValue());
		break;
		}
	   
	}
  }
```



 
  
