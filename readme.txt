=== Plugin Name ===
Contributors: mbjacket81
Donate link: http://smartwaredesign.com/donate
Tags: google calendar combiner, combine google calendars, google calendar, combine calendar
Requires at least: 3.0.1
Tested up to: 4.8
Stable tag: 4.8
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Wordpress Plugin for combining public Google Calendars for display, created by SmartwareDesign.com for use by everyone!

== Description ==

The user can combine multiple public Google calendars into one feed to use on the REST API or generate one agenda calendar on the Wordpress frontend.

The user can have multiple combined calendars to use on different API calls or front end views with different shortcodes.  This plugin allows the user to enter a list of all public Google Calendars, the number of look-ahead days, and the timezone for displaying the dates and times of the calendar.

The RESTful call generates JSON that looks like the following as an example:
{
 'date':'2016-03-31',
 'events':[
   {'title':'Mayor&#39;s Masters Reception',
    'link':'https://calendar.google.com/calendar/event?eid=X2Q...&ctz=America/New_York'},
   {'time':'10am',
    'title':'AARP Tax Help', 
    'link':'https://calendar.google.com/calendar/event?eid=aWwy...&ctz=America/New_York'}
  ]
}

The RESTful call can be made by using a custom url to:
<your base wordpress site url>/wp-json/sd-google-calendar/v1/sdcalendar/<post ID>

The agenda calendar can be inserted to your wordpress post using the shortcode:
[sd_show_calendar id="<cal id>"]

There's also a "type" parameter which is defaulted to "agenda" for now but will be further developed to eventually use full calendar displays for scrolling different months.

== Installation ==

1. Upload the plugin files to the `/wp-content/plugins/sd-google-calendar` directory, or install the plugin through the WordPress plugins screen directly.
1. Activate the plugin through the 'Plugins' screen in WordPress
1. Use Google Calendars admin menu option for setting up combined calendars.


== Frequently Asked Questions ==

= Can I use a private calendar? =

At the moment, no.  It's not configured to use the Google API so it can't use private calendars.

= What about calendar-type displays? =

Right now only an agenda-style format is available.  If there's a strong desire to have a calendar layout then we will consider this in future versions.

= What about using my own calendar styles? =

The calendar CSS styles are located in the plugin /css folder

== Screenshots ==

1. The list of combined calendars (you can have multiple combined calendars to place on different pages or posts).
2. The edit screen for each individual combined calendar (# calendar items to pull down, timezone, and calendar ids).
3. An example post with a combined calendar.

== Changelog ==

= 1.0.1 =
* Updated version to 4.7
= 1.0 =
* The initial version includes WP REST API and Agenda layout

== Upgrade Notice ==

= 1.0 =
No Upgrade notice for the initial version.

= 1.1 =
Corrected the problems happening with recent Google Calendar updates.  Agenda now displays with latest version and works with WordPress 4.8