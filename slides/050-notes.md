##

<h1>Notes</h1>

## Browser APIs (window, document, Location, etc)

**Not directly available**

Angular provides wrapped services

```javascript
import { Location, DOCUMENT } from '@angular/common';
// ...
  constructor(
    private location: Location,
    @Inject(DOCUMENT)
    private document: Document
) {  }
```

## Preboot

Capture and replay events (click, keyup, etc)

[https://github.com/angular/preboot](https://github.com/angular/preboot)

Framework Agnostic with extra utilities for Angular

## Routing

- Using absolute URLs for server requests

- Filtering request URLs: must distinguish app page requests other kinds *(handled automatically by NgUniversal Express schematic)*




## Static Assets (images, etc)

only honor requests for files from the /dist folder.

**server.ts**
```javascript
// Serve static files from /browser
app.get('*.*', express.static(join(DIST_FOLDER, 'browser')));
```

---
