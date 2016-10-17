# Chess Events Ltd

<img src="./images/chessevents.png?raw=true" width="100" />

## Functional Specification

### Matthew D Webb

Last updated 17th October 2016

## Overview

Chess Events Ltd is a software service which aims to improve the efficiency, accessibility and management of events relating to chess carried out in the United Kingdom.

This specification is not, by any means, complete. Most of the wording will be revised several times before it is finalised. The graphics and layout of the wireframes shown here merely illustrate the underlying functionality. The actual look and feel will be developed over time with the input of graphic designers and iterative user feedback.

This specification does not discuss the algorithms or business logic used within the Chess Events API, Mobile or Web Application, all of these will be discussed elsewhere. It simply discusses what the user sees when they interact with the application through chessevents.co.uk

## Scenarios

In designing products, it helps to imagine a few real life stories of how actual (stereotypical) chess players would use them. We'll look at four scenarios.

**Scenario 1**: Frequent Player "Joe"

Joe regularly enters chess events all across the country, he picks up entry forms for future events at many of the events he attends. Joe usually plays the same events year in year out and has a good grasp for when these are and where they're being held.

Joe is likely to miss new opportunities or more critically not be informed of last minute changes to events unforeseen by the organiser. Currently organisers can only inform players by telephone, by post or email (if provided on the entry form) this is an ineffective means of urgent communication, time consuming and potentially costly.

Through Chess Events Joe was able to 'Favourite' the events he regularly attends. This favourites automatically reminds him before the event begins so he doesn't forget to enter or incur a late fee! Joe and other players taking part benefit from being notified instantly of any changes to events, particularly the date, as some venues are prone to double book and reschedule their event for later or earlier in the season. The severity of these changes are highlighted to the players so they are always in the know and can plan their travel accordingly.

Joe now regularly views new events, especially in place of cancellation or rescheduled events, he no longer needs to pick up a paper entry forms or send cheques in the post to participate in those events. He is also notified of events which are likely to be of interest to him, these are chosen specifically for him when taking into account the events he already enters, where is lives and how far on average he is willing to travel.

**Scenario 2**: New To Chess "Charlotte"

Charlotte enjoyed playing chess when she was at school but since leaving school and starting her career, she hasn't thought much about chess since. Charlotte is completely unaware of the chess events which are regularly taking place in and around her local area.

Through the Chess Events mobile application, Charlotte is able to quickly and easily see what events are taking place, with simple filters she can narrow down the events closest to her, see when these take place and how to entry. Not only this but with the ability to contact the organiser directly, Charlotte is reassured especially having never played in an adult tournament previously.

NB. New players are usually confused by entry forms which ask for a "grade" or "indication of playing strength". Opening up direct and easy assess to the official tournament organisers, together with a concise list of FAQs new players are able to comfortably take part in any event.

**Scenario 5**: Tech Phobe "Richard"

Richard has organised chess events for almost 20 years, he knows everything there is to know about running a successful congress but, despite his best efforts to improve things over the last few years, entries have been consistently falling year on year.

Richard doesn't know much about computers and admits he struggles to keep on top of his emails when players send in their queries, especially about payment including late fees and discounts.

Through Chess Events Richard created all of his events recursively, providing all answers to common queries this significantly reducing his yearly admin. Not only this but Richard set up a payment method to allow players to enter his prestigious events directly online, this automatically accounted for late payment fees and member discounts.

Richard now focuses on the other aspects of event organisation, the parts he most enjoys; preparing the facilities to accommodate the players (chess sets, clocks, arbiters, refreshments, etc). Richard allows Chess Events to promote and share his events on social media as well as notify existing users of these events and encouraging new players to come along.

**Scenario 4**: Keen Organiser "Jess"

Jess was never particularly talented in chess but has always loved getting involved with the organising aspects, especially new events. Every time Jess has tried to find any information about this using internet search engines, such as Google, or by asking other members of the chess community, she has been met with an overwhelming list of tasks from members but no official documentation from any governing body.

Through the Chess Events web and mobile application Jess delved into the details of organising an event without any hinderance. She quickly and easily defined the criteria of her first tournament, the number of rounds; the time limit and the number of sections. Jess was also able to plan her event to avoid any clashes with other in the calendar. Not only this but Jess received advice and praise from the other organisers within the app and was able to get in touch with venues where events have previously been held.

## Non Goals

Our initial intentions are to stay clear of the following areas, reasons and future possibilities are discussed below.

### Grading / Rating System

There are two existing systems in operation in the UK, these are:

