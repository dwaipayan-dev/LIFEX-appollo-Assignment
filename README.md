# LIFEX-appollo-Assignment

# Overview:
In another repository I have designed a reusable custom table UI component. This repository has the build files of that component and has an html file in mytable-in-action folder that demonstrates that component. I would like to thank LIFEX Apollo team for giving me opportunity to work on this project.

# Features of Customized table component

1. Reusable across all popular js frameworks. Runs on the node environment like Angular applications. Made on Angular Framework.
2. Simple to use
3. Easily extendable to any usecase.
4. Resizable columns
5. Column header and Cell Content are editable.
6. Toolbox buttons for inserting and deleting rows and columns.
7. Table supports large number of rows and columns. Can easily handle upto 100 rows x 100 columns. Becomes quite slow at 1000 rows x 1000 columns. Becomes inefficient beyond that.

# Prerequisites:

A server: To run the project go to "assignmentLIFEXdeployed\mytable-in-action" and type the following:

```
npm install -g serve
```

and then in the terminal type 

```
serve
```
This will initiate a node server and serve the index.html file. Go to the given URL in the terminal to see the web project in action


#Usage:
Create a new folder. You would need to copy all the files except index.html in the mytable-in-action folder. Make a new html file. Then in the body where you need the component include as such

```
<body>
  <!-- Prceding code -->
  <custom-table-widget id = "MyTable"></custom-table-widget>
  
  <script type="text/javascript" src="runtime-es5.js"></script>
  <script type="text/javascript" src="runtime-es2015.js"></script>
  <script type="text/javascript" src="polyfills-es5.js" nomodule></script>
  <script type="text/javascript" src="polyfills-es2015.js"></script>
  <script type="text/javascript" src="scripts.js"></script>
  <script type="text/javascript" src="main-es5.js"></script>
  <script type="text/javascript" src="main-es2015.js"></script>
  
<!-- Following code -->
</body>
```


# UI Guide:

# New Table box

This box has two input fields, for number of rows and number of columns. Once you enter the number of rows and columns. Click the submit button. A table of that many rows and columns will be created with a toolbox, having buttons for inserting and deleting rows and columns.

# The Table

1. The table will have as many rows and columns as specified by the user when created. 
2. Columns are named as c0, c1, ... by default, but they are editable. Rows are named r1, r2, ... by default and they are not editable. When a column is inserted it is labeled as 'New Column' by default but the names of other columns do not change. When a row is inserted/deleted the row numbers stay continuous. This is done as row number specify S.No which should be consistent, but column heads represent name of column which should stay same.
3. Cells are editable.
4. Columns are resizable. Just select the column you want to resize and drag horizontally.

# The Toolbox

The toolbox has 4 buttons as follows:

1. Insert Row: When a cell is selected, it is the active cell. On clicking the "Insert row" button, a new row is added below the row containing active cell. Row numbers stay continuous.

2. Insert Column: On clicking, a new column is added to the right of column containing active cell. The new Column is labelled as "New Column". Other column head do not change.

3. Delete Row: On clicking. The row containing active cell gets deleted.

4. Delete Column: On clicking. The column containing active cell gets deleted.

# Freeze/Unfreeze button:

When you have finalized the table. Click the Freeze button. It will remove the New Table box and Toolbox and it will freeze the table (Table would be non editable). THe Freeze button would be replaced by Unfreeze button which would restore New Table box and Toolbox and make table editable again.

# Bugs and Bottlenecks:
Though I have tried my best to make this project completely bug free. It has not been possible. These are the known bugs and bottlenecks that I aim to fix in future.

1. Very rarely the content of the cell gets duplicated which is manually fixable by deleting duplicate content from the end.
2. The table becomes quite slow at 1000 rows x 1000 columns. Becomes inefficient beyond that. As I am still using for loops and a bigger table means more rendering, it becomes slower above 1,000,000 cells.

# Final Note:
Thank you for reading this far. If you face any issues with the component, feel free to connect to me about it. I would look forward to your feedback:)

