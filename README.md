# What Is W3 Total Cache

## Description

In this lesson you will learn about the benefits of using the W3 Total Cache plugin for enhancing your website's speed, and you will learn how to install and configure it properly to cover your website's needs.

* * *

## Prerequisite Skills

You will be better equipped to work through this lesson if you have experience in and familiarity with:

*   Basic knowledge of [installing and activating WordPress plugins](https://make.wordpress.org/training/handbook/user-lessons/choosing-and-installing-plugins/)

* * *

## Learning Objectives

Upon completing this lesson you should be able to:

*   Describe the benefits and possible drawbacks of using W3 Total Cache
*   Identify main W3 Total Cache's modules and explain their purpose
*   Perform starter's optimization on your site using W3 Total Cache

* * *

## Assets

*   [W3 Total Cache](https://wordpress.org/plugins/w3-total-cache/) plugin

* * *

## Screening Questions

1.  Are you familiar with the concept of a plugin in WordPress?
2.  Do you have a self-hosted WordPress website?
3.  Do you have a user role that allows you to install plugins?

* * *

## Teacher Notes

*   The recommended way to approach the scenarios would be to demonstrate and explain the process first and then ask students to repeat the actions using their own devices, while you’re available for questions and troubleshooting if something doesn’t work out.
*   It is easiest for students to work on a locally installed copy of WordPress. Set some time aside before class to assist students with installing WordPress locally if they need it or, if possible, send them out instructions before the class so they would come prepared. For more information on how to install WordPress locally, please visit our [Teacher Resources](https://make.wordpress.org/training/teacher-resources/)s page. However, you will not be able to test the speed of the site with a locally installed copy of WordPress, so it's helpful if you have access to a hosted site you can use to demonstrate to the students the speed values before and after the plugin is installed. Note - you may run into problems (unable to activate the plugin properly) when using The Bitnami WordPress stack installation with W3 Total cache.
*   The preferred answer to the screening questions is “yes.” Participants who reply “no” to question #1 might require a bit of explanation, and if they answer “no” to questions 2 & 3 they may be grouped with other students to work in pairs on the installation.
*   You may print out the Hands-On Walkthrough part to use as a handout or to send it out as a .pdf file to keep it green and preserve the links used throughout the document.
*   This lesson is meant  to serve as instruction for using W3 Total Cache for beginning webmasters and does not aspire to cover its functionality in all of the nuances. At the end of the lesson feel free to refer your students to W3 Total Cache documentation to help them fine-tune their sites.

* * *

## Hands-on Walkthrough

### What Does W3 Total Cache Do?

W3 Total Cache (W3TC) is a WordPress performance optimization framework designed to improve page speed and user experience. In more detail, using the W3 Total Cache plugin lets us benefit from **caching** - a process of storing data from previous requests to be re-used for subsequent requests. Caching prevents repeating database requests and transferring the same data over and over. It stores some of the information that has already been requested so it can be instantly served to the client. It also minimizes server load: once again, normally when a visitor comes to your site, WordPress launches MySQL queries and PHP scripts to the database to locate a requested page. Then the requested resources are parsed, and PHP generates a page to display to the visitor, taking some of the server resources. With the page caching on, you can skip all that server load and display a cached copy of the page as soon as it's requested. Additionally, W3 Total Cache helps reduce web page size by compressing it before it's actually rendered by the visitor's browser. There are several aspects caching brings to the table:

*   User experience. If web pages are loaded faster, it's more likely visitors will stay on the website. Therefore, you get a chance to increase conversion, ad revenue per thousand impressions (RPM) and generally provide a better experience for your users.
*   Search engines. Sites with the faster loading pages are better ranked by all of the search engines.

[tip]Before you begin -- if your site is accessible in the web -- it’s recommended to test your site’s productivity with such online services as [Google Page Speed](https://developers.google.com/speed/pagespeed/insights/) and/or [Pingdom Tools](https://tools.pingdom.com/) so that you can compare the results you get with what you obtain after the plugin is installed and configured.[/tip]

### Installing W3 Total Cache

Now it's time to install the W3 Total Cache plugin and activate it. Before you activate W3 Total Cache make sure all the other caching plugins are deleted. Otherwise, you will have an error when you activate W3 Total Cache. [tip]Note that it's highly recommended to make a backup of your WordPress site before you install new plugins so that you can simply roll back if something goes wrong.[/tip] [![install_w3_cache](https://make.wordpress.org/training/files/2015/12/install_w3_cache.png)](https://make.wordpress.org/training/files/2015/12/install_w3_cache.png) <span style="font-weight: 400">[tip]If you get any access errors upon activating, note that W3 Total Cache  requires that wp-content/ and wp-content/uploads/ (temporarily) have 777 permissions, e.g. for publicly available sites you can use your web hosting control panel or your FTP/SSH account in the terminal and type in: </span><span style="font-weight: 400"># chmod 777 /var/www/vhosts/domain.com/httpdocs/wp-content/</span><span style="font-weight: 400">.</span>[/tip] [tip]If you're using The Bitnami WordPress stack note it's likely it will not be compatible with W3 Total Cache. You may check out this thread if you encounter _FTP credentials don't allow to write to file/.htaccess_ error.[/tip]

### Configuring W3 Total Cache

#### W3 Total Cache Dashboard

After you’ve activated W3 Total Cache, you should be able to see a new **performance** tab in the side menu. Clicking here will take you to the W3 Total Cache **dashboard**. [![w3-total-cache-dashboard](https://make.wordpress.org/training/files/2015/12/w3-total-cache-dashboard.png)](https://make.wordpress.org/training/files/2015/12/w3-total-cache-dashboard.png) The dashboard has several blocks which can be used for the following:

1.  Check out prices for premium services (paid support, etc)
2.  Support the plugin by spreading the word, etc
3.  Integrate the plugin with the MaxCDN content delivery network to further increase site speeds
4.  Check out data on your site speed
5.  Look up statistics regarding the speed of the site via Google Page Speed

One of the main points of configuring W3 Total Cache is that different functionality is turned on and off via the **general settings** menu option and then fine-tuned via individual modules. Let's proceed to the **general settings** tab.

#### General Settings

The **general settings** tab is the main place for you to decide which modules of W3 Total Cache’s functionality you want to use. As this overview is designed for aspiring webmasters, to avoid being overwhelmed with fine-tuning the caching intricacies, we will focus on a basic subset that can benefit even the simplest of site setups.

#### Preview mode

If you want to test out W3TC before using in for the site's public version you should enable preview mode:

*   When preview mode is enabled, only the site's admin is able to view the results of applying W3TC.
*   When preview mode is disabled, which is a default setting, everyone can view and use the results of applying W3TC.

Note if you choose to enable preview mode it will stay active while you adjust the further plugin settings, until the moment you turn it off. We will leave the preview mode disabled. [![preview-mode](https://make.wordpress.org/training/files/2015/12/preview-mode.png)](https://make.wordpress.org/training/files/2015/12/preview-mode.png)

#### Page Cache

Our next option in the **general settings** tab is **page cache**. We have mentioned the way this mechanism works in the introduction. By activating page caching you ensure cache copies will be created for all of the pages, enhancing user experience and minimizing server load. [![page-cache](https://make.wordpress.org/training/files/2015/12/page-cache.png)](https://make.wordpress.org/training/files/2015/12/page-cache.png) Tick the **e****nable** checkbox for page cache. Next option - **page cache method** is set to **disk: enhanced** by default. This option depends on your server type and most likely you should proceed with **disk: enhanced** option which is suitable for most of basic hosting setups.

#### Minify

The **Minify** module controls whether HTML, CSS and Javascript files are minified and compressed. Minification characterizes by removing all unnecessary or redundant data from the code without affecting performance. This leads to website pages loading faster and generally speeds up site operation. However, you need to be really careful when setting up minification as there are a lot of parts that could potentially conflict and hinder each other's performance. For the purposes of this lesson, we will simply try the default settings as generally you need to proceed with caution when attempting minification. Let's enable minification and leave the default settings active. After that, make sure to check your website to ensure nothing was broken. [tip]It's a good idea to try enabling minification in the Preview mode.[/tip] [![minify-settings](https://make.wordpress.org/training/files/2015/12/minify-settings.png)](https://make.wordpress.org/training/files/2015/12/minify-settings.png)

##### Browser Cache

Switch to the **browser cache** tab. This is where one can configure how the visitor’s browser should handle your pages and page elements, and the amount of the information which should be cached on the client side. It’s quite an easy win in what concerns improving performance and reducing server load, so enable**browser cache** and save the settings. [![browser-cache](https://make.wordpress.org/training/files/2015/12/browser-cache.png)](https://make.wordpress.org/training/files/2015/12/browser-cache.png)

#### Further Fine-Tuning

As you see, for all of the W3TC modules there are plenty of fine-tuning options available in further menu tabs. Let's try adjusting settings for one of the options we've enabled - browser cache. Go to**browser cache** tab. Make sure it's set up as shown in the screenshot:

*   Tick Set Last-Modified header.
*   Tick Set expires header.
*   Tick Set cache control header.
*   Tick Set entity tag (eTag).
*   Tick Set W3 Total Cache header.
*   Tick Enable HTTP (gzip) compression.
*   Untick Prevent caching of objects after settings change.
*   Untick Don’t set cookies for static files.
*   Untick Do not process 404 errors for static objects with WordPress.

Save the settings. [![browser-cache-general-setting](https://make.wordpress.org/training/files/2015/12/browser-cache-general-setting.png)](https://make.wordpress.org/training/files/2015/12/browser-cache-general-setting.png)

#### Other Modules

This lesson is meant  to serve as an instruction for using W3 Total Cache for beginning webmasters and does not aspire to fully cover its functionality in all of the nuances, and it is important to proceed slowly when you are first getting to grips with it. However, we'll sure provide a brief overview of the other options so that you would know what else is there. Let's quickly overview the other modules:

*   **Database cache** is meant to speed up interactions with the MySQL database. However, W3 Total Cache’s official installation guidelines point out that for shared server hosting setups it might be not efficient, so it makes sense to test this feature in isolation to be able to judge its effectiveness.
*   **Object cache** involves dynamic objects caching and further reduction of time required for further operation. It’s also not recommended when using shared server hosting. However, you may look into it when you’re using a dedicated server and your site has a lot of dynamic objects.

[tip]It may sound weird that some of the caching options the plugin offers should actually be avoided - let’s go into some for detail to find out why. The main idea behind caching is increasing speed by storing data that is slow to generate in a place that’s quicker to access. However, most shared server hosting are providing database and object reads from extremely fast solid-state drives, and when you enable database or object caching to disk, the disks that W3 Total Cache will save the data to are spinning disks, which are much slower compared to solid-state drives. So it’s actually faster to generate data again, not store it.[/tip]

*   **User agent groups**  - this section enables management of user agent groups. It's active by default. The typical use case for applying it would be redirecting a specific group - visitors using a mobile device - to a third party site which is providing the mobile version of your site.
*   **Referrer groups** support is also enabled by default. Referrer groups are about search engines or other sites that are sending significant amounts of traffic to your site. You can assign a set of referrers to see a specific theme, redirect them to another domain and ensure that a unique cache is created for each referrer group.
*   **CDN** stands for Content Delivery Network. A CDN is a network of servers, usually located at various sites around the world. These powerful servers can cache the static content of a site, such as image, CSS and JavaScript files, and when a visitor lands on your site, the content is provided by the server closest to their location. If you’re signed up with a CDN you can integrate it together with W3TC plugin.

#### Importing and Exporting W3TC settings

In this section, you may export or import W3TC settings to make sure all your hard work fine-tuning the plugin is preserved. Click **download** button to download W3TC configuration. After that, to test it out you may **restore default settings**, make sure all the settings are reverted back and then import the configuration file you have just downloaded. [![import_export](https://make.wordpress.org/training/files/2015/12/import_export.png)](https://make.wordpress.org/training/files/2015/12/import_export.png) [tip]If your site is publicly accessible, and you had a chance to test your site’s productivity with [Google Page Speed](https://developers.google.com/speed/pagespeed/insights/) or [Pingdom Tools,](https://tools.pingdom.com/) do it once again now to compare the results.[/tip]

#### Conclusion

Overall, W3 Total Cache enables beginner WordPress webmasters to reap its major benefits easily by enabling page and browser caching, while also allowing the experts a plethora of advanced fine-tuning options. For someone who just begins optimizing their sites, the following algorithm should be used:

<div class="shortcode-list">

1.  Install and activate W3 Total Cache.
2.  Enable page caching and browser caching.
3.  Be cautious when fine-tuning and testing minification.
4.  Compare your before and after results :)

</div>

* * *

## Alternatives

There are other caching plugins out there - some of the most popular alternatives are [W3 Super Cache](https://wordpress.org/plugins/wp-super-cache/), which has a bit fewer options to customize so may feel less overwhelming and [WP Rocket](http://wp-rocket.me/), which is an efficient but quite simple premium plugin.

* * *

## Quiz

**Which of the following are among the benefits caching brings to the table? (select 2 answers)**

1.  Improves security
2.  Decreases page loading speed
3.  Decreases server load
4.  Makes the website design to look better
5.  Attracts more visitors

**Answer:** 2. Decreases page loading speed & 3. Decreases server load 

<hr>

**Which of the following best describes minification?**

1.  Compressing the web pages' data
2.  Removing all unnecessary data from the code without affecting performance
3.  Increasing speed by storing data that is slow to generate in a place that’s quicker to access

**Answer:** 2. Removing all unnecessary data from the code without affecting performance 

<hr>

**Do you need to keep W3TC activated to reap its benefits?**

1.  Yes
2.  No, it can be deactivated after the initial setup

**Answer:** 1. Yes    

* * *

## Additional Resources

1.  Official W3 Total Cache [FAQ](https://wordpress.org/plugins/w3-total-cache/faq/)
2.  [Advanced W3 total cache tutorial](https://theme-fusion.com/advanced-w3-total-cache/) @ https://theme-fusion.com/advanced-w3-total-cache/
