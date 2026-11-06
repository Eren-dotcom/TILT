# TILT

An interactive business-card studio: customize a card, tilt it to reveal a hidden message, then share a permalink, save a vCard, or print a trim-and-bleed sheet.

## Run locally

This is a static app with no build step. From the repository root:

```sh
python3 -m http.server 8000 --bind 0.0.0.0
```

Open `http://localhost:8000`. State is saved in local storage; the share action uses the URL hash to carry a card's editable design (no uploaded images or personal data are sent to a server).

## Included

- Ten starter templates, seven card layouts, and nine color finishes
- Live editing for font family, name case/alignment/scale, contact arrangement, and text/accent/background colors
- Local logo, portrait (circle/square), and background image uploads with opacity/veil controls
- Mouse tilt plus touch drag/tap reveal, glare, and angle-gated message
- Browser-local autosave, URL permalink, undo/redo
- 3× PNG export, vCard download, share/copy-link actions
- Print sheet for a 105 × 60 mm trim card, with 3 mm bleed on every side (111 × 66 mm sheet) and crop marks

The permalink contains the full card state, including its message and contact details. It is encoded in the URL fragment and is not a secure-storage format. The app is dependency-free; typography loads from Google Fonts when a network connection is available.
