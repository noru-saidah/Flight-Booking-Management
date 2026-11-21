# SkyRoute – Flight Booking Management System

## Project description
SkyRoute is a responsive flight booking management web application prototype. It provides a single workspace to manage flight schedules, passenger details and booking records, with a dashboard and reports for a quick operational overview.

## Features
- Account registration and sign-in with input validation and clear error feedback.
- Session-based sign-in state for the current browser tab/session.
- Responsive navigation and mobile-friendly layout.
- Dashboard summary cards and meaningful booking charts.
- Flight schedule management: create, read, update, delete, search and filter.
- Booking management: create, read, update, delete, search, filter and CSV export.
- Passenger directory: create, read, update, delete, search and CSV export.
- Reports for booking status, monthly booking activity and popular routes.
- Restore sample records and export data to CSV.
- Structured page titles, labels, metadata and footer content.

## How to run
1. Download and extract the project ZIP.
2. Open `index.html` using Google Chrome. An internet connection is needed to load Bootstrap, Bootstrap Icons, Google Fonts and Chart.js from their CDNs.
3. On the sign-in screen, select **Create an account**.
4. Register using your own test name, email address and password (minimum 8 characters).
5. Return to **Sign in** and use the account you just registered.
6. Use the sidebar to explore Dashboard, Flight schedule, Bookings, Passengers, Reports, Settings and Quick guide.

## Login testing instructions
There is no pre-created demo account. Create a new account on the registration form first. To test the error handling, try signing in with an incorrect password or an unregistered email address. The system should display an error message.

## Frameworks and libraries
- HTML5 – page structure and forms.
- CSS3 – custom visual design and responsive layout.
- JavaScript – form validation, navigation, session state, CRUD operations, search, filtering and CSV export.
- Bootstrap 5.3.3 – responsive grid, components and layout utilities.
- Bootstrap Icons – interface icons.
- Chart.js 4.4.7 – dashboard and report visualisations.

## Data and authentication limitation
This version is designed as a GitHub Pages-compatible academic prototype. User accounts and application records are stored in the browser using `localStorage`; the sign-in state uses `sessionStorage`. This demonstrates the required interface and interaction but is **not production-grade authentication or a shared database**. Browser storage is not secure for real passwords or sensitive passenger information. Each browser/device has its own data.

The lecture notes also introduce PHP, MySQL, server-side sessions and database-driven CRUD. To turn this prototype into a production-style multi-user application, implement a PHP backend, server-side session authentication, password hashing, server-side validation, access control and a MySQL database. GitHub Pages does not execute PHP, so a PHP/MySQL deployment needs a PHP-capable host. Do not describe this localStorage prototype as a live airline reservation service.

## Suggested database entities for a future PHP/MySQL version
- `users`: user_id, full_name, email, password_hash, created_at.
- `flights`: flight_id, flight_number, airline, origin, destination, flight_date, departure_time, arrival_time, capacity, fare, status.
- `passengers`: passenger_id, full_name, email, phone, nationality.
- `bookings`: booking_id, booking_reference, passenger_id, flight_id, seat_number, travel_class, amount, status, created_at.

## Project structure
```text
SkyRoute/
├── index.html
├── README.md
└── assets/
    ├── css/
    │   └── style.css
    ├── js/
    │   └── app.js
    └── images/
```

## GitHub Pages deployment
1. Create a GitHub repository and upload the complete project structure.
2. Open repository **Settings → Pages**.
3. Under Build and deployment, select **Deploy from a branch**.
4. Select the `main` branch and `/ (root)` folder, then save.
5. Wait for GitHub Pages to publish and copy the live website URL.
6. Submit both the GitHub Pages live link and repository link as required by the assignment.

## Testing checklist
- [ ] Register a new account and sign in successfully.
- [ ] Try an incorrect password and confirm that an error message appears.
- [ ] Navigate between all sidebar pages on desktop and mobile widths.
- [ ] Add, edit, search, filter and delete a flight that has no linked booking.
- [ ] Add, edit, search and delete a passenger that has no linked booking.
- [ ] Create, edit, search, filter and delete a booking.
- [ ] Confirm that linked flights/passengers cannot be deleted while bookings refer to them.
- [ ] Check that dashboard figures and charts reflect the stored booking records.
- [ ] Export the records to CSV.
- [ ] Sign out and sign in again.

---
**Academic use note:** Review the code, customise the content and design, and make sure you can explain the functions and limitations during assessment.
