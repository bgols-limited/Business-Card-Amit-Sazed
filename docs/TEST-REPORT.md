# Test report (Amit Sazed card), 2026-11-12

Tested in headless Chromium with the iPhone 13 profile (390 × 844, touch) against a local copy.

| Check | Result |
|---|---|
| Page loads, no console errors, no failed requests | Pass |
| No horizontal scroll at phone width | Pass |
| `tel:` links: +8801886813699 and +8801335134477 | Pass |
| WhatsApp link `wa.me/8801886813699` | Pass |
| WeChat sheet (quick button and contact row) shows +8801886813699 | Pass |
| `#qr` opens the card on the QR side; plain address opens the front | Pass |
| QR codes (SVG/PNG, printed card back, portrait card back) decode to `https://alshams8.github.io/Business-Card-Amit-Sazed/` | Pass (zxing-cpp) |
| `contact.vcf`: vCard 3.0, CRLF, lines ≤ 75 octets, two mobile numbers, embedded 256 px photo | Pass |
| card.html, nfc-setup.html, email-signature.html, manifest, sw.js load | Pass |

## Still to test on a real iPhone

- [ ] Save Contact in Safari shows the contact preview with photo, both numbers, website and card link.
- [ ] NameDrop between two iPhones (iOS 17.1+) after setting My Card.
- [ ] AirDrop of My Card and of the card link.
- [ ] Add to Home Screen icon and name ("Amit Sazed").
- [ ] Back Tap shortcut opens `#qr`.
- [ ] NFC tag written with NFC Tools opens the card on iPhone and Android.
- [ ] WeChat: the number can be found in WeChat search (depends on Amit's WeChat privacy settings).
