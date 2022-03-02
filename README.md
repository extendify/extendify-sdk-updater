# Extendify Updater Workflow
This repo includes a workflow for updating the Extendify SDK in partner plugins or themes.
## Ongoing updates
To update the Extendify SDK in a plugin or theme where it is already loaded:

1) Add the workflow in this repo to your project
2) Manually run it from GitHub actions
3) Merge the created PR

_Note: If extendify isn't located in /extendify-sdk then you will need to update the workflow accordingly to match the directory it is installed into_

## First install
If Extendify isn't yet installed:

1) Follow the steps above to add the SDK
2) Add the below code snippet to the main plugin file to load Extendify
3) Change the `Partner Name` to the name of your plugin or theme

```php
require_once plugin_dir_path( __FILE__ ) . 'extendify-sdk/loader.php'

if ( ! isset( $GLOBALS['extendify_sdk_partner'] ) ) {
    // phpcs:ignore WordPress.NamingConventions.PrefixAllGlobals.NonPrefixedVariableFound
    $GLOBALS['extendify_sdk_partner'] = 'Partner Name';
}
```

_Note: Be sure to update 'Partner Name' with the name of your product._
