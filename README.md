# hacksp-events

Public event database for Hack SP.

This repository stores public event data in a simple JSON file and serves images through a free CDN.

## Files

```txt
hacksp-events/
├── events.json
└── assets/
    └── events/
        ├── daydream-sp/
        │   ├── event1.jpeg
        │   ├── event2.jpeg
        │   ├── event3.jpeg
        │   ├── event4.jpeg
        │   └── event5.jpeg
        └── drx_hacksp/
            ├── drx_banner.jpg
            ├── event1.jpeg
            ├── event2.jpeg
            ├── event3.jpeg
            └── event4.jpeg
````

## JSON structure

The main file is:

```txt
/events.json
```

It contains a map of events.

Example:

```json
{
  "daydream": {
    "id": "daydream-sp",
    "status": "past",
    "name": "Daydream São Paulo",
    "videoUrl": "https://youtu.be/example",
    "websiteUrl": "https://example.com",
    "translations": {
      "pt": {
        "date": "27 de Setembro de 2025",
        "location": "IME-USP, São Paulo",
        "description": "Portuguese description"
      },
      "en": {
        "date": "September 27, 2025",
        "location": "IME-USP, São Paulo",
        "description": "English description"
      }
    },
    "stats": {
      "participants": "12+",
      "projects": "3",
      "duration": "10h"
    },
    "photos": [
      "https://cdn.jsdelivr.net/gh/USERNAME/hacksp-events/assets/events/daydream-sp/event1.jpeg"
    ]
  }
}
```

## CDN usage

This repository is meant to be consumed with jsDelivr.

Base format:

```txt
https://cdn.jsdelivr.net/gh/USERNAME/hacksp-events/events.json
```

Images also use the same CDN:

```txt
https://cdn.jsdelivr.net/gh/USERNAME/hacksp-events/assets/events/daydream-sp/event1.jpeg
```

## Notes

* Keep all image URLs public
* Use full CDN URLs inside `events.json`
* Do not use local imports in the JSON file
* This repository is public and intended for read-only use by websites and apps