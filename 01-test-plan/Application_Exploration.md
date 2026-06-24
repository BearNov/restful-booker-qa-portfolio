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

The booking process allows the user to select reservation dates, review the price calculation, enter guest information, and submit a room reservation.

**Inputs:**

* Check-in date
* Checkout date
* First name
* Last name
* Email address
* Phone number
* **Reserve Now** button

**Expected user outcome:**

The application should validate the selected dates and guest information, clearly display the reservation details, prevent duplicate bookings, and show a confirmation after a successful reservation.

**Observed behaviour:**

* The **Single Room** was selected for **28/06/2026–30/06/2026**.
* The price summary correctly displayed:

  * Room cost: **£200**
  * Cleaning fee: **£25**
  * Service fee: **£15**
  * Total: **£240**
* Clicking **Reserve Now** replaced the booking-calendar section with a guest-information form.
* The form contained fields for first name, last name, email, and phone number.
* No visible required-field indicators were shown.
* The selected dates were no longer visible after opening the guest-information form.
* The price summary remained visible.

**Empty submission:**

Submitting the form with all fields empty was blocked.

The following validation messages were displayed together in one combined area:

* `must not be empty`
* `size must be between 3 and 18`
* `size must be between 3 and 30`
* `must not be empty`
* `Lastname should not be blank`
* `size must be between 11 and 21`
* `Firstname should not be blank`

**Invalid submission:**

The following values were tested:

* First name: `A`
* Last name: `B`
* Email: `invalid-email`
* Phone: `123`

The reservation was not created.

The following validation messages were displayed:

* `size must be between 11 and 21`
* `size must be between 3 and 18`
* `size must be between 3 and 30`
* `must be a well-formed email address`

All validation messages appeared in one combined area rather than beside the corresponding fields.

**Valid submission:**

The following test data was accepted:

* First name: `Test`
* Last name: `User`
* Email: `test.user@example.com`
* Phone: `07123456789`

The booking was successfully created.

The confirmation displayed:

* **Booking Confirmed**
* `Your booking has been confirmed for the following dates: 2026-06-28 - 2026-06-30`
* A **Return Home** button that returned the user to the homepage

No booking reference or reservation number was displayed.

**Duplicate-booking observation:**

After a successful reservation, the same room and date range, **28/06/2026–30/06/2026**, remained selectable.

Submitting the same guest information again produced another **Booking Confirmed** message.

Because the application is a shared demonstration environment whose database may reset periodically, further API or administrative verification is required to confirm whether two overlapping booking records were created.

**Question for later verification:**

* Does the backend permit multiple active bookings for the same room and overlapping dates?

**Questions or unclear behaviour:**

* Should the selected dates remain visible while the user enters guest information?
* Should required fields be marked clearly before submission?
* Should validation messages identify the corresponding field more clearly?
* Should validation messages appear beside the relevant inputs?
* Should already-booked dates be disabled or marked as unavailable?

---

### 5. Contact Form

**What the feature appears to do:**

The **Send Us a Message** form allows users to submit a general enquiry to the bed-and-breakfast.

**Inputs:**

* Name
* Email
* Phone
* Subject
* Message
* **Submit** button

No placeholder text or visible required-field indicators were displayed.

**Expected user outcome:**

The application should validate the submitted information, explain invalid input clearly, and show confirmation after a valid message is submitted.

**Empty submission:**

Submitting the form with all fields empty was blocked.

The following validation messages appeared together in one error area below the form:

* `Phone may not be blank`
* `Phone must be between 11 and 21 characters.`
* `Email may not be blank`
* `Message may not be blank`
* `Message must be between 20 and 2000 characters.`
* `Subject must be between 5 and 100 characters.`
* `Name may not be blank`
* `Subject may not be blank`

The individual fields were not highlighted, and the error messages were not displayed beside their corresponding fields.

**Invalid submission:**

The following values were tested:

* Name: `A`
* Email: `invalid-email`
* Phone: `123`
* Subject: `Hi`
* Message: `Too short`

The form was not submitted.

The following validation messages were displayed:

* `Phone must be between 11 and 21 characters.`
* `must be a well-formed email address`
* `Subject must be between 5 and 100 characters.`
* `Message must be between 20 and 2000 characters.`

The phone, email, subject, and message values were rejected.

No validation message was displayed for the one-character name.

**Valid submission:**

The following test data was accepted:

* Name: `Test User`
* Email: `test.user@example.com`
* Phone: `07123456789`
* Subject: `Room information request`
* Message: `I would like more information about room availability and booking options.`

The form was replaced by a confirmation panel containing:

* `Thanks for getting in touch Test User!`
* `We'll get back to you about`
* `Room information request`
* `as soon as possible.`

No reference number was displayed.

The confirmation showed the submitted name and subject, but did not display the email address, phone number, or full message.

Refreshing the page restored a new blank contact form.

**Questions or unclear behaviour:**

* Should required fields be identified before submission?
* Should validation messages appear beside their corresponding fields?
* Should the email validation message identify the email field explicitly?
* Is a one-character name intentionally accepted?
* Should the confirmation include a message reference number?
* Should the confirmation display more of the submitted information?

---

### 6. Responsive Behaviour

**What was checked:**

Responsive behaviour was tested in Firefox Responsive Design Mode on Windows 10 using the following simulated viewport sizes:

* Mobile: **375 × 667**
* Tablet: **768 × 1024**
* Device pixel ratio: **1**
* Browser zoom: **100%**

The homepage and room-detail pages were reviewed at both viewport sizes.

#### Mobile — 375 × 667

**Homepage observations:**

* The header changed to a hamburger navigation menu.
* The hamburger menu opened and remained usable.
* The hero section, availability form, room cards, contact form, and footer fitted the viewport correctly.
* The room cards stacked vertically.
* No horizontal scrolling was observed.
* The location map displayed as a very short horizontal strip, leaving most of the map area hidden.

**Room-detail page observations:**

* The room title, accessibility label, maximum guest capacity, image, description, features, policies, and house rules fitted the viewport.
* The calendar controls and date selection remained usable.
* The price summary fitted within the screen width.
* The guest-information form and reservation controls remained usable.
* The similar-room recommendations displayed correctly.
* No horizontal scrolling or overlapping content was observed.

#### Tablet — 768 × 1024

**Homepage observations:**

* The header continued to use a hamburger menu.
* Opening the menu expanded the header and moved the page content downward.
* The menu opened and closed correctly, and all links remained usable.
* The hero section, availability form, room cards, contact form, and footer fitted the viewport.
* No horizontal scrolling was observed.
* The location map remained compressed and did not display its full intended height.

**Room-detail page observations:**

* The room information, image, calendar, price summary, booking form, and reservation controls remained usable.
* Similar-room cards displayed in two columns.
* The spacing between the reservation section and the **Similar Rooms You Might Like** heading was very limited.
* The cramped spacing was reproduced on more than one room-detail page.
* No overlapping controls or horizontal scrolling were observed.

**Other observation requiring later verification:**

* The number and content of similar-room cards changed after refreshing the page.
* A partially displayed third card disappeared after the refresh.
* Further testing is needed to determine whether this is caused by changing application data, loading behaviour, or a display issue.

**Questions or unclear behaviour:**

* Should the map maintain a larger visible height on mobile and tablet screens?
* Should additional spacing appear between the reservation section and the similar-room recommendations?
* Is the changing similar-room content expected in the shared demonstration environment?

