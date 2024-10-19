- data view supports three formats list, table and task. 
- default it showcase all the tasks or files.
- for list it is default but for table we can do customizations.
---
#### List
- for retrieving the list of files:
- ```LIST``` is enough.
##### Queries
###### from
- for certain **tag** ```LIST FROM #Electrical ``` and all the notes from electrical tag will show up.
- from **folder** ```LIST FROM "Exams" ``` and all the notes from Exams folder will show up.
- we can also apply **logical expressions** to dataview such as ```AND``` & ```OR``` to the list and exclude things by applying``` FROM -#electrical```.
###### where
- for finding specific author ```LIST WHERE contains(author, " Name of author")```
###### sort
- 
---
#### Table
- for table if you want with created on date then write ```TABLE createdon```
- for author to write as Author write ```TABLE author AS Author```
- many other functionality can be achieved but for some time it is enough
##### Queries:
###### Where:
- searching the file name and author of it.
- ``` TABLE author WHERE file.name = " File Name" ``` this way you will only get one file and it's author.
- it can be used for logical too. 
- ``` TABLE from #Electrical where file.size>1``` this will only show the files which got more then 1 bytes size.
###### sort
- sort the file size table in ascending order.
- ```TABLE FROM #Electrical WHERE file.size>100 SORT file.size asc``` and desc for descending order.
- 
- ---
#### Tasks
- for task write ```TASK``` and all the task from vault will show up.
### from:
```dataview
LIST FROM "Exams"
```

---
##### My categories that i want to make:
###### Tags
1. Electrical
	1. Motors
	2. Protection system
	3. Distribution system.
2. Detail Engineering


#### DataviewJS:
```dataviewjs
const folderPath = "Detail Engineering/calculation sheets"; // Your folder path

function renderTable() {
    // Clear previous content
    dv.container.empty();
    
    // Get Excel files
    const excelFiles = app.vault.getFiles().filter(file => 
        file.path.startsWith(folderPath) && 
        (file.extension === "xlsx" || file.extension === "xls")
    );

    // Render new table
    dv.table(["File Name", "Created On"], 
        excelFiles.map(f => [
            dv.fileLink(f.path), 
            new Date(f.stat.ctime).toLocaleDateString()
        ])
    );
}

// Initial render
renderTable();

// Refresh every 10 seconds (100000000 milliseconds)
setInterval(renderTable, 100000000);
```

#### Metadata of file:

| **Field Name**    | **Data Type**  | **Description**                                                                                                                                                                 |
|-------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| file\.name        | Text           | The file name as seen in Obsidians sidebar\.                                                                                                                                    |
| file\.folder      | Text           | The path of the folder this file belongs to\.                                                                                                                                   |
| file\.path        | Text           | The full file path, including the files name\.                                                                                                                                  |
| file\.ext         | Text           | The extension of the file type; generally md\.                                                                                                                                  |
| file\.link        | Link           | A link to the file\.                                                                                                                                                            |
| file\.size        | Number         | The size \(in bytes\) of the file\.                                                                                                                                             |
| file\.ctime       | Date with Time | The date that the file was created\.                                                                                                                                            |
| file\.cday        | Date           | The date that the file was created\.                                                                                                                                            |
| file\.mtime       | Date with Time | The date that the file was last modified\.                                                                                                                                      |
| file\.mday        | Date           | The date that the file was last modified\.                                                                                                                                      |
| file\.tags        | List           | A list of all unique tags in the note\. Subtags are broken down by each level, so \#Tag/1/A will be stored in the list as \[\#Tag, \#Tag/1, \#Tag/1/A\]\.                       |
| file\.etags       | List           | A list of all explicit tags in the note; unlike file\.tags, does not break subtags down, i\.e\. \[\#Tag/1/A\]                                                                   |
| file\.inlinks     | List           | A list of all incoming links to this file, meaning all files that contain a link to this file\.                                                                                 |
| file\.outlinks    | List           | A list of all outgoing links from this file, meaning all links the file contains\.                                                                                              |
| file\.aliases     | List           | A list of all aliases for the note as defined via the YAML frontmatter\.                                                                                                        |
| file\.tasks       | List           | A list of all tasks \(I\.e\., \| \[ \] some task\) in this file\.                                                                                                               |
| file\.lists       | List           | A list of all list elements in the file \(including tasks\); these elements are effectively tasks and can be rendered in task views\.                                           |
| file\.frontmatter | List           | Contains the raw values of all frontmatter in form of key \| value text values; mainly useful for checking raw frontmatter values or for dynamically listing frontmatter keys\. |
| file\.day         | Date           | Only available if the file has a date inside its file name \(of form yyyy\-mm\-dd or yyyymmdd\), or has a Date field/inline field\.                                             |
| file\.starred     | Boolean        | If this file has been bookmarked via the Obsidian Core Plugin "Bookmarks"\.                                                                                                     |
