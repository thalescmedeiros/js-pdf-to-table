# js-pdf-to-table
Read all pages from a PDF file and returns an array containing all tables found and the text contents for each cell in a JavaScript object format. Requires jsPDF plugin.

Format returned:

```
[
  {  // This is one page
    w: NUMBER,
    h: NUMBER,
    tables:
    [  // Every element is a table of the current page
      { // This is the first table of the page
        x: NUMBER,  // coordinates in reference to the page
        y: NUMBER,  // coordinates in reference to the page
        w: NUMBER,
        h: NUMBER,
        numberRows: NUMBER,
        numberColumns: NUMBER,
        cells: [  // Every element is a cell of the current table
          {  // This is the first cell of the table
            x: NUMBER,  // coordinates in reference to the table
            y: NUMBER,  // coordinates in reference to the table
            w: NUMBER,
            h: NUMBER,
            rowStart: NUMBER,    // starting at 0 for the first vertical line
            rowEnd: NUMBER,
            columnStart: NUMBER, // starting at 0 for the first horizontal line
            columnEnd: NUMBER,
            text: STRING
          }
        ]
      }
    ]
  }
]
```
