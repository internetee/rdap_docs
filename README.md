# .ee RDAP API Documentation

This repository contains the OpenAPI specification and rendered documentation for the
**.ee RDAP service** — the Registration Data Access Protocol (RFC 7480 / RFC 9083, with
RFC 9560 `farv1` federated authentication via eeID) for `.ee` domains.

The documentation is generated with [ReDoc](https://github.com/Redocly/redoc) from a single
source file, `openapi/openapi.yaml`, mirroring the sibling `reservation_api_docs` project.

## Viewing the Documentation

The site is published to GitHub Pages on every push to the default branch (see
`.github/workflows/deploy.yml`). The committed `index.html` is the rendered single-page
documentation and can be opened directly in a browser.

## Development

To run the documentation locally with live reload:

1. Clone this repository
2. Run `npm install`
3. Run `npm start` and open the served URL

## Build

To build the static documentation (`index.html`):

1. Run `npm install`
2. Run `npm run build`

## Source of truth

The OpenAPI document describes the RDAP service **as implemented** — every endpoint,
response member, and example value is taken from the RDAP source and its golden test
fixtures, not invented. Notice/legal wording that is still a placeholder in the service is
reflected as such here and is owned by the legal sign-off step; the production base URL in
`servers:` is a placeholder until the prod host is fixed.
