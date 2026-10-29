=== Custom links in Elementor Image Carousel (HackIndex Patched) ===
Contributors: charlieetienne, joshuavanderpoll
Tags: elementor, image carousel, custom links
Stable tag: 1.1.2
Requires at least: 5.2
Tested up to: 7.1
Requires PHP: 7.2
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html
Donate Link: https://paypal.me/webnancy

Lets you add custom links in Elementor Image Carousel widget (HackIndex Patched)

== Description ==

= HackIndex Patched fork =
This is an unofficial fork of Custom links in Elementor Image Carousel by Charlie Etienne. The original plugin is no longer maintained and its latest release (1.1.1) has a [known vulnerability](https://www.wordfence.com/threat-intel/vulnerabilities/id/53880f49-a2f0-4864-ba85-8fbf06ea7833). HackIndex maintains this fork for security fixes only.

* We fix security issues and keep the plugin working on current WordPress and PHP versions. We do not add features or change how the plugin works.
* It is a drop-in replacement: the custom links and "Open in new tab" settings on your images keep working.
* HackIndex is not affiliated with or endorsed by Charlie Etienne. Please do not contact the original author for support with this fork, open an issue on the fork instead.
* Original plugin: [WordPress.org](https://wordpress.org/plugins/custom-links-in-elementor-image-carousel/) and [GitHub](https://github.com/CharlieEtienne/custom-links-in-elementor-image-carousel) by Charlie Etienne.
* HackIndex fork and issues: [github.com/HackIndex-io/custom-links-in-elementor-image-carousel](https://github.com/HackIndex-io/custom-links-in-elementor-image-carousel)
* Licensed under the GPLv2 or later, like the original, and provided without any warranty.

There is a WordPress limitation (no custom link on images) that makes impossible to add custom links on each image in an image carousel or image gallery like the one in Elementor free version. 

This plugin just overrides WordPress attachment fields and Elementor Image Carousel widget to let you add custom links to each image in the carousel.
Basically, it adds two custom fields to each image in WordPress Media Library (Custom link and "Open in new tab?" checkbox).
Then it hooks into elementor image carousel widget just before it's rendered on frontend.

== Usage & Documentation ==

No options, no premium version, no bullshit. Just activate or deactivate.

**Note:** You have to enable the option “Link” in the Elementor Image Carousel widget and set it to: “Media Files” in order for it to work.

= Resources =

* **WordPress Plugin:** [https://wordpress.org/plugins/custom-links-in-elementor-image-carousel](https://wordpress.org/plugins/custom-links-in-elementor-image-carousel)
* **GitHub Repository:** [https://github.com/CharlieEtienne/custom-links-in-elementor-image-carousel](https://github.com/CharlieEtienne/custom-links-in-elementor-image-carousel)
* **Support:** [https://github.com/CharlieEtienne/custom-links-in-elementor-image-carousel/issues](https://github.com/CharlieEtienne/custom-links-in-elementor-image-carousel/issues)

== Installation ==

1. Install this plugin either via the WordPress.org plugin directory, or by uploading the files to your server.
2. Activate the plugin.
3. That's it. You're ready to go! Please, refer to the Usage & Documentation section for examples and how-to information.

== Frequently Asked Questions ==

= Is this plugin completely free? =
Yes.

= Can I use this plugin for commercial purposes? =
Sure, go ahead! It is completely open source.

== Screenshots ==

1. Custom fields on images in Media Library

== Changelog ==

= 1.1.2 =
* Security: fixed Author+ stored Cross-Site Scripting ([CVE-2026-65534](https://www.cve.org/CVERecord?id=CVE-2026-65534), [Wordfence advisory](https://www.wordfence.com/threat-intel/vulnerabilities/id/53880f49-a2f0-4864-ba85-8fbf06ea7833)) by sanitizing the custom link on save and escaping the link and target in the carousel
* Fixed PHP warnings when saving an image without the custom link fields
* Tested with WordPress 7.1, Elementor 4.3 and PHP 8.5

= 1.1.1 =
* Fix fatal errors in some edge cases

= 1.1.0 =
 * Move to Singleton pattern to let other developpers unhook actions or filters

= 1.0.1 =
 * Fixes "Open in new tab" option. It's now possible to uncheck this setting
 * Improve docs