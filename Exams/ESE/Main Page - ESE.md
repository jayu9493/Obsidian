---
Exam: Yes
Finished: No
---
### colander:

- [[RevisedAnnualCalendar-2025-UPSC.pdf | UPSC Calender]]

## PYQs:
```dataviewjs
const folderPath = "Exams/ESE/supporting files/PYQs"; // Your folder path

function renderTable() {
    // Clear previous content
    dv.container.empty();
    
    // Get Excel files
    const excelFiles = app.vault.getFiles().filter(file => 
        file.path.startsWith(folderPath) && 
        (file.extension === "pdf" )
    ).sort((a, b) => a.name.localeCompare(b.name)); // Sort alphabetically

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

// Refresh every 10 seconds (10000 milliseconds)
setInterval(renderTable, 1000000);
```

## Playlist for preparation:

### Technical subjects:

| Topics                                     | Playlist link                                                                            | Tutor                                  |
| ------------------------------------------ | ---------------------------------------------------------------------------------------- | -------------------------------------- |
| 1. Engineering Mathematics:                | https://youtube.com/playlist?list=PLvTTv60o7qj_tdY9zH7YceES7jfXiZkAz&si=WUZSkh5SkKGjljG6 | Vishal Soni(Gate wallah)               |
| 2. Electrical Materials:                   |                                                                                          |                                        |
| 3. Electric Circuits and Fields:           | https://youtube.com/playlist?list=PL3eEXnCBViH8lKOXZeghNfHmr2C8FNldP&si=xTOflQB0K0w-ytuC | GATE Wallah(circuits are not included) |
| 4. Electrical and Electronic Measurements: |                                                                                          |                                        |
| 5. Computer Fundamentals:                  |                                                                                          |                                        |
| 6. Basic Electronics Engineering:          |                                                                                          |                                        |
| 1. Analog and Digital Electronics:         | 1. Analog Electronics:                                                                   |                                        |
| 2. Systems and Signal Processing:          |                                                                                          |                                        |
| 3. Control Systems:                        |                                                                                          |                                        |
| 4. Electrical Machines:                    |                                                                                          |                                        |
| 5. Power Systems:                          |                                                                                          |                                        |
| 6. Power Electronics and Drives:           |                                                                                          |                                        |
