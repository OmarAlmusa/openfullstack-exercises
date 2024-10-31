```mermaid
sequenceDiagram
    participant browser
    participant server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa
    activate server
    server->>browser: HTML document
    deactivate server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    activate server
    server->>browser: CSS file
    deactivate server

    browser->> server: GET https://studies.cs.helsinki.fi/exampleapp/spa.js
    activate server
    server->>browser: spa.js file
    deactivate server

    browser->> server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    activate server
    server->> browser: data.json file
    deactivate server

    browser->> server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server->> browser: {"message":"note created"} + updated data.json
    deactivate server

```