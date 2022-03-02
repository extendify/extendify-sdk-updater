# Extendify Updater Workflow

To use, add this workflow to your project and manually run it from GitHub actions.

> ⚠️ If extendify isn't located in /extendify-sdk then you will need to update the workflow accordingly to match the directory you installed it into

## First install
If Extendify isn't yet installed, first add and run the workflow to create a new PR with the latest from Extendify. Next, load it into your plugin from the main plugin file (or where ever makes the most sense):
```php
require_once plugin_dir_path( __FILE__ ) . 'extendify-sdk/loader.php'

if ( ! isset( $GLOBALS['extendify_sdk_partner'] ) ) {
    // phpcs:ignore WordPress.NamingConventions.PrefixAllGlobals.NonPrefixedVariableFound
    $GLOBALS['extendify_sdk_partner'] = 'Plugin Name';
}
```
