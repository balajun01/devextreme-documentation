---
##### shortDescription
Sets several options of a column at once.

##### param(id): Number|String
The name, index, data field,or  caption of a column.

##### param(options): Object
The required configuration options.

---
Using this method, you can set several options of a specific column from code. This method accepts one of the following as the first parameter.

* **Name**		
The [unique name](/api-reference/10%20UI%20Widgets/dxDataGrid/1%20Configuration/columns/name.md '/Documentation/ApiReference/UI_Widgets/dxDataGrid/Configuration/columns/#name') of the column.

* **Column Index**		
The index of the column in the [columns](/api-reference/10%20UI%20Widgets/dxDataGrid/1%20Configuration/columns '/Documentation/ApiReference/UI_Widgets/dxDataGrid/Configuration/columns/') array.

* **Data Field**		
The name of the [data source field](/api-reference/10%20UI%20Widgets/dxDataGrid/1%20Configuration/columns/dataField.md '/Documentation/ApiReference/UI_Widgets/dxDataGrid/Configuration/columns/#dataField') assigned to the column.

* **Caption**		
The text displayed in the column header.

* **Service String**  
One of the following values:
 - *"command:edit"*    
    Gets the [edit column](/concepts/05%20Widgets/DataGrid/001%20Visual%20Elements/010%20Grid%20Columns/070%20Command%20Columns.md '/Documentation/Guide/Widgets/DataGrid/Visual_Elements/#Grid_Columns/Command_Columns').

 - *"command:select"*    
    Gets the [select column](/concepts/05%20Widgets/DataGrid/001%20Visual%20Elements/010%20Grid%20Columns/070%20Command%20Columns.md '/Documentation/Guide/Widgets/DataGrid/Visual_Elements/#Grid_Columns/Command_Columns').  

 - *"command:adaptive"*  
    Gets the [adaptive column](/concepts/05%20Widgets/DataGrid/001%20Visual%20Elements/010%20Grid%20Columns/070%20Command%20Columns.md '/Documentation/Guide/Widgets/DataGrid/Visual_Elements/#Grid_Columns/Command_Columns').  
 
 - Any string matching the following format: *"optionName:value"*  
    Here, the *optionName* is one of the [column options](/api-reference/10%20UI%20Widgets/dxDataGrid/1%20Configuration/columns '/Documentation/ApiReference/UI_Widgets/dxDataGrid/Configuration/columns/').

    [note]In command columns, you can change only the [width](/api-reference/10%20UI%20Widgets/dxDataGrid/1%20Configuration/columns/width.md '/Documentation/ApiReference/UI_Widgets/dxDataGrid/Configuration/columns/#width') or the [visibleIndex](/api-reference/10%20UI%20Widgets/dxDataGrid/1%20Configuration/columns/visibleIndex.md '/Documentation/ApiReference/UI_Widgets/dxDataGrid/Configuration/columns/#visibleIndex').  

The options of the first column matching the name, column index, data field or caption will be changed by this method.

For the list of accessible options, refer to the [columns](/api-reference/10%20UI%20Widgets/dxDataGrid/1%20Configuration/columns '/Documentation/ApiReference/UI_Widgets/dxDataGrid/Configuration/columns/') option description. If you need to set only one option for a column, you can use the [columnOption(id, optionName, optionValue)](/api-reference/10%20UI%20Widgets/dxDataGrid/3%20Methods/columnOption(id_optionName_optionValue).md '/Documentation/ApiReference/UI_Widgets/dxDataGrid/Methods/#columnOptionid_optionName_optionValue') method instead.