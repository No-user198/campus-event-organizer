# 📅 Campus Event Organizer

A console-based Java application to manage university campus events including Workshops and Seminars. Built as an OOP Lab project demonstrating all four core Object-Oriented Programming principles.

---

## 👨‍💻 Team Members

| Name | Registration No |
|------|----------------|
| Abdul Razzaq | B25F0293AI178 |
| Shafiullah | B25F0120AI177 |

**Section:** Orange  
**Submitted to:** Mr. Obiadullah Miakhel  
**Institute:** Pak-Austria Fachhochschule (AF-IAST), Haripur, Pakistan  
**Department:** Artificial Intelligence  

---

## 📌 Problem Statement

Universities organize many events every semester — seminars, workshops, fests, and competitions. There is no proper central system to track these events. Volunteers and participants are managed manually on paper or through WhatsApp groups. This causes students to miss important events and organizers face a lot of confusion.

---

## ✅ Solution

A console-based Java application where an organizer can:
- Add events (Workshop or Seminar)
- Assign volunteers to events
- Register student participants
- View, search, and cancel events

---

## 🚀 Features

### Must Have (MVP)
- ✅ Add a new event with name, date, venue, and type
- ✅ Add volunteers to an event
- ✅ Register student participants
- ✅ Display list of all events
- ✅ Show full details of a specific event

### Should Have
- ✅ Cancel an existing event
- ✅ Search event by name
- ✅ Count total number of participants
- ✅ List all volunteers assigned to an event

---

## 🗂️ Project Structure

```
campus-event-organizer/
│
├── Event.java          # Abstract base class
├── Workshop.java       # Extends Event (trainer, seats)
├── Seminar.java        # Extends Event (speaker, topic)
├── Volunteer.java      # Helper class for volunteers
├── Participant.java    # Helper class for participants
└── Main.java           # Main menu-driven application
```

---

## 🧱 OOP Concepts Used

### 1. Encapsulation
All variables in every class are declared `private`. They are accessed and modified only through public getter and setter methods.

### 2. Inheritance
`Workshop` and `Seminar` both extend the abstract base class `Event`. They inherit common attributes `name`, `date`, and `venue` and add their own specific attributes.

### 3. Polymorphism
Both `Workshop` and `Seminar` override the `getEventType()` and `displayInfo()` methods from `Event`. Same method name produces different behavior depending on which object calls it — this is **Runtime Polymorphism**.

### 4. Abstraction
`Event` is declared as an abstract class. It forces all child classes to provide their own implementation of `getEventType()` and `displayInfo()`. You cannot create an `Event` object directly.

---

## 🗃️ UML Class Diagram

```
          ┌──────────────────────┐
          │     <<abstract>>     │
          │        Event         │
          ├──────────────────────┤
          │ - name : String      │
          │ - date : String      │
          │ - venue : String     │
          ├──────────────────────┤
          │ + getName()          │
          │ + getDate()          │
          │ + getVenue()         │
          │ + getEventType()     │
          │ + displayInfo()      │
          └──────────┬───────────┘
                     │ extends
          ┌──────────┴───────────┐
          │                      │
┌─────────┴────────┐   ┌─────────┴────────┐
│     Workshop     │   │     Seminar      │
├──────────────────┤   ├──────────────────┤
│ - trainerName    │   │ - speakerName    │
│ - maxSeats       │   │ - topic          │
├──────────────────┤   ├──────────────────┤
│ + getEventType() │   │ + getEventType() │
│ + displayInfo()  │   │ + displayInfo()  │
└──────────────────┘   └──────────────────┘

┌──────────────────┐   ┌──────────────────┐
│    Volunteer     │   │   Participant    │
├──────────────────┤   ├──────────────────┤
│ - name           │   │ - name           │
│ - role           │   │ - rollNo         │
│ - eventName      │   │ - eventName      │
├──────────────────┤   ├──────────────────┤
│ + getName()      │   │ + getName()      │
│ + getRole()      │   │ + getRollNo()    │
│ + setRole()      │   │ + register()     │
│ + getDetails()   │   │ + getDetails()   │
└──────────────────┘   └──────────────────┘
```

---

## ▶️ How to Run

**Step 1 — Compile all files:**
```bash
javac *.java
```

**Step 2 — Run the application:**
```bash
java Main
```

**Step 3 — Use the menu:**
```
===== Campus Event Organizer =====
1. Add Event
2. Add Volunteer
3. Register Participant
4. Display All Events
5. Show Event Details
6. Search Event by Name
7. Cancel Event
0. Exit
```

---

## 🛠️ Language & Tools

- **Language:** Java
- **Type:** Console-based Application
- **Concepts:** OOP (Encapsulation, Inheritance, Polymorphism, Abstraction)

---

## ❌ Out of Scope

- Online or web-based interface
- Payment or ticketing system
- Email or SMS notifications
- Database or file storage
- Mobile application
