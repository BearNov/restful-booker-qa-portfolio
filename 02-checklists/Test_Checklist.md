# Manual Test Checklist — Restful Booker Platform

## Document Information

* **Project:** Restful Booker QA Portfolio
* **Application Under Test:** Restful Booker Platform
* **Prepared by:** Baruch Ilhanov
* **Version:** 1.0
* **Status:** Draft

## Status Legend

* **Not Run:** The scenario has not yet been executed.
* **Pass:** The observed result matches the expected behaviour.
* **Fail:** The observed result does not match the expected behaviour.
* **Blocked:** The scenario cannot be completed because of another issue or environment limitation.

## 1. Homepage and Navigation

| ID      | Test Scenario                                           | Expected Result                                                  | Status  |
| ------- | ------------------------------------------------------- | ---------------------------------------------------------------- | ------- |
| NAV-001 | Open the homepage using the public application URL      | The homepage loads successfully and its main content is visible  | Not Run |
| NAV-002 | Click the logo in the header                            | The user returns to the homepage                                 | Not Run |
| NAV-003 | Open and close the hamburger navigation menu            | The menu opens and closes correctly, and its links remain usable | Not Run |
| NAV-004 | Click the **Rooms** navigation link                     | The page moves to the **Our Rooms** section                      | Not Run |
| NAV-005 | Click the **Booking** navigation link                   | The page moves to the intended booking or room-selection section | Not Run |
| NAV-006 | Click the **Amenities** navigation link                 | The page moves to the corresponding amenities content            | Not Run |
| NAV-007 | Click the **Location** navigation link                  | The page moves to the location section                           | Not Run |
| NAV-008 | Click the **Contact** navigation link                   | The page moves to the contact form                               | Not Run |
| NAV-009 | Click the hero **Book Now** button                      | The page moves to the room-selection section                     | Not Run |
| NAV-010 | Click the **Admin** navigation link                     | The administration login page opens                              | Not Run |
| NAV-011 | Click the footer quick links                            | Each link moves to its corresponding page section                | Not Run |
| NAV-012 | Open the **Cookie Policy** and **Privacy Policy** links | Each policy page opens successfully                              | Not Run |
| NAV-013 | Click the footer **Admin Panel** link                   | The administration login page opens                              | Not Run |

## 2. Room Listings and Room Details

| ID       | Test Scenario                                               | Expected Result                                                                                                              | Status  |
| -------- | ----------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ------- |
| ROOM-001 | View the **Our Rooms** section on the homepage              | Available room cards are displayed correctly                                                                                 | Not Run |
| ROOM-002 | Review the information displayed on each room card          | Each card displays an image, room type, description, amenities, price per night, and **Book Now** button                     | Not Run |
| ROOM-003 | Compare the displayed room cards                            | Each room displays information that corresponds to that specific room                                                        | Not Run |
| ROOM-004 | Click **Book Now** on the Single Room card                  | The Single Room detail page opens                                                                                            | Not Run |
| ROOM-005 | Click **Book Now** on the Double Room card                  | The Double Room detail page opens                                                                                            | Not Run |
| ROOM-006 | Compare the room card information with its detail page      | The room title, price, capacity, and features match the selected room card                                                   | Not Run |
| ROOM-007 | Review the room-detail page content                         | The page displays the room image, description, accessibility information, capacity, features, policies, and booking controls | Not Run |
| ROOM-008 | Use the browser Back button from a room-detail page         | The user returns to the previous page without unexpected errors                                                              | Not Run |
| ROOM-009 | Click **Home** in the room-detail breadcrumb                | The user returns to the homepage                                                                                             | Not Run |
| ROOM-010 | Click **Rooms** in the room-detail breadcrumb               | The user returns to the **Our Rooms** section                                                                                | Not Run |
| ROOM-011 | Use the **Today**, **Back**, and **Next** calendar controls | The calendar moves to the expected date or month                                                                             | Not Run |
| ROOM-012 | Select reservation dates on the room-detail page            | The selected dates are shown and the price summary updates                                                                   | Not Run |
| ROOM-013 | Review the **Similar Rooms You Might Like** section         | Similar-room cards display correctly with working **View Details** buttons                                                   | Not Run |
| ROOM-014 | Click **View Details** on a similar-room card               | The corresponding room-detail page opens                                                                                     | Not Run |
| ROOM-015 | Refresh a room-detail page                                  | The page reloads successfully without missing or corrupted room information                                                  | Not Run |

## 3. Availability Search

