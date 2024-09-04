```mermaid
  sequenceDiagram
    participant browser
    participant server

  browser->>server:HTTP POST https://studies.cs.helsinki.fi/exampleapp/spa/new_note_spa
  Note right of browser:content-type: application/json  content:"a" date:"2024-09-04"
  activate server
  server-->>browser: Code 201 created
  deactivate server
  Note right of browser:browser executes the event handler that renders notes to display
```
