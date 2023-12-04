# Welcome to National Parks Uml

---

## Task

_What is the problem? And where is the challenge?_\
A project task is to create a UML Class diagram considering the following features:

- Multiple Parks
- Users
- Rangers per Park
- Visitors
- Lodges
- Tickets
- Annual Passes

## Description

_How have you solved the problem?_\
Created a diagram defining various Classes, Class Attributes and Methods.\
Scotland's National Parks were used as a basis for UML diagram: https://www.visitscotland.com/things-to-do/landscapes-nature/national-parks

#### National Park Management System Class

A base class for multiple parks.

- _National Park Management System Class Attributes_: parks (list of parks)
- _National Park Management System Class Methods_: None
- _National Park Management System Class Sub-classes_: National Park
- _National Park Management System Class Multiplicity_:
  - National Park Management System may have at least one National Park associated with it. One or more National Parks may be part of the National Park Management System.
- _National Park Management System Class Super-classes_: None

#### National Park Class

A class for the National Park.

- _National Park Class Attributes_: name, id, address, area, rangers (list of rangers)
- _National Park Class Methods_: None
- _National Park Class Sub-classes_: None
- _National Park Associated Classes_: Attraction, Accommodation, User, Visitor, Ranger, Ticket
- _National Park Multiplicity_:
  - National Park may be associated with one or more Attractions.
  - National Park may be associated with zero or more Accommodation.
  - National Park may be associated with zero or more Users.
  - National Park may be associated with zero or more Visitor.
  - National Park may be associated with one or more Rangers.
  - At least one Ticket is needed to access a National Park.
- _National Park Class Super-classes_: National Park Management System Class

#### User Class

A class for various Users of the National Park.

- _User Class Attributes_: firstName, lastName, email, phone, userID, username, password
- _User Class Methods_: register(), login(), updatePassword(), editProfile()
- _User Class Sub-classes_: Ranger, Visitor
- _User Associated Classes_: National Park, Tickets (from Visitor Class)
- _User Multiplicity_:
  - A User can be associated with zero or more National Parks.
- _User Class Super-classes_: None

##### _Ranger Class_

A sub-class of User's Class.

- _Ranger Class Attributes_: rangerID, badgeNumber, parks (list of parks), salary
- _Ranger Class Methods_: None
- _Ranger Class Sub-classes_: None
- _Ranger Associated Classes_: National Park
- _Ranger Multiplicity_:
  - A Ranger can be associated with one or more National Parks.
- _Ranger Class Super-classes_: User

##### _Visitor Class_

A sub-class of User's Class.

- _Visitor Class Attributes_: parks (list of parks), tickets(list of tickets)
- _Visitor Class Methods_: deleteAccount()
- _Visitor Class Sub-classes_: None
- _Visitor Associated Classes_: National Park, Attraction, Ticket
- _Visitor Multiplicity_:
  - A Visitor can be associated with zero or more National Parks.
  - A Visitor can have one or more Tickets.
  - A Visitor can visit one or more Attractions.
- _Visitor Class Super-classes_: User

#### Accommodation Class

A class for various Accommodation in the National Park.

- _Accommodation Class Attributes_: accommodationID, name, type, park, addres, email, phone, capacity, facilities
- _Accommodation Class Methods_: checkAvailability(), book(), cancel()
- _Accommodation Class Sub-classes_: Lodge, Bed & Breakfast(B&B), Cottage
- _Accommodation Associated Classes_: National Park
- _Accommodation Multiplicity_:
  - An Accommodation can be associated with zero or more National Parks.
- _Accommodation Class Super-classes_: None

#### Attraction Class

A class for various Attractions in the National Park.

- _Attraction Class Attributes_: attractionID, name, description
- _Attraction Class Methods_: None
- _Attraction Class Sub-classes_: Lake, River, Forest Trail, Mountain, Village, Rheindeer Centre, Animals
- _Attraction Associated Classes_: National Park
- _Attraction Multiplicity_:
  - Attraction can have zero or more Visitors.
  - An Attraction can be associated with one or more National Parks.
  - Rheindeer Centre cannot exist without at least one Rheindeer.
- _Attraction Class Super-classes_: None

##### Animals Class

A class for various Animals in the National Park. A sub-class of Attraction's Class.

- _Animals Class Attributes_: type, name, age, gender, color, quantity
- _Animals Class Methods_: None
- _Animals Class Sub-classes_: Rheindeer, Sheep, Highland Cow
- _Animals Associated Classes_: None
- _Animals Multiplicity_: None
- _Animals Class Super-classes_: Attraction

#### Ticket Class

A Ticket Class is a Super-class for different types of tickets and has associations with other classes.

- _Ticket Class Attributes_: id, issueDate, expiryDate, visitor, parks
- _Ticket Class Methods_: choose(), add(), update(), buy(), cancel(), upgrade()
- _Ticket Class Sub-classes/Inheritance_: Annual Pass, Day Ticket, Weekend Ticket.
- _Ticket Class Associated Classes_: National Park, Visitor, Date.
- _Ticket Class Multiplicity_:
  - A Ticket may be associated with zero or one Annual Pass. An Annual Pass may be associated with exactly one Ticket.
  - A Ticket may be associated with zero or one Day Pass. A Day Pass may be associated with exactly one Ticket.
  - A Ticket may be associated with zero or one Weekend Pass. A Weekend Pass may be associated with exactly one Ticket.
  - Ticket can have one issue date and one expiry date.
  - A Ticket can be associated with one or more National Parks.
  - A Ticket may be associated with one or more Visitors.
- _Ticket Class Super-classes_: None

#### Date Class

A class for different types of dates related to the Ticket.

- _Date Class Attributes_: day, month, year
- _Date Class Methods_: None
- _Date Class Sub-classes_: None
- _Date Associated Classes_: Ticket
- _Date Multiplicity_:
  - The same Date can be reused for multiple tickets. Zero or more Dates can be associated with the Ticket.
- _Date Class Super-classes_: None

## Installation

_How to install your project? npm install? make? make re?_\
Installation is not required.

## Usage

_How does it work?_\
The UML diagram can be accessed on draw.io.
This is draw.io link: https://drive.google.com/file/d/1YfX7r8sqtuGD2h_ktvo3byREEDJn2QwP/view?usp=sharing

### The Core Team

Natalie Peyre
<br>
<span><i>Made at <a href='https://qwasar.io'>Qwasar SV -- Software Engineering College</a></i></span>
<span><img alt="Qwasar SV -- Software Engineering School's Logo" src='https://storage.googleapis.com/qwasar-public/qwasar-logo_50x50.png' width='20px' /></span>
