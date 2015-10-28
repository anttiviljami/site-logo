# Site Logo

[![License](https://poser.pugx.org/automattic/jetpack/license.svg)](http://www.gnu.org/licenses/gpl-2.0.html)

Add a logo to your WordPress site. Set it once, and all themes that support it will display it automatically.

A standalone version of the WordPress Site Logo feature included in [Jetpack](https://github.com/Automattic/jetpack)'s *theme-tools* module. Also used on WordPress.com

## Why?

[The original standalone version](https://github.com/Automattic/site-logo) of Site Logo by Automattic was merged to Jetpack and is sadly no longer being updated.

This plugin is for themes that don't want to require all of Jetpack, but still want to declare `add_theme_support( 'site-logo' );` and use the simple Customizer upload interface.

## Installation

1. Upload the `site-logo` folder to the `/wp-content/plugins/` directory, or check out the plugin from GitHub: `git clone git@github.com:anttiviljami/wp-site-logo.git`.
2. Activate the plugin through the 'Plugins' menu in WordPress.
3. Add support by adding `add_theme_support( 'site-logo' );` to the theme's setup function.
4. Use the `the_site_logo()` template tag in `header.php` to display the logo on the front-end.

## Use

Declare theme support for the *site-logo* feature in your theme `functions.php`

```HTML+PHP
<?php add_theme_support( 'site-logo', array( 'size' => 'full' ) ); ?>
```

In your theme `header.php`, or wherever you wish to use your logo, just use:

```HTML+PHP
<?php the_site_logo(); ?>
```

or

```HTML+PHP
<?php echo get_the_site_logo(); ?>
```

which would both output

```HTML
<a href="http://amazing.com/" class="site-logo-link" rel="home">
    <img width="200" height="200" src="http://amazing.com/wp-content/uploads/2014/09/logo.jpg" class="site-logo attachment-mytheme-logo" alt="Company logo" data-size="mytheme-logo">
</a>
```

Full Jetpack doc for *site-logo*: http://jetpack.me/support/site-logo/
