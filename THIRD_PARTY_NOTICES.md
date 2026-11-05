# Third-party resources

This package retains the supplied research website template and bundles its runtime dependencies for independent static hosting.

- **Nerfies website template**: https://github.com/nerfies/nerfies.github.io — original template attribution and Creative Commons Attribution-ShareAlike 4.0 link remain in the page footer.
- **Bulma** and the supplied Bulma Carousel / Slider libraries: copied from the user's template; copyright and license comments are retained in those files.
- **jQuery 3.5.1**: https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js — MIT license; original header retained.
- **Font Awesome Free 5.15.1**: https://fontawesome.com/license/free — Icons: CC BY 4.0; fonts: SIL OFL 1.1; code: MIT. Original CSS and JS headers are retained. Matching font files are bundled in `static/webfonts/`.
- **Google Sans, Noto Sans and Castoro**: the existing template font declarations were obtained from the Google Fonts CSS endpoint and localized. The returned font files are bundled in `static/fonts/`. Original download URLs are recorded in `asset-manifest.json`; the website does not request the remote CSS or fonts at runtime.

Research text, figures, recordings and manuscript are the supplied ViTacDex materials. The template's license attribution does not assign a new license to the research materials.
