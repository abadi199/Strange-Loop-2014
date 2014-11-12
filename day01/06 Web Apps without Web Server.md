Web Apps without Web Server
===========================

Richard Feldman
@rtfeldman

## Native apps vs web apps
- Past reputation of web apps (slow, clunky)
- Minimal server interaction
- Example (which one requires server interaction):
    + dreamwriter.io (no server interaction)
    + no web server (static file on amazon s3)

## The App Cache
- Application cache is a douchebag - Jake Archibald
- cache manifest
    + cache: list of resources (pre-cache)
    + network: put * so if not available in the cache, will get it from the network
    + fallback: if resource is not available, specify the fallback file.

<blockquote>
    <html manifest="http://example.com/my-app.cache">
</blockquote>


## Reading Files
- FileReader API

## Downloading Data
- Blob
- FileSaver.js (polyfill)

## Offline Persistence
- localStorage (sync, capped 5mb because it's sync - blocking)
- IndexedDB (async, large data, document database)
    + Quota prompt to increase the maximum size

## Third party service
- Dropbox sync integration
- Problem: Same origin policy
    + CORS - send ahead the ok to whitelist the client
    + easyXDM (using iframe and javascript to communicate with the local iframe, hacky, clunky)
- OAuth 2
- Browser file package manager
- 

## Future
- Native app still first class citizen in the OS
- Fluid
- Web Manifest proposal