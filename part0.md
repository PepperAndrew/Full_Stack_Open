# Part 0 - Diagrams

## 0.4: New note diagram
```mermaid
sequenceDiagram
    browser->>server: POST /new_note
    server-->>browser: 302 Redirect
    browser->>server: GET /notes
    server-->>browser: HTML file
    browser->>server: GET /main.css
    server-->>browser: CSS file
    browser->>server: GET /main.js
    server-->>browser: JS file
    browser->>server: GET /data.json
    server-->>browser: JSON file (notes list)
```

## 0.5: Single page app diagram
```mermaid
sequenceDiagram
    browser->>server: GET /spa
    server-->>browser: HTML file
    browser->>server: GET /main.css
    server-->>browser: CSS file
    browser->>server: GET /main.js
    server-->>browser: JS file
    browser->>server: GET /data.json
    server-->>browser: JSON file (notes list)
```

## 0.6: New note in Single page app diagramm
```mermaid
sequenceDiagram
    browser->>server: POST /new_note_spa
    server-->>browser: 201 Created
    note over browser: JavaScript adds new note and rerenders page
```
