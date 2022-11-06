Replace the "button"-element within the "&lt;nav id="site-navigation" class="main-navigation"&gt;-element to:
&lt;button class="menu-toggle" aria-controls="primary-menu" aria-expanded="false"&gt;&lt;?php esc_html_e( '&amp;equiv;', '_d-underscored' ); ?&gt;&lt;/button&gt; 
In short, you're (actually) changing "Menu" to "&equiv;" this will generate the "burger" menu-icon in the menu-button, when it's present/available.
