```mermaid
    sequenceDiagram
    participant browser
    participant server
    
    Note over browser: User creates a new note in the SPA
    browser->>browser: User enters content in the form and submits it
    
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/notes
    Note right of browser: The browser sends the new note data to the server
    activate server
    server-->>browser: Response with status (e.g., 200 OK)
    deactivate server
    
    Note right of browser: The SPA updates the UI to show the newly created note
    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    activate server
    server-->>browser: Updated JSON data with the new note
    deactivate server
    
    Note right of browser: The browser re-renders the notes, including the new one
