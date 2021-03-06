WordPress Plugin Profiler
==========================

Basic profiler for WordPress Plugins. Benchmarks any given plugin by testing response times with and without the plugin activated.

Usage
-----

Since this plugin needs to have control over the plugins which are loaded, it needs to be in your `mu-plugins` folder. An easy way to do so is 
by installing the plugin in your plugins folder and then placing the following file in `/wp-content/mu-plugins/plugin-profiler.php`.

```php
// load the plugin profiler plugin early
require_once WP_PLUGIN_DIR . '/plugin-profiler/plugin-profiler.php';
```

To run a profile on any given plugin, visit **Tools > Plugin Profiler** in your WordPress admin area and select the plugin to profile.

Here's a rundown of the configuration settings.

| URL parameter | Description           |
| ------------- |:-------------:|
| slug     		| The full file slug of the plugin you want to profile      |
| n 			| The number of times the profile should run for each step. (default=10)     |
| url			| The URL which should be profiled against.	(default=homepage)|

