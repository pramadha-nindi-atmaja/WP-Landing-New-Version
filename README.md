# WP Landing
* **Requires at least:** 4.6
* **Tested up to:** 5.1.1
* **Stable tag:** 1.0.0
* **Requires PHP:** 5.6
* **License:** GPLv3.0 or later
* **License URI:** https://www.gnu.org/licenses/gpl-3.0.en.html

## Description

The plugin allows you to create a performing landing page.
Use a custom method for including resources to maximize the page loading speed.

It is possible to overwrite the template file, from the theme in use through the filter <code>"wpl-page_template_plugin_dir_path"</code> 
to change the directory from which to take the file. On your theme you should have <code>templates/wpl.php</code>

## Dependence

WpLanding requires plugin <strong>ACF Pro - https://www.advancedcustomfields.com/</strong> to correctly insert all the fields on the template page. 
Using the <strong>ACF</strong> plugin, repeaters will not be displayed.

## Installation

This section describes how to install the plugin and make it work.

1. Upload the 'wplanding' folder to the /wp-content/plugins/
2. Install the PHP dependencies from inside the plugin folder (the `vendor/` directory is not committed):
   ```
   cd wp-content/plugins/wplanding
   composer install --no-dev
   ```
3. Install and enable **ACF Pro** (see Dependence above).
4. Enable <strong>WpLanding</strong> from the WordPress "Plugins" page.
5. Create a page and assign the "WP Landing template" page template.
6. Fill in the ACF fields on that page, then view it. If the site is set as a static front page, set this page as the front page under Settings > Reading.

## Troubleshooting

* **Site shows a maintenance message / blank or broken page:** make sure `composer install` was run, so `vendor/autoload.php` exists. Without it the plugin shows an admin notice and does nothing. If WordPress is stuck in maintenance mode after a failed update, delete the `.maintenance` file in the WordPress root. Also disable any maintenance / coming-soon plugin.
* **Page template not listed:** confirm the plugin is active and you are editing a *Page* (not a Post).
* **Sections empty:** ACF Pro is not active or the fields are not filled in.

## Development

Assets are compiled with Grunt (`npm install`, then `npx grunt`). Sources are in `assets/sass` and `assets/js`.

## Performaces

<img src="https://github.com/Picaland/wplanding/blob/master/wplanding-performance.jpg" alt="Wp Landing Performaces">

## Requirements

* **Php** >= 5.6
* **WordPress** >= 4.6

## Changelog

= 1.0.0 =
* Initial release