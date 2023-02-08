Here is a sequence diagram for a successful new note insert attempt:

```mermaid
sequenceDiagram
    note left of Browser: User inputs details into new note form

    Browser->>+Server: POST https://studies.cs.helsinki.fi/exampleapp/notes
    
    note right of Server: server validates the note then inserts the note onto the database
    
    Server-->>-Browser: return redirect to new note page
    Browser->>+Server: GET https://studies.cs.helsinki.fi/exampleapp/notes/{new note id}
    Server-->>-Browser: HTML document
    Browser->>+Server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    Server-->>-Browser: CSS file
    Browser->>+Server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
    Server-->>-Browser: JS file
    
    note right of Browser: The browser starts executing the javascript code
    note left of Browser: The user can now see the new blog post
  
```
