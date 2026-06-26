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

To be completed.

## 4. Booking Flow

To be completed.

## 5. Contact Form

To be completed.

## 6. Responsive Behaviour

To be completed.

## 7. Cross-Browser Checks

To be completed.
