# PFI Tree Volume Calculator — Version 1.1

Developed by Forestry Research Division, Pakistan Forest Institute, Peshawar.

Repository owner: Faizan-Qnadil. Prepared for Cloudflare Pages hosting; deployment to Cloudflare is pending.

## Contents

- `dist/`: deployable static application, PFI logo, equations, inventory tools and offline support.
- `review/`: equation inclusion decisions and provenance. Do not publish this directory as website assets.
- `DEPLOYMENT.md`: ownership, publishing and migration instructions.
- `CHECKSUMS.json`: SHA-256 checksums of application files.

Application version: 1.1. Equation set: 1; 52 included tables. The equations are identical to the current published calculator. Unresolved tables remain excluded. Numerical agreement with source tables does not replace independent field validation.

All volume calculations, imports, exports and inventory storage run in the browser. No AI service, API key, database, npm installation or server functions are required. Saved inventories remain in the user's browser; clearing browser data may delete them. Export JSON backups regularly.

## Local preview

Run `python3 -m http.server 8000 --directory dist` from this folder and open http://localhost:8000. Do not open index.html directly as a file: modules and service workers need an HTTP origin (HTTPS for public hosting).

## Release maintenance

Use Git commits for every reviewed change and a release tag such as v1.1.0 for the first institutional release. Keep the application version and equation-set version separate. When app assets change, update the cache identifier in dist/sw.js. When equations change, document source evidence and range checks, update the equation-set version, and validate against the approved tables before deployment.

No open-source licence has been assigned by this package. PFI should choose its distribution and licensing terms.
