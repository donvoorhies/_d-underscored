Replace the "button"-element in "&lt;nav id="site-navigation" class="main-navigation"&gt;" to:
&lt;button class="menu-toggle" aria-controls="primary-menu" aria-expanded="false"&gt;&lt;?php esc_html_e( '&equiv;', '_d-underscored' ); ?&gt;&lt;/button&gt; 
In short, you're (actually) changing "Menu" to "&equiv;" this will generate the "burger" menu-icon in the menu-button, when it's present/available.
