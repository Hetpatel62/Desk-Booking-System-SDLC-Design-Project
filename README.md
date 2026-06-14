================================================================================
DESK BOOKING SYSTEM — SDLC Design Project
================================================================================

Project Type   : Software Design & Requirements Engineering
Team           : Group 15
Members        : Het BharatKumar Patel, Atiroop Vaid, Rebecca Lulu,
                 Jay Girishkumar Champaneri
Methodology    : Agile / SDLC


--------------------------------------------------------------------------------
PROJECT OVERVIEW
--------------------------------------------------------------------------------

This project covers the full software development lifecycle (SDLC) design for a
Desk Booking System — an internal enterprise tool that allows employees to
reserve office desks and enables administrators to manage desk configurations
across office spaces.

The system supports two primary use cases:
  1. Desk Booking       — Employees browse available desks and reserve them
                          for specific dates, times, and locations.
  2. Desk Configuration — Office Administrators add, edit, or remove desks
                          and adjust layouts based on employee feedback.


--------------------------------------------------------------------------------
ARTIFACTS PRODUCED
--------------------------------------------------------------------------------

Q1 — Use Case Descriptions
  - Fully developed use case: Desk Booking
      Actors       : Employee
      Stakeholders : Managers, IT Department
      Includes     : Preconditions, postconditions, flow of activities,
                     exception conditions

  - Fully developed use case: Desk Configuration Management
      Actors       : Office Administrator
      Stakeholders : Office Administrators, Facilities Manager
      Includes     : Preconditions, postconditions, flow of activities,
                     exception conditions

Q2 — Activity Diagrams
  - Activity diagram for Desk Booking (swimlane: User | System)
  - Activity diagram for Desk Configuration Management
    (swimlane: Administrator | System)

Q3 — System Sequence Diagrams (SSD)
  - SSD for Desk Booking
  - SSD for Desk Configuration Management

Q4 — First Cut Design Class Diagrams
  - Booking System class diagram
      Classes: Employee, Booking, Desk, BookingHandler (Controller)
  - Desk Configuration class diagram
      Classes: Employee, OfficeSpace, DeskConfiguration, Desk

Q5 — Agile CRC Cards + Sequence & Communication Diagrams
  - CRC Cards: Employee, Booking
  - Sequence Diagram: Desk Booking flow
      (Employee → BookingHandler → Desk → Booking)
  - Communication Diagram: Desk Configuration flow
      (Admin → OfficeSpace → DeskConfiguration → Desk)

Q6 — Agile Fully Developed Design Class Diagram
  - Full system diagram including:
      Classes: Employee, Booking, Desk, Space, Amenity, Feedback,
               DateTime, FacilitiesManager, Administrator,
               TaskHandler, Database

Q7 — Agile Class Package Diagram
  - 3-layer architecture:
      View Layer        : DeskBookingWindow, AppointmentWindow,
                          UserPersonalWindow, FacilitiesManager
      Domain Layer      : Booking, Amenity, Desk, DateTime,
                          TaskHandler, Feedback, Space, Employee
      Data Access Layer : Database, BookingDA, DeskDA,
                          FeedbackDA, EmployeeDA


--------------------------------------------------------------------------------
KEY SYSTEM FEATURES
--------------------------------------------------------------------------------

- Employee authentication (login / signup / password reset)
- Date, time, and location-based desk search and filtering
- Desk availability validation and conflict prevention
- Booking confirmation via email notification
- Admin desk add / edit / remove with validation rules
- Feedback collection loop for layout adjustments
- Audit logging of all booking transactions (desk ID, user ID, timestamps)
- Exception handling for invalid credentials, booking conflicts,
  policy violations (e.g., blocking emergency exits)


--------------------------------------------------------------------------------
TECH CONTEXT / DESIGN DECISIONS
--------------------------------------------------------------------------------

- MVC pattern applied: BookingHandler acts as Controller
- Relational data model with foreign keys:
    Desk → OfficeSpace, DeskLocation
    Booking → Desk, Employee
- Booking records stored with: bookingID, bookedSpace, bookedDesk,
  bookedBy, startTime, endTime
- Desk availability toggled on reservation to prevent double-booking
- Layered package architecture separates UI, business logic, and data access


--------------------------------------------------------------------------------
SKILLS DEMONSTRATED
--------------------------------------------------------------------------------

- Requirements elicitation and use case documentation
- Process flow modeling (activity diagrams, SSDs)
- Agile artifact creation (CRC cards, user stories, backlog-ready specs)
- Object-oriented design (class diagrams, package diagrams)
- Stakeholder analysis and multi-actor system design
- Structured exception and edge case handling
- SDLC end-to-end coverage from requirements to design


--------------------------------------------------------------------------------
