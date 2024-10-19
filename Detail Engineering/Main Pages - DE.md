[[TCC chart]]

# Components of Electrical sys.:
[[Main Page - CB | Main Page - Circuit breaker]]
[[Main page - relay]]
[[Detail Engineering/Components/Transformer/Main Page - Transformer]]
[[Main Page - Motor]]
## Folders that are to study:

- [[Root Cause Analysis Methods]]
- [[Main Page - IS]]
- [[Main Page - Inst.]]
- [[Main Page - Utility]]


### Calculations sheets we have:
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

// Refresh every 10 seconds (100000 milliseconds)
setInterval(renderTable, 100000);
```

