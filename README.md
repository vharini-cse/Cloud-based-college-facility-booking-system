# Cloud Based Facility Booking and Management System

A web-based system that lets students and faculty book seminar halls, labs, auditoriums, and classrooms online, instead of checking availability manually. Users browse facilities, check real-time availability for a chosen date and time slot, and submit a booking request. Admins review, approve, or reject each request. This repository contains the **frontend** of the system.

**Live demo:** [# PolyBook — Cloud Based Poly Facility Booking and Management System

A web-based system that lets students and faculty book seminar halls, labs, auditoriums, and classrooms online, instead of checking availability manually. Users browse facilities, check real-time availability for a chosen date and time slot, and submit a booking request. Admins review, approve, or reject each request. This repository contains the **frontend** of the system.

**Live demo:**https://cloud-based-college-facility-booking-l51s.onrender.com 

## Features

- Student/Faculty and Admin login
- Browse facilities by category — Seminar Hall, Lab, Auditorium, Classroom
- Date and time-slot selection with live availability status (Available / Requested / Booked)
- Booking request submission
- Admin approval and rejection of pending requests
- Booking history for each user
- Full booking log for admin oversight

## Tech stack

- HTML, CSS, and vanilla JavaScript (no framework, no build step)
- Frontend logic is structured around JS classes (`User`, `Facility`, `BookingRequest`, `FacilityBookingService`) so it can be connected to a real backend API without reworking the UI
- Designed for deployment as a static site on Render

## Project structure

```
.
└── polybook-facility-booking.html   # entire frontend — HTML, CSS, and JS in one file
```

## Running locally

No build tools or dependencies are required.

1. Clone the repository
2. Open `polybook-facility-booking.html` directly in a browser

   or serve it locally:

   ```bash
   python3 -m http.server 8000
   ```

   then visit `http://localhost:8000/polybook-facility-booking.html`

## Deploying on Render

1. Push this repository to GitHub
2. On Render, create a new **Static Site**
3. Connect the repository
4. Leave the build command empty and set the publish directory to the repository root
5. Deploy, then add the resulting URL to the **Live demo** link at the top of this README

## Backend integration (planned)

The frontend currently keeps all data in memory inside the `FacilityBookingService` class, with no persistence between page reloads. Each of its methods (`getFacilities`, `getAvailability`, `submitBooking`, `approveBooking`, `rejectBooking`, etc.) is written as an async function with a `TODO(backend)` comment marking the exact API call it should become once a backend is deployed — for example, `submitBooking` becomes a `POST` to `/api/bookings`. Connecting a real backend should only require editing that one class.

## Author

[Add your name / roll number / institution here]

## Features

- Student/Faculty and Admin login
- Browse facilities by category — Seminar Hall, Lab, Auditorium, Classroom
- Date and time-slot selection with live availability status (Available / Requested / Booked)
- Booking request submission
- Admin approval and rejection of pending requests
- Booking history for each user
- Full booking log for admin oversight

## Tech stack

- HTML, CSS, and vanilla JavaScript (no framework, no build step)
- Frontend logic is structured around JS classes (`User`, `Facility`, `BookingRequest`, `FacilityBookingService`) so it can be connected to a real backend API without reworking the UI
- Designed for deployment as a static site on Render

## Project structure

```
.
└── polybook-facility-booking.html   # entire frontend — HTML, CSS, and JS in one file
```

## Running locally

No build tools or dependencies are required.

1. Clone the repository
2. Open `polybook-facility-booking.html` directly in a browser

   or serve it locally:

   ```bash
   python3 -m http.server 8000
   ```

   then visit `http://localhost:8000/polybook-facility-booking.html`

## Deploying on Render

1. Push this repository to GitHub
2. On Render, create a new **Static Site**
3. Connect the repository
4. Leave the build command empty and set the publish directory to the repository root
5. Deploy, then add the resulting URL to the **Live demo** link at the top of this README

## Backend integration (planned)

The frontend currently keeps all data in memory inside the `FacilityBookingService` class, with no persistence between page reloads. Each of its methods (`getFacilities`, `getAvailability`, `submitBooking`, `approveBooking`, `rejectBooking`, etc.) is written as an async function with a `TODO(backend)` comment marking the exact API call it should become once a backend is deployed — for example, `submitBooking` becomes a `POST` to `/api/bookings`. Connecting a real backend should only require editing that one class.

