# Spelling Bee Practice — PDF import version

Upload `index.html` to the root of the `spelling-bee-practice` repository, then enable GitHub Pages under **Settings → Pages → Deploy from a branch → main → /(root)**.

Students select the exact original PDF. The app checks the file's SHA-256 fingerprint and attempts to extract its words in the browser. The PDF is not uploaded to a server.

Notes:
- PDF.js is loaded from a public CDN, so the browser needs internet access to load the reader library.
- This browser-side file check is a convenience gate, not strong security; technically skilled users can bypass client-side checks.
- The configured fingerprint accepts only the exact original PDF file used during setup.
- If PDF extraction reports that it could not extract enough entries, the PDF parsing logic needs adjustment for the source PDF's text layout.
