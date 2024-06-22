
```mermaid
sequenceDiagram

participant user
participant browser
participant server


user ->> browser: Save note
activate browser
Note right of browser: The browser creates a new note with the content and a generated date, then redraws the notes
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: 201 Created
    deactivate server
```