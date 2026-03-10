# Hospital-Management-System-LLD-Java-
1️⃣ Project Overview

A Hospital Management System manages:

Patient registration

Doctor management

Appointment booking

Treatment records

Billing

Core Actors

Patient

Doctor

Appointment

Hospital System

Example Workflow
Patient registers
      ↓
Doctor available
      ↓
Appointment booked
      ↓
Doctor treats patient
      ↓
Bill generated
🧠 LLD Concepts Used

This project demonstrates important interview design principles:

Concept	Where Used
Encapsulation	Patient, Doctor classes
Abstraction	HospitalService
Aggregation	Hospital contains doctors/patients
Collections	List, Map
Unique ID generation	Appointment IDs
Clean Code	Modular methods
📦 Class Design (LLD)
HospitalManagementSystem
        │
        ├── Patient
        │       id
        │       name
        │       age
        │
        ├── Doctor
        │       id
        │       name
        │       specialization
        │
        ├── Appointment
        │       appointmentId
        │       patient
        │       doctor
        │       date
        │
        └── HospitalService
                addPatient()
                addDoctor()
                bookAppointment()
                generateBill()

                🔍 Detailed Explanation
1️⃣ Patient Class

Represents a hospital patient.

Attributes:
id
name
age

Encapsulation:

private variables
getter methods

Example:

Patient p1 = new Patient(101,"Alice",30);
👨‍⚕️ Doctor Class

Represents hospital doctors.

Attributes:

id
name
specialization

Example:

Doctor d1 = new Doctor(1,"Dr Smith","Cardiology");
📅 Appointment Class

Represents patient-doctor booking.

Attributes:

appointmentId
patient
doctor
date

Relationship:

Appointment
   ↳ Patient
   ↳ Doctor

This demonstrates object composition.

🏥 HospitalService Class

This is the core business logic layer.

Data Structures used:

Map<Integer, Patient>
Map<Integer, Doctor>
List<Appointment>

Why?

Structure	Reason
HashMap	Fast lookup
ArrayList	Store appointment history
Methods
Add Patient
addPatient()

Adds new patient to hospital.

Add Doctor
addDoctor()

Registers doctor.

Book Appointment
bookAppointment(patientId, doctorId, date)

Steps:

1 validate patient
2 validate doctor
3 create appointment
4 store appointment
Generate Bill
generateBill()

Simple billing system.

⚙️ Time Complexity
Operation	Complexity
Add Patient	O(1)
Add Doctor	O(1)
Book Appointment	O(1)
View Appointments	O(n)
📈 How To Make It Enterprise Level

To upgrade this system:

Add:

Features

Room Management

ICU Management

Pharmacy

Lab Reports

Nurse Management

Payment Gateway

Insurance Handling

Emergency Queue

Design Patterns
Pattern	Usage
Factory Pattern	Create Doctors
Singleton	HospitalService
Observer	Patient Notifications
Strategy	Billing calculation
🧠 Why This Project Is Powerful For Interviews

Companies test exactly this level.

Typical interview question:

Design a Hospital Management System

This solution shows:

OOP

Collections

Relationships

Modular architecture

Clean design
