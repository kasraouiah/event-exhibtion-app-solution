# Exhibition & Event Handler App Solution
## Description

The Exhibition & Event Handler App Solution is designed to streamline the management of guest check-ins, event organization, and exhibition handling. The system ensures structured registration, guest verification, and event oversight.

## Data Model
The solution is based on the following entities:

###  Event Maker
Represents the organizer of an event.
- fullname: String (Full Name of the organizer)
- email: String (Email of the organizer)
- Organizer Phone Number: String (Contact number of the organizer)

###  Event
Defines an event that is being organized.
- Name_of_Event: String (Event name)
- Start_date: Date (Event start date)
- End_date: Date (Event end date)

### Exhibition
Represents an exhibition held within an event.
- Exhibition_Name: String (Exhibition name)
- Start_Datetime: Datetime (Exhibition start date and time)
- End_Datetime: Datetime (Exhibition end date and time)


### Guest

Represents an attendee registering for exhibitions.
- Full_Name: String (Guest's full name)
- Email: String (Guest's email)

### Current Address

Represents the location details of events and guests.
- Country : String
- City : String
- Adress : String

### Interest
Represents an area of interest related to exhibitions.
- Interest: String (Description of the interest)


## Relationships:

```json

regarding Event entity
"An Event Maker can organize multiple events (one-to-many)."
"Each Event can be held at a specific Current Address (one-to-one)."
"Each Event can be associated with multiple Exhibitions (one-to-many)."

regarding Exhibition entity
"An Exhibition is part of an Event (many-to-one)."
"An Exhibition has multiple Guests (many-to-many)."
"An Exhibition has multiple Interests associated with it (one-to-many)."

regarding Guest entity
"A Guest can register for multiple Exhibitions (many-to-many)."
"A Guest has a Current Address (one-to-one)."

regarding Current Address
"A Current Address may be used by many guests (Many-to-one)."
"A Current Address may be used by many events AND an event is related to one Current Address (one-to-one)."

regarding Interest
"An exhibition is related to one Interest AND Interest can be related to many exhibition (One-to-many)" 
```


![image](https://github.com/user-attachments/assets/58d20218-7ff7-4f40-b56e-fb628c9114db)
