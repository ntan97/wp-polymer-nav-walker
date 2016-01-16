# wp-polymer-nav-walker
Custom Nav Walker to format links and print out a paper-menu and paper-item navigation system into a polymer based WordPress theme; Designed to be used in [Polypress](https://github.com/ntan97/Polypress), but maintained seperately for anyone with a polymer based theme.

## How to Use
wp-polymer-nav-walker is designed to be used in wp_nav_menu(), and you should already have Polymer elements included as imports in your header.php, or through another method. 

```PHP
$args = array(
    'menu'  => 'header_menu',
    'theme_location'  => 'header_menu',
    'container'         => false,
    'items_wrap'      => '<paper-menu id="%1$s" class="%2$s">%3$s</paper-menu>',
    'walker'          => new polymer_walker_nav_menu(),
    'fallback_cb'     => 'polymer_walker_nav_menu::fallback',
);

wp_nav_menu($args);
```
