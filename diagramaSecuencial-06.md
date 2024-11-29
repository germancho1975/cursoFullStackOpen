sequenceDiagram
    participant browser
    participant server

    Note right of browser: El usuario escribe una nota y hace clic en el botón Save
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: {"content": "nueva nota", "date": "2024-02-29"}
    deactivate server

    Note right of browser: El navegador ejecuta el código JavaScript
    Note right of browser: La nueva nota se renderiza instantáneamente en la página