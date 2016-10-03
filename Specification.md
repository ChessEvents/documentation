## Chess Events Ltd
### Functional Specification
##### Matthew D Webb
Last updated 3rd October 2016

### Overview

Chess Events Ltd is a software service which aims to improve the efficiency, accessibility and management of Chess events played in the United Kingdom.

This specification is not, by any means, complete. Most of the wording will be revised several times before it is finalised. The graphics and layout of the wireframes shown here merely illustrate the underlying functionality. The actual look and feel will be developed over time with the input of graphics designers and iterative user feedback.

This specification does not discuss the algorithms or business logic used within the Chess Events API, Mobile or Web Application, all of these will be discussed elsewhere. It simply discusses what the user sees when they interact with the application through chessevents.co.uk

### Scenarios

In designing products, it helps to imagine a few real life stories of how actual (stereotypical) chess players would use them. We'll look at four scenarios.

**Scenario 1**: Frequent Player "Joe"

Joe regularly enters chess events all across the country, he picks up entry forms for future events at many of the events he attends. Joe usually plays the same events year in year out and has a good grasp for when these are held and where they're being played.

Joe is likely to miss new opportunities or last minute changes to events unforeseen by the organiser (currently organiser can only inform players by telephone or by post).

Through Chess Events, Joe can favourite the events he regularly attends, this automatically him reminders a few weeks before the event so he doesn't forget.  Joe and other players taking part are notified instantly of any changes to these events, the severity of these changes are highlighed in the notification. 

Joe can now view new events, especially if his old event is cancelled and the new event in it's place so he doesn't miss out or need a paper entry form to participate.

**Scenario 2**: New To Chess "Charlotte"

Charlotte enjoyed playing chess when she was at school but hasn't thought much about it since. Charlotte is completely unaware of the chess events regularly taking place in her area.

Through the Chess Events mobile app, Charlotte can quickly and easily see what events are taking place but more importantly, when and where. Not only this but a quick message directly to the organiser Charlotte can be put at ease having never played in a "proper" tournament and doesn't know what a grade is (which demanded on existing paper entry forms).

**Scenario 3**: Keen Organiser "Jess"

Jess was never very good at chess but has always loved getting involve with organising, especially new events. Every time Jess has tried to find any information about this using Google, or asking other members of the chess community, she has been met with an overwelming list tasks from members but no official documentation from any governing body.

Through the Chess Events web and mobile app Jess delved into the details of organising an event. She quickly and easily defined the criteria of her first tournament, the number of rounds; time limit and the number of sections. Jess was also able to plan her event to avoid any clashes with other events in the calendar. Jess asked for advice from the other organisers (registered on Chess Events) and was able to get in touch with venues where events have previously been held to book hers.

**Scenario 4**: Tech Phobe "Richard"

Richard has organised chess events for nearly 20 years, he knows everything there is to know about running a successful congress but, despite his best efforts to improve things over the last few years, entries have been consistently falling year on year.  

Richard doesn't know much about computers and admits he struggles to keep on top of his emails when players send in their queries, especially about payment including late fees and discounts.

Through Chess Events Richard created all of his events recursively year significantly reducing his yearly admin. Not only this but Richard set up a payment method to allow players to enter his prestigious events, automatically adjusting for late payment fees and member discounts.

Richard busies himself with the more important aspects of event organisation, preparing the facilities to accommodate the players (chess sets, clocks, arbiters etc). Richard is happy Chess Events are busy promoting and sharing his event on social media, notifying existing users of these events and encouraging new players to come along.

### Non Goals

Our initial intentions are to stay clear of the following areas:

##### Grading / Rating System

There are already two primary systems in operation in the UK, these are:

* The English Chess Federation Grade -  [view](http://www.ecfgrading.org.uk/new/menu.php)
* The FIDE International Rating (based on the Elo Rating System) - [view](https://ratings.fide.com/)

These systems are well established an suitably maintained which provide a reliable reference for players and organiser to accurately determine playing strength in relation to others.

Although there are no immediate plan to build a bespoke system for tracking players performance, Chess Events will use both systems mentioned in order to provide a more detailed profile, this will aid both  the organisers (for players entering their events), and the players themselves to view their performance.

##### Tournament Results Tracking

Again, there are a number of systems in operation which offer tournament organisers a reliable solution to manage tournament participation and performance calculations.

* Swiss Perfect - [view](http://www.swissperfect.com/)
* Vega Chess [view](http://www.vegachess.com/tl/index.php/Home_page_English.html)

Chess Events aims to provide a more seamless intregration with all third party tournament tracking systems. This offers two significant benefits to the chess community:

1. Improved efficiency for the organisers - entries to their events are tracked through a single platform allowing a consistent download of entry data into the format pre formatted for the tournament software of their choice.
2. Reduced human error - as the downloaded data is verified with the official rating / grading systems(s) the unique player ids and format of the data will vastly reduce human errors for result publication.

### Screen by Screen Specification

**Landing Page**

* Allow users download the mobile app (both iOS and Android)
* Allow users to sign in to the web app
    * This will redirect the user to the web application for sign in.
* Allow new users to sign up
    * This will redirect the user to the web application registration page.
* Allow users to see a list of featured events
* Allow users to see an overview of the key features offered by Chess Events.

The Chess Events application is split into two primary functions in order to deliver tailored features to both mobile and desktop users:

**Web Application**

To view the web application users must be signed in. Users who are not signed in will automatically be redirected to the "sign in / create account page".

When the user is signed in:

* Home page
    * Search for events
    * View featured events
    * View upcoming events
    * View favourited events
    * See a list of notifications (link to their inbox)
* Profile page
    * View and Edit profile basic details:
         * Username / Email / Address / Grade / Rating / Profile imagine
    * View list of upcoming entered events
    * View list of favourites
    * View list of events played (pending review)
    * Notification inbox
    * Sign out
    * Become and organiser(!)
        * More info
        * Create organiser profile
    * Delete profile
* Event Calendar
    * View a list of events in date order, grouped by month
    * View events by type (Rapid play, Standard, Swiss, etc)
    * Filter events based on data, type criteria
* Event
    * View details of the event:
        * Dates / Location
        * Facilities
        * Previous Years Reviews
        * Price / How to Enter / Submit Entry
        * Event Parameters (sections / format)
        * View entries
* Organiser
    * Create a profile
         * View events created
         * View entries into event(s)
         * Download player entry details
         * Send notifications to entered player(s)     

**Mobile Application**

To view the mobile applications, users must download the app from either the Apple App store or the Google Play store. Once downloaded users can login (with their existing details) or create an account.

When the user is signed in:

* Home page
    * View featured events
    * View upcoming events
    * swipe left menu
* Left menu
    * Link - "View featured events"
    * Link - "My events"
    * Link - "My profile"
* Profile page
    * View and Edit profile basic details:
         * Username / Email / Address / Grade / Rating / Profile imagine
    * View list of upcoming entered events
    * View list of favourites
    * View list of events played (pending review)
    * Notification inbox
    * Sign out
    * Delete profile
* Event Calendar
    * View a list of events in date order, grouped by month
    * View events by type (Rapid play, Standard, Swiss, etc)
    * Filter events based on data, type criteria
* Event
    * View details of the event:
        * Dates / Location
        * Facilities
        * Previous Years Reviews
        * Price / How to Enter / Submit Entry
        * Event Parameters (sections / format)
        * View entries
