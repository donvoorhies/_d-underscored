Replace the "button"-element within the: 

"&lt;nav id="site-navigation" class="main-navigation"&gt;-element to:
&lt;button class="menu-toggle" aria-controls="primary-menu" aria-expanded="false"&gt;&lt;?php esc_html_e( '&amp;equiv;', '_d-underscored' ); ?&gt;&lt;/button&gt; 

In short, you're (actually) changing "Menu" to "&amp;equiv;" this will generate the "burger" menu-icon (&equiv;) in the menu-button, when it's present/available.

**Recommendation:**
For better compatibility and translatability with the base Underscores (`_s`) theme, consider using its text domain `_s` instead of `_d-underscored`. The line would then be:
`&lt;?php esc_html_e( '&amp;equiv;', '_s' ); ?&gt;`
This ensures that the string can be translated with the rest of the `_s` theme if language files are used. If `_d-underscored` is your custom theme with its own full text domain setup, then using `_d-underscored` is appropriate.
