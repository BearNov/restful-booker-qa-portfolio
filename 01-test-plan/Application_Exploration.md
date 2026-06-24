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

-Clicking the logo in the upper-left corner returns the user to the homepage.
-Clicking the hamburger menu opens and closes the navigation menu.
-Clicking Rooms scrolls to the Our Rooms section.
-Clicking Booking also scrolls to the Our Rooms section.
-Clicking Amenities changes the URL, but no visible page movement or content change occurs.
-Clicking Location scrolls to the location and contact-information section.
-Clicking Contact scrolls to the contact form.
-Clicking Admin opens the administration login page.
-Clicking Book Now in the hero section scrolls to the Our Rooms section.
-The footer contains quick links, policy links, contact information, and a link to the administration panel.
-The Cookie Policy and Privacy Policy links open their respective pages.
-The Admin Panel footer link opens the same administration page as the main navigation link.

**Questions or unclear behaviour:**

-Is the Amenities link intended to scroll to an amenities section that is currently missing or inaccessible?
-Should the Booking link open a dedicated booking section instead of the general rooms section?
-The footer links for Home, Rooms, Booking, and Contact all appear to return to the hero section. Should each link navigate to its corresponding section?
-Should a Logout button be visible on the administration page before the user has successfully logged in?

---

### 2. Room Listings and Details

**What the feature appears to do:**

**Available actions:**

**Inputs:**

**Expected user outcome:**

**Questions or unclear behaviour:**

---

### 3. Availability Search

**What the feature appears to do:**

**Inputs:**

**Expected user outcome:**

**Questions or unclear behaviour:**

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
