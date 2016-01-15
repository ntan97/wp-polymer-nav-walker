# WP_Polymer_Nav_Walker
Custom Nav Walker to format links properly and navigation for paper-menu element

## How to Use
WP_Polymer_Nav_Walker is designed to be used in wp_nav_menu(), and you should already have polymer elements included as imports in your header.php, or through another method

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
