I, Chen-Pang He (jdh8), subset [Libertinus Sans][libertinus] for the French
suit symbols:

- ♠ (U+2660)
- ♥ (U+2665)
- ♦ (U+2666)
- ♣ (U+2663)

Libertinus draws its suits at its own cap height, 0.63 em, so the outlines are
scaled 1.13x to the cap height of [Open Sans][open], 0.71 em, which is also
close to common `system-ui` fonts.  This is the same file as the polish.club
bridge books; see `suits.py` in that repository.

Declare the face with `unicode-range: U+2660, U+2663, U+2665-2666`.  The
subset keeps Libertinus's vertical metrics, whose ascent (0.894 em) is far
shorter than a typical `system-ui` font's.  Listed first in `font-family`
without the range, it becomes the first available font, so every line box
takes those metrics and every baseline rises by a pixel or two.  With the
range, it lacks U+0020 and only supplies the suit glyphs.

[open]: https://fonts.google.com/specimen/Open+Sans
[libertinus]: https://github.com/alerque/libertinus
