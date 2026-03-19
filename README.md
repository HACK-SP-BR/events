# events

Public event database for Hack SP.

This repository stores public event data in a simple JSON file and serves images from GitHub raw URLs.

## Files

```txt
events/
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
      "https://raw.githubusercontent.com/HACK-SP-BR/events/main/assets/events/daydream-sp/event1.jpeg"
    ]
  }
}
```

## Public usage

This repository is meant to be consumed directly from GitHub raw URLs.

Main JSON file:

```txt
https://raw.githubusercontent.com/HACK-SP-BR/events/main/events.json
```

Images also use raw GitHub URLs:

```txt
https://raw.githubusercontent.com/HACK-SP-BR/events/main/assets/events/daydream-sp/event1.jpeg
```

## Notes

* Keep all image URLs public
* Use full raw GitHub URLs inside `events.json`
* Do not use local imports in the JSON file
* This repository is public and intended for read-only use by websites and apps