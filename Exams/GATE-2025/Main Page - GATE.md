---
Exam: Yes
Finished: No
---


## PYQs:

```dataviewjs
const folderPath = "Exams/GATE-2025/supporting files/PYQs"; // Your folder path

function renderTable() {
    // Clear previous content
    dv.container.empty();
    
    // Get Excel files
    const excelFiles = app.vault.getFiles().filter(file => 
        file.path.startsWith(folderPath) && 
        (file.extension === "pdf" )
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

// Refresh every 10 seconds (10000 milliseconds)
setInterval(renderTable, 10000000);
- ```

## Syllabus:

- [[Exams/GATE-2025/supporting files/GATE _EE_2025_Syllabus.pdf|GATE _EE_2025_Syllabus]]

### Preparation playlist:

| Topics                                 | Playlist Link                                                                            | Tutor                    |
| :------------------------------------- | ---------------------------------------------------------------------------------------- | ------------------------ |
| Engineering Mathematics                | https://youtube.com/playlist?list=PLvTTv60o7qj_tdY9zH7YceES7jfXiZkAz&si=WUZSkh5SkKGjljG6 | Vishal Soni(Gate wallah) |
| Electric circuits                      | do more and more **PYQs**                                                                |                          |
| Electromagnetic Fields                 | https://youtube.com/playlist?list=PL3eEXnCBViH8lKOXZeghNfHmr2C8FNldP&si=xTOflQB0K0w-ytuC | GATE Wallah              |
| Signals and Systems                    | https://youtube.com/playlist?list=PLR7krO3VHssSsUoMzIyYrUre_dM4M9LfI&si=rCl5nmbTXqb-Myv7 | Ankit Goyal              |
| Electrical Machines                    | https://youtube.com/playlist?list=PLs5_Rtf2P2r5YY5b23uDGrtpo42ezMmGp&si=9ErqzBrNrYVQ9MyW | Ankit Goyal              |
| Power Systems                          | https://youtube.com/playlist?list=PLe8lX1SLwAPG_ssxiyipma2oHqeusP3co&si=O2YECf9R_4l4O_1G | Ankit Goyal              |
| Control Systems                        | https://youtube.com/playlist?list=PLA9RS_96_LD53SbY9hcOVsw6dQvkHiVka&si=dS6cTAKvGbuUh0KK | Ankit Goyal              |
| Electrical and Electronic Measurements | https://youtube.com/playlist?list=PLs5_Rtf2P2r69m2DL5loIcjGKCkQxXqHy&si=XoOfVxTVhBp0AB_1 | Prameet sir(Unacademy)   |
| Analog Electronics                     | https://youtube.com/playlist?list=PLs5_Rtf2P2r5MplAOADz3fTWIyBZTkGbB&si=UNgPi2yAnU3V36WE | Ankit Goyal              |
| Power Electronics                      | https://youtube.com/playlist?list=PLs5_Rtf2P2r7CiI8XOcYx9pOeuU7XsnJO&si=u3_9Lra-2c53WTjE | Ankit Goyal              |
| Digital Electronics                    | https://youtube.com/playlist?list=PLR7krO3VHssS2rKksstCXwB5B13CXcQqd&si=dJ52g34zGRVS865T | Ankit Goyal              |
