# What's this
Sample project of chrome extention.

# About mani
`manifest.json` is the central definition of chrome extention. Behaves like an entry point.  

## background
- scripts executed in background
- must be registered in manifest.json at least 1 background  
- `service_worker` script may have some codes to create app's initial context  
```json
    "background": {
        "service_worker": "background.js"
    },
```

## permissions
- same as smartphone app, chrome needs to be given the permissions to access to/execute something 
```json
"permissions": ["storage", "activeTab", "scripting"],
```
note that the permissions names are constant(choose the one defined by google)

## action
- settings for toolbar icon & action
```json
    "action": {
        "default_popup": "popup.html",
        "default_icon": {
            "16": "/images/get_started16.png",
            "32": "/images/get_started32.png",
            "48": "/images/get_started48.png",
            "128": "/images/get_started128.png"
        }
    }
```

## icons
- icons used as favicon, extension mgr, etx. 
```json
    "icons": {
        "16": "/images/get_started16.png",
        "32": "/images/get_started32.png",
        "48": "/images/get_started48.png",
        "128": "/images/get_started128.png"
    }
```

This project is based on https://developer.chrome.com/docs/extensions/mv3/getstarted/ 