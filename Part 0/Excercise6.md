sequenceDiagram
    participant browser
    participant server

    Note right of browser: User interacts with the SPA, creates a new note

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/spa/new_note
    activate server
    server-->>browser: 200 OK (Note saved)
    deactivate server

    Note right of browser: The SPA updates the UI to display the new note
