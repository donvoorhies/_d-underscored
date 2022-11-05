Replace the "button"-element in "<nav id="site-navigation" class="main-navigation">" to:
<button class="menu-toggle" aria-controls="primary-menu" aria-expanded="false"><?php esc_html_e( '&equiv;', '_d-underscored' ); ?></button> 
In short, you're (actually) changing "Menu" to "&equiv;" this will generate the "burger" menu-icon in the menu-button, when it's present/available. 
