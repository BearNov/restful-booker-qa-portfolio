# Application Exploration

## Application

**Name:** Restful Booker Platform
**URL:** https://automationintesting.online/

## Exploration Objective

Understand the application's main features, user flows, inputs, and expected outcomes before creating formal test cases.

## Main Areas to Explore

### 1. Homepage and Navigation

**What the feature appears to do:**

The homepage presents the bed-and-breakfast service and provides navigation to the main customer-facing sections, including rooms, booking, amenities, location, contact information, and the administration login page.

**Available actions:**

- Clicking the logo in the upper-left corner returns the user to the homepage.
- Clicking the hamburger menu opens and closes the navigation menu.
- Clicking Rooms scrolls to the Our Rooms section.
- Clicking Booking also scrolls to the Our Rooms section.
- Clicking Amenities changes the URL, but no visible page movement or content change occurs.
- Clicking Location scrolls to the location and contact-information section.
- Clicking Contact scrolls to the contact form.
- Clicking Admin opens the administration login page.
- Clicking Book Now in the hero section scrolls to the Our Rooms section.
- The footer contains quick links, policy links, contact information, and a link to the administration panel.
- The Cookie Policy and Privacy Policy links open their respective pages.
- The Admin Panel footer link opens the same administration page as the main navigation link.

**Questions or unclear behaviour:**

- Is the Amenities link intended to scroll to an amenities section that is currently missing or inaccessible?
- Should the Booking link open a dedicated booking section instead of the general rooms section?
- The footer links for Home, Rooms, Booking, and Contact all appear to return to the hero section. Should each link navigate to its corresponding section?
- Should a Logout button be visible on the administration page before the user has successfully logged in?

---

### 2. Room Listings and Details

**What the feature appears to do:**

The **Our Rooms** section displays available rooms and allows users to open a detailed page for an individual room before starting the reservation process.

**Available actions:**

* Three room cards are displayed in the **Our Rooms** section.
* Each room card includes an image, title, description, amenities, price per night, and a **Book Now** button.
* Clicking **Book Now** opens the corresponding room-detail page.
* The room-detail page allows the user to browse dates using the **Today**, **Back**, and **Next** buttons.
* The user can select reservation dates and continue by clicking **Reserve Now**.
* The **Similar Rooms You Might Like** section provides links to other room-detail pages.

**Inputs:**

* Check-in and checkout dates selected through the calendar.
* Room selection through the room cards or similar-room recommendations.

**Expected user outcome:**

The user should see accurate information about the selected room, including its price, guest capacity, features, policies, available dates, calculated charges, and reservation controls.

**Room comparison:**

| Detail          | Single Room    | Double Room     |
| --------------- | -------------- | --------------- |
| Price per night | £100           | £150            |
| Maximum guests  | 2              | 2               |
| Features        | TV, WiFi, Safe | TV, Radio, Safe |

**Information displayed on the room-detail page:**

* Room title and image
* Accessibility information
* Maximum number of guests
* Room description and features
* Check-in and checkout information
* House rules
* Price per night
* Booking calendar
* Cleaning fee
* Service fee
* Total reservation price
* **Reserve Now** button
* Similar-room recommendations
* Footer navigation

**Questions or unclear behaviour:**

* Clicking **Rooms** in the breadcrumb adds `#` to the URL, but no navigation or scrolling occurs.
* Should the breadcrumb return the user to the **Our Rooms** section?
* Are the displayed price calculations updated correctly for every selected date range?
* Why do some room images or amenity icons appear to change after returning to the homepage?

---

### 3. Availability Search

**What the feature appears to do:**

The **Check Availability** section allows users to enter check-in and checkout dates before viewing the available rooms.

**Inputs:**

* Check-in date
* Checkout date
* **Check Availability** button

**Expected user outcome:**

The application should validate the selected date range and display rooms that are available for the requested stay.

The checkout date should be later than the check-in date, and past dates should not be accepted for a new reservation.

**Observed behaviour:**

* The default check-in date was **24/06/2026**.
* The default checkout date was **25/06/2026**.
* Three room cards were already displayed before performing a search.
* Clicking **Check Availability** scrolled the page to the **Our Rooms** section.
* A valid future range from **25/06/2026 to 27/06/2026** was accepted, but the displayed rooms did not change.
* A second valid future range from **01/07/2026 to 03/07/2026** produced the same result.
* The same check-in and checkout date, **25/06/2026**, was accepted without validation.
* A checkout date earlier than the check-in date, **25/06/2026 to 24/06/2026**, was accepted without validation.
* A past date range, **22/06/2026 to 23/06/2026**, was accepted without validation.
* No error messages or availability messages were displayed for any of the tested date ranges.
* The same three room cards remained visible after each search.

**Questions or unclear behaviour:**

* Should the availability search filter the displayed rooms according to the selected dates?
* Why are invalid date ranges accepted without validation?
* Should same-day bookings be allowed?
* Should past dates be disabled in the date picker?
* Should the user receive a message confirming whether rooms are available?

---

### 4. Booking Form

**What the feature appears to do:**

**Inputs:**

**Expected user outcome:**

**Questions or unclear behaviour:**

---

### 5. Contact Form

**What the feature appears to do:**

**Inputs:**

**Expected user outcome:**

**Questions or unclear behaviour:**

---

### 6. Responsive Behaviour

**What was checked:**

**Observed behaviour:**

**Questions or unclear behaviour:**

## General Notes

*