| ID        | Test Scenario                                               | Expected Result                                                                               | Status  |
| --------- | ----------------------------------------------------------- | --------------------------------------------------------------------------------------------- | ------- |
| AVAIL-001 | Open the homepage and review the default availability dates | The check-in date defaults to the current date and the checkout date defaults to a later date | Not Run |
| AVAIL-002 | Search using a valid future check-in and checkout range     | The date range is accepted and rooms available for the selected dates are displayed           | Not Run |
| AVAIL-003 | Compare results from two different valid future date ranges | The displayed availability reflects the date range used in each search                        | Not Run |
| AVAIL-004 | Select the same date for check-in and checkout              | The application rejects a zero-night stay and provides clear validation                       | Not Run |
| AVAIL-005 | Select a checkout date earlier than the check-in date       | The invalid date range is rejected and a clear validation message is displayed                | Not Run |
| AVAIL-006 | Select a check-in date in the past                          | Past dates cannot be selected or submitted for a new reservation                              | Not Run |
| AVAIL-007 | Select a valid check-in date and a past checkout date       | The invalid combination is rejected and a clear validation message is displayed               | Not Run |
| AVAIL-008 | Click **Check Availability** with a valid date range        | The application processes the selected dates and moves the user to the availability results   | Not Run |
| AVAIL-009 | Review the room cards after an availability search          | Only rooms available for the selected date range are shown                                    | Not Run |
| AVAIL-010 | Review feedback after an availability search                | The application clearly indicates whether matching rooms are available                        | Not Run |
| AVAIL-011 | Open a room from the availability results                   | The selected dates are preserved when the room-detail page opens                              | Not Run |
| AVAIL-012 | Refresh the page after entering availability dates          | The application handles the entered dates consistently without corrupted or unexpected values | Not Run |

## 4. Booking Flow

| ID       | Test Scenario                                                                  | Expected Result                                                                                 | Status  |
| -------- | ------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------- | ------- |
| BOOK-001 | Select a valid future reservation date range                                   | The dates are selected successfully                                                             | Not Run |
| BOOK-002 | Select a two-night stay in the Single Room                                     | The room cost is calculated as the nightly price multiplied by two nights                       | Not Run |
| BOOK-003 | Review the complete price summary                                              | The room cost, cleaning fee, service fee, and total are displayed and calculated correctly      | Not Run |
| BOOK-004 | Click **Reserve Now** after selecting valid dates                              | The guest-information form opens                                                                | Not Run |
| BOOK-005 | Review the guest-information form                                              | First name, last name, email, and phone fields are displayed                                    | Not Run |
| BOOK-006 | Review the selected dates after opening the guest-information form             | The selected reservation dates remain visible to the user                                       | Not Run |
| BOOK-007 | Submit the guest-information form with all fields empty                        | Submission is blocked and clear validation is shown for every required field                    | Not Run |
| BOOK-008 | Enter first and last names below the minimum permitted length                  | The invalid names are rejected with clear field-specific validation                             | Not Run |
| BOOK-009 | Enter an incorrectly formatted email address                                   | The invalid email is rejected with a clear email validation message                             | Not Run |
| BOOK-010 | Enter a phone number below the minimum permitted length                        | The invalid phone number is rejected with a clear phone validation message                      | Not Run |
| BOOK-011 | Correct invalid guest information and resubmit                                 | Previous validation errors are removed when the values become valid                             | Not Run |
| BOOK-012 | Submit valid guest information for an available room and date range            | The reservation is accepted and a confirmation is displayed                                     | Not Run |
| BOOK-013 | Review the successful-booking confirmation                                     | The confirmation displays the booked dates and clearly states that the booking succeeded        | Not Run |
| BOOK-014 | Review the confirmation for a booking reference                                | A unique booking reference or another way to identify the reservation is displayed              | Not Run |
| BOOK-015 | Click **Return Home** after a successful reservation                           | The user returns to the homepage                                                                | Not Run |
| BOOK-016 | Attempt to reserve the same room for the same dates after a successful booking | The application prevents an overlapping reservation or clearly explains the room is unavailable | Not Run |
| BOOK-017 | Attempt to reserve a room using a checkout date earlier than the check-in date | The invalid reservation range is rejected                                                       | Not Run |
| BOOK-018 | Attempt to reserve a room using past dates                                     | Past dates cannot be used to create a new reservation                                           | Not Run |

## 5. Contact Form

To be completed.

## 6. Responsive Behaviour

To be completed.

## 7. Cross-Browser Checks

To be completed.
