# TNG RSS to WordPress Post

* Contributors: natejacobs
* Tags: genealogy, rss, post
* Requires at least: 4.0
* Tested up to: 4.0
* Stable tag: 1.6
* License: GPL2

Uses the TNG-WP integration plugin to import the TNG RSS feed and create a new post for each new entry per date.

## Description

This plugin queries your The Next Generation of Genealogy Sitebuilding (TNG) RSS feed and creates a new post for each days update. The TNG RSS feed is retrieved once a day. 

There are plenty of filters and action hooks to modify the post content before the post is created. The plugin is also ready for localization.

View [this](https://gist.github.com/NateJacobs/4b126a2c850b0aa04b68) Github Gist for sample functions that take advantage of the filters to be added to the functions.php file in a theme or used in a plugin.

### Filters

The following filters are available. All the filters occur before the new post is created.

* tng_wp_rss_post_schedule - change the scheduled event frequency. Will need to use the core ````cron_schedules```` filter to add custom intervals to make the best use of this filter.
* tng_wp_rss_url - change the TNG RSS URL used to fetch content from.
* tng_wp_rss_list_class - add a class name to the unordered list element in the post content, defaults to 'list-unstyled'.
* tng_wp_rss_before_content - add any text or other content just before the list of updates is displayed in the post.
* tng_wp_rss_after_content - add any text or other content just after the list of updates is displayed in the post.
* tng_wp_rss_post_content - add anything or modify the full html of the post.
* tng_wp_rss_post_title - change the title of the post.
* tng_wp_rss_post_author_id - change the author of the post.

### Actions

The following actions are available.

* tng_wp_rss_new_post_id - the newly created post ID is passed. You could add a new category or tag or send a Tweet with the new post link.

## Installation

1. Download the plugin from Github
2. Upload `tng-wp-rss` folder to the `/wp-content/plugins/` directory
3. Activate the plugin through the Plugins menu in WordPress