- The English Chess Federation Grade - [view](http://www.ecfgrading.org.uk/new/menu.php)
- The FIDE International Rating (based on the [elo rating system](https://en.wikipedia.org/wiki/Elo_rating_system)) - [view](https://ratings.fide.com/)

These systems are well established and suitably maintained, they provide a reliable reference for players and organisers to accurately determine playing strength in relation to others.

Although there are no immediate plans to build a bespoke service for tracking players performance, Chess Events will use both systems mentioned in order to provide a more detailed player profile, this will aid both the organiser (for players entering their events), and the player (when viewing their individual performance via their profile page).

In order for players to attain a grade or rating players are required to be members of the [English Chess Federation](http://www.englishchess.org.uk/membership/joining/guide-to-joining-the-ecf/). Furthermore, for players to attain an International rating, a higher membership band is required.

### Tournament Tracking

There are a number of systems in operation which offer tournament organisers a reliable solution to manage tournament participation and performance calculations.

- Swiss Perfect - [view](http://www.swissperfect.com/)
- Vega Chess - [view](http://www.vegachess.com/tl/index.php/Home_page_English.html)

Chess Events aims to provide seamless integration between the main third party tournament tracking systems. This offers two significant benefits to the chess community:

1. Improved efficiency for the organisers - entries to their events are tracked through a single platform allowing a consistent download of entry data into the format specifically prepared for the tournament software of their choice.
2. Reduced human error - as the downloaded data is verified with the official rating / grading systems(s) the unique player ID's and correct formatting of the data will vastly reduce human errors ready for publication.

Although there are no plans for Chess Events to develop tournament management software, it may in future be important to maintain a list of tournament results, this would be to enhance the data of previously held events, offering a more detailed reflection of future events and allowing players easy access to their performance across events beyond individual game by game results.

### Result Publication

This is perhaps the most challenging of tasks, it is expected that our users will wish to see specific feedback from events they enter through Chess Events.

The major provider for results online is:

- Chess-Results.com - [view](http://www.chess-results.com/)

Our aim therefore is to compliment this software by providing as above, a seamless integration path in order for organisers to publish their results on both platforms. A concise view will be provided on Chess Events and the detailed breakdown remaining on Chess-Results.

## Screen by Screen Specification

**Landing Page**

- Allow users to download the mobile app (both iOS and Android)
- Allow users to sign in to the web app

  - This will redirect the user to the web application for sign in.

- Allow new users to sign up

  - This will redirect the user to the web application registration page.

- Allow users to see a list of featured events
- Allow users to see an overview of the key features offered by Chess Events.

The Chess Events application is split into two primary functions in order to deliver tailored features to both mobile and desktop users:

**Web Application**

To view the web application users must be signed in. Users who are not signed in will automatically be redirected to the "sign in / create account page".

<img src="./images/landing-wireframe.png?raw=true" width="500" />

When the user is signed in:

- Home page

  - Search for events
  - View featured events
  - View upcoming events
  - View favourited events
  - See a list of notifications (link to their inbox)

- Profile page

  - View and Edit profile basic details:

    - Username / Email / Address / Grade / Rating / Profile image

  - View list of upcoming entered events
  - View list of favourites
  - View list of events played (pending review)
  - Notification inbox
  - Sign out
  - Become and organiser(!)

    - More info
    - Create organiser profile

  - Delete profile

- Event Calendar

  - View a list of events in date order, grouped by month
  - View events by type (Rapid play, Standard, Swiss, etc)
  - Filter events based on data, type criteria

- Event

  - View details of the event:

    - Dates / Location
    - Facilities
    - Previous Year's Reviews
    - Price / How to Enter / Submit Entry
    - Event Parameters (sections / format)
    - View entries

- Organiser

  - Create a profile

    - View events created
    - View entries into event(s)
    - Download player entry details
    - Send notifications to entered player(s)

**Mobile Application**

To view the mobile applications, users must download the app from either the Apple App store or the Google Play store. Once downloaded users can login (with their existing details) or create an account.

<img src="https://github.com/ChessEvents/documentation/blob/master/images/iphone-home-screen.png?raw=true" width="120" align="right" />

When the user is signed in:

- Home page

  - View featured events
  - View upcoming events
  - swipe left menu

- Left menu

  - Link - "View featured events"
  - Link - "My events"
  - Link - "My profile"

- Profile page

  - View and Edit profile basic details:

    - Username / Email / Address / Grade / Rating / Profile image

  - View list of upcoming entered events
  - View list of favourites
  - View list of events played (pending review)
  - Notification inbox
  - Sign out
  - Delete profile

- Event Calendar

  - View a list of events in date order, grouped by month
  - View events by type (Rapid play, Standard, Swiss, etc)
  - Filter events based on data, type criteria

- Event

  - View details of the event:

    - Dates / Location
    - Facilities
    - Previous Year's Reviews
    - Price / How to Enter / Submit Entry
    - Event Parameters (sections / format)
    - View entries
