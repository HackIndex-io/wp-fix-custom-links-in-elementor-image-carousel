# Custom links in Elementor Image Carousel (HackIndex Patched)

> [!IMPORTANT]
> This is an unofficial fork of [Custom links in Elementor Image Carousel](https://wordpress.org/plugins/custom-links-in-elementor-image-carousel/) by [Charlie Etienne](https://github.com/CharlieEtienne/custom-links-in-elementor-image-carousel). HackIndex is not affiliated with or endorsed by the original author.

The original plugin is no longer maintained and its latest release (1.1.1) has a [known vulnerability](https://www.wordfence.com/threat-intel/vulnerabilities/id/53880f49-a2f0-4864-ba85-8fbf06ea7833). HackIndex maintains this fork for security fixes only:

- We fix security issues and keep the plugin working on current WordPress and PHP versions.
- We do not add features or change how the plugin works.
- It is a drop-in replacement: same plugin folder and meta fields, so the custom links on your images keep working.

Need help with this fork? [Open an issue](https://github.com/HackIndex-io/custom-links-in-elementor-image-carousel/issues) here, please don't contact the original author about it.

## What it does

Adds a "Custom link" and "Open in new tab?" field to every image in the Media Library, and uses that link for the image in the Elementor Image Carousel widget. No options, just activate it.

## Security fixes

### 1.1.2

- Author+ stored Cross-Site Scripting ([CVE-2026-65534](https://www.cve.org/CVERecord?id=CVE-2026-65534), [Wordfence advisory](https://www.wordfence.com/threat-intel/vulnerabilities/id/53880f49-a2f0-4864-ba85-8fbf06ea7833)): the custom link was saved and printed in the carousel without any sanitizing, so an author could add a `javascript:` link or break out of the `href` attribute. The link is now sanitized on save and escaped on output, which also neutralizes links that were stored before the update.
- Fixed PHP warnings when saving an image without the custom link fields
- Tested with WordPress 7.1, Elementor 4.3 and PHP 8.5

## Install

1. Download `custom-links-in-elementor-image-carousel.zip` from the [latest release](https://github.com/HackIndex-io/custom-links-in-elementor-image-carousel/releases/latest).
2. Upload the zip in **Plugins > Add New > Upload Plugin** and choose **Replace current with uploaded**. The links on your images are kept.
3. Don't delete the original plugin first: deleting a plugin can run its uninstall and remove its settings.

WordPress does not update this fork automatically. Watch this repo's releases to get new security fixes.

## License

GPLv2 or later, like the original. See [LICENSE.txt](LICENSE.txt). Provided without any warranty.

All credit for the plugin goes to [Charlie Etienne](https://github.com/CharlieEtienne/custom-links-in-elementor-image-carousel). The full upstream history is kept in this repository.
