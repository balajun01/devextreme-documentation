---
type: Object
---
---
##### shortDescription
Specifies options for the underlain editor.

---
Depending on the [dataType](/api-reference/10%20UI%20Widgets/GridBase/1%20Configuration/columns/dataType.md '{basewidgetpath}/Configuration/columns/#dataType'), the column offers a user different widgets for editing and filtering (using the [filter row](/concepts/05%20Widgets/DataGrid/30%20Filtering%20and%20Searching/1%20Filter%20Row.md '/Documentation/Guide/Widgets/{WidgetName}/Filtering_and_Searching/#Filter_Row')): [TextBox](/api-reference/10%20UI%20Widgets/dxTextBox '/Documentation/ApiReference/UI_Widgets/dxTextBox/'), [DateBox](/api-reference/10%20UI%20Widgets/dxDateBox '/Documentation/ApiReference/UI_Widgets/dxDateBox/'), [Lookup](/api-reference/10%20UI%20Widgets/dxLookup '/Documentation/ApiReference/UI_Widgets/dxLookup/'), etc. In the **editorOptions** object, you can specify options for the widget.

[note]

Do not specify the **onValueChanged** option in this object. If you need to add custom logic to the standard value change handler, override the handler in the [onEditorPreparing](/api-reference/10%20UI%20Widgets/dxDataGrid/1%20Configuration/onEditorPreparing.md '{basewidgetpath}/Configuration/#onEditorPreparing') function in the following manner.

---
##### jQuery

    <!--JavaScript-->$(function() {
        $("#dataGridContainer").dxDataGrid({
            // ...
            onEditorPreparing: function(e) {
                if (e.dataField == "requiredDataField") {
                    var standardHandler = e.editorOptions.onValueChanged;
                    e.editorOptions.onValueChanged = function(e) { // Overriding the standard handler
                        // ...
                        // Custom commands go here
                        // ...
                        standardHandler(e); // Calling the standard handler to save the edited value
                    }
                }
            }
        });
    });

##### Angular
    
    <!--TypeScript-->
    import { DxDataGridModule } from 'devextreme-angular';
    // ...
    export class AppComponent {
        onEditorPreparing (e) {
            if (e.dataField == "requiredDataField") {
                let standardHandler = e.editorOptions.onValueChanged;
                e.editorOptions.onValueChanged = function (e) { // Overriding the standard handler
                    // ...
                    // Custom commands go here
                    // ...
                    standardHandler(e); // Calling the standard handler to save the edited value
                }
            }
        }
    }
    @NgModule({
        imports: [
            // ...
            DxDataGridModule
        ],
        // ...
    })

    <!--HTML-->
    <dx-data-grid ... 
        (onEditorPreparing)="onEditorPreparing($event)">
    </dx-data-grid>
    
---

[/note]