# _d (Underscored)
The repository for my slight variant (or tweak) of the _s-theme ("Underscores" - by Automattic: https://github.com/Automattic/_s), which I've named: _d (as in "Underscored").

Insert (Copy&Paste) the posted CSS in the theme's "Appearance"-section -> "Customize"-section ->"Additional CSS", publish and you're good to go...

Regarding the markdown-file at: https://github.com/donvoorhies/_d-underscored/blob/main/4header_php.md - view the file to see the alterations and the code needed to be done with the "headers.php"-file...

No additional `<div class="push"></div>` markup is required anymore for sticky footer support.
The current CSS uses a flexbox-based layout that works without template edits.

## Compatibility and safety notes

- Keep the reCAPTCHA badge visible when using plugins that require it.
- Use the documented text domain consistently across your theme files.
- Test menu toggle behavior on small screens after header changes.

## Quick test checklist

1. Homepage loads with no layout shift in header/footer.
2. Mobile menu toggle appears and opens/closes correctly.
3. Footer stays at the bottom on short-content pages.
4. Keyboard focus is visible on links and menu button.
