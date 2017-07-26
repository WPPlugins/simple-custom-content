=== Simple Custom Content ===

Plugin Name: Simple Custom Content
Plugin URI: https://perishablepress.com/simple-custom-content/
Description: Easily add custom content to your WP Posts and RSS Feeds.
Tags: content, custom content, customize, feeds, posts, rss
Author: Jeff Starr
Author URI: https://plugin-planet.com/
Donate link: https://m0n.co/donate
Contributors: specialk
Requires at least: 4.1
Tested up to: 4.8
Stable tag: 20170325
Version: 20170325
Text Domain: simple-custom-content
Domain Path: /languages
License: GPL v2 or later

Easily add custom content to your WP Posts and RSS Feeds.



== Description ==

[Simple Custom Content](https://perishablepress.com/simple-custom-content/) (SCC) enables you to add custom content to all of your WP Posts and RSS Feeds. Additionally, SCC provides several shortcodes for adding custom content to individual Posts, Pages, or any location in your theme template. This plugin is ideal for adding copyright information, official policies, disclaimers, credits, thank-you messages, custom links, special offers, and anything you can imagine.

**Features**

* Custom content can be text and/or markup
* Display custom content automatically on all WP Posts
* Display custom content automatically on all RSS Feeds
* Optionally display custom content only in Post Excerpts
* Optionally display custom content only in Feed Excerpts
* Provides setting to reset all plugin options to default values
* Provides Shortcodes to add custom content to specific Posts and Pages
* Specify location of custom content (before content, after content, or both)
* NEW! Option to limit custom content to WP Posts
* NEW! Option to allow custom content on WP Pages

**Automatic Custom Content**

For each of the automatic inclusion methods (WP Posts and RSS Feeds), you can specify where you would like to display the custom content:

* Before content
* After content
* Both before and after
* Do not display (disable)

**Post-Specific Custom Content**

Here is a summary of the SCC Shortcodes, which may be used to display your custom content based on where it is viewed:

* `[scs_post]` - display custom content when post is viewed as a WP Post
* `[scs_feed]` - display custom content when post is viewed as a RSS Feed
* `[scs_both]` - display custom content when post is viewed as either Post or Feed
* `[scs_alt]`  - bonus shortcode displays content exactly where it is included

[Check out the screenshot](https://wordpress.org/plugins/simple-custom-content/screenshots/) to get a better idea of how it works.



== Installation ==

**Installation**

1. Upload the plugin to your blog and activate
2. Visit the settings to configure your options

[More info on installing WP plugins](http://codex.wordpress.org/Managing_Plugins#Installing_Plugins)


**Usage**

Visit the plugin settings to define custom content for each of these SCC Shortcodes. Then add the shortcodes to any WP Post as desired. 

For example, let's say that you want to display a copyright statement in specific posts when they are viewed via RSS Feed. First you would visit the plugin settings and define the `[scs_feed]` shortcode with your copyright message. Then when writing a post that should display the message, you would add `[scs_feed]` to the desired location (e.g., at the bottom of the post). Once the post is published, your copyright statement will be displayed whenever the post is viewed as a RSS Feed. 

Likewise with the other shortcodes, they display your custom content depending on where the post is viewed: WP Post, RSS Feed, or both. Visit the plugin settings for shortcodes and more information.


**Upgrades**

To upgrade SCC, remove the old version and replace with the new version. Or just click "Update" from the Plugins screen and let WordPress do it for you automatically.

__Note:__ uninstalling the plugin from the WP Plugins screen results in the removal of all settings from the WP database. 


**Restore Default Options**

To restore default plugin options, either uninstall/reinstall the plugin, or visit the plugin settings &gt; Restore Default Options.


**Uninstalling**

Simple Custom Content cleans up after itself. All plugin settings will be removed from your database when the plugin is uninstalled via the Plugins screen.



== Upgrade Notice ==

To upgrade SCC, remove the old version and replace with the new version. Or just click "Update" from the Plugins screen and let WordPress do it for you automatically.

__Note:__ uninstalling the plugin from the WP Plugins screen results in the removal of all settings from the WP database. 



== Screenshots ==

1. Simple Custom Content: Plugin Settings (panels toggle open/closed)

More screenshots and info available at the [SCC Homepage](https://perishablepress.com/simple-custom-content/#screenshots)



== Frequently Asked Questions ==

**How do I change the priority of the custom content filter?**

You can use the `scs_content_priority` filter hook, for example:

	function scs_custom_content_priority() { return 999; }
	add_filter('scs_content_priority', 'scs_custom_content_priority');

This can help if you want to display your custom content at the very end of the post, after any content that may be added via other plugins, etc.


**Questions? Feedback?**

Send any questions or feedback via my [contact form](https://perishablepress.com/contact/). Thanks! :)



== Support development of this plugin ==

I develop and maintain this free plugin with love for the WordPress community. To show support, you can [make a cash donation](https://m0n.co/donate), [bitcoin donation](https://m0n.co/bitcoin), or purchase one of my books:

* [The Tao of WordPress](https://wp-tao.com/)
* [Digging into WordPress](https://digwp.com/)
* [.htaccess made easy](https://htaccessbook.com/)
* [WordPress Themes In Depth](https://wp-tao.com/wordpress-themes-book/)

And/or purchase one of my premium WordPress plugins:

* [BBQ Pro](https://plugin-planet.com/bbq-pro/) - Pro version of Block Bad Queries
* [Blackhole Pro](https://plugin-planet.com/blackhole-pro/) - Pro version of Blackhole for Bad Bots
* [SES Pro](https://plugin-planet.com/ses-pro/) - Super-simple &amp; flexible email signup forms
* [USP Pro](https://plugin-planet.com/usp-pro/) - Pro version of User Submitted Posts

Links, tweets and likes also appreciated. Thanks! :)



== Changelog ==

**20170325**

* Refines display of settings panels
* Updates show support panel in plugin settings
* Replaces global `$wp_version` with `get_bloginfo('version')`
* Tests on WordPress version 4.8

**20161118**

* Added option to display custom content only on posts
* Added option to display custom content on pages
* Added `scs_content_priority` filter hook
* Refined display of plugin settings page
* Updated plugin author URL
* Changed stable tag from trunk to latest version
* Refactored `add_scs_links()` function
* Updated URL for rate this plugin links
* Removed default abbr styles
* Regenerated default language template
* Tested on WordPress version 4.7 (beta)

**20160813**

* Streamlined and optimized plugin settings page
* Replaced `_e()` with `esc_html_e()` or `esc_attr_e()`
* Replaced `__()` with `esc_html__()` or `esc_attr__()`
* Added plugin icons and larger banner image
* Improved translation support
* Removed local translations in favor of [GlotPress](https://make.wordpress.org/polyglots/handbook/tools/glotpress-translate-wordpress-org/)
* Changed text-domain from "scc" to "simple-custom-content"
* Added more allowed tags and attributes to custom content
* Generated new translation template
* Tested on WordPress 4.6

**20160409**

* Changed the WP Menu item from SCC to Custom Content
* Fixed mismatched Text Domain and domain parameters
* Added option to include custom content in feed excerpts
* Fixed bug by changing "scs_feed_none" to "scs_post_none"
* Clarified some information on the settings screen
* Clarified example text/markup for default options
* Increased the size of textareas in plugin settings
* Improved appearance of the plugin settings screen
* Replaced icon with retina version
* Added screenshot to readme/docs
* Added retina version of banner
* Reorganized and refreshed readme.txt
* Tested on WordPress version 4.5 beta

**20151111**

* Updated heading hierarchy in plugin settings
* Updated minimum version requirement
* Tested on WordPress 4.4 beta

**20150808**

* Tested on WordPress 4.3
* Updated minimum version requirement

**20150507**

* Tested with WP 4.2 + 4.3 (alpha)
* Changed a few "http" links to "https"

**20150315**

* Tested with latest version of WP (4.1)
* Increased minimum version to WP 3.8
* Renamed plugin title in WP menu
* Removed deprecated screen_icon()
* Added Text Domain and Domain Path to file header
* Added $scs_wp_vers for minimum version check
* Streamline/fine-tune plugin code
* Changed text domain from scs to scc
* Added .pot translation template in /languages/
* Added $allowedposttags to wp_kses() validation
* Exclude pages from simple_custom_content_posts()

**20140925**

* Tested on latest version of WordPress (4.0)
* Increased min-version requirement to WP 3.7
* Added conditional check for min-version function

**20140305**

* Bugfix: now using isset() for toggling admin panel custom classes, resolves PHP error "undefined index"

**20140123**

* Tested with latest version of WordPress (3.8)
* Added trailing slash to load_plugin_textdomain()
* Fixed 3 incorrect _e() tags in core file

**20131106**

* Tested with latest version of WordPress (3.7)
* General code cleanup and maintenance
* Removed closing `?>` from simple-custom-content.php
* Added line to prevent direct loading of the script
* Added uninstall.php file
* Added "rate this plugin" links
* Added i18n support

**20130713**

* General code check n clean
* Improved localization support
* Overview and Updates admin panels toggled open by default

**20130104**

* Added margins to submit buttons

**20121025**

* Refactored Authenticate plugin and renamed to Simple Custom Content

**20080629**

* Initial release of [Authenticate](https://perishablepress.com/wordpress-plugin-authenticate/)


