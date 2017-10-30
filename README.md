# Cronofy

API Documentation
=======
https://www.getpostman.com/collections/f411cfe210cce5dfdeeb

---
### GET Events
---

Return a JSON list of events from the synched calender.

* **URL**

  `/events?tzid=Etc/UTC`

* **Method:**
  
  `GET`
  
*  **URL Params**

   **Required:**
 
     `*None*`

   **Optional:**
 
     `*None*`

* **Success Response:**

  * **Code:** 200 <br />

* **Content:**
  
  ```bash
  {
    "pages": {
        "current": 1,
        "total": 1
    },
    "events": [
        {
            "calendar_id": "cal_WfHs-c1iVgP3AAKx_RKyPAEDs8zSkRLgWYheKWw",
            "event_uid": "evt_external_59f1ed034f5f8dc7da000010",
            "summary": "Career and Resource Fair",
            "description": "To see detailed information for automatically created events like this one, use the official Google Calendar app. https://g.co/calendar\n\nThis event was created from an email you received in Gmail. https://mail.google.com/mail?extsrc=cal&plid=ACUX6DNPYhAIDajB6jME-dZIyISP4xmG7Z-yTeI",
            "start": "2017-09-19T17:00:00Z",
            "end": "2017-09-19T20:00:00Z",
            "deleted": false,
            "created": "2017-08-10T15:38:49Z",
            "updated": "2017-09-17T17:01:44Z",
            "location": {
                "description": "Adam Clayton Powell State Office Building, 163 West 125th Street8th Floor, New York, NY, US, 10027"
            },
            "participation_status": "accepted",
            "attendees": [
                {
                    "email": "msruthi.92@gmail.com",
                    "display_name": "Sruthi Morusu",
                    "status": "accepted"
                }
            ],
            "organizer": {
                "email": "unknownorganizer@calendar.google.com",
                "display_name": "Unknown Organizer"
            },
            "transparency": "transparent",
            "status": "confirmed",
            "categories": [],
            "recurring": false,
            "options": {
                "delete": true,
                "update": true,
                "change_participation_status": true
            }
        }
  ``` 


--
### POST Message
---

Should accept a “message_text” parameter that creates a Message object and stores the value.

* **URL**

`/messages/`

* **Method:**

`POST`

*  **URL Params**

**Required:**

  `*None*`

**Optional:**

  `*None*`

* **Data Params**

**Required:**

* **JSON Object:**

```bash
{ “message_text”: “hello world” }
```

* **Success Response:**

* **Code:** 200 <br />

* **Content:**
  
  ```bash
  {“message”: {“message_text”: “hello world”, “id”: 1}]}}
  ``` 

---
### DELETE Message
---

Delete the message with the given id

* **URL**

`/messages/:id`

* **Method:**

`DELETE`

*  **URL Params**

**Required:**

 `*id*`
 
**Optional:**

  `*None*`

* **Data Params**

**Required:**

  `*None*`

**Optional:**

  `*None*`

* **Success Response:**

* **Code:** 200 <br />
