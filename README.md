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
### POST Event
---

Should accept a “calender Id” parameter and "event id " parameter that creates a event object and stores in the calender

* **URL**

`/{calender-Id}/events`

* **Method:**

`POST`

*  **URL Params**

**Required:**

  `calender id`

**Optional:**

  `*None*`

* **Data Params**

**Required:**

* **JSON Object:**

```bash
{ {
    "event_id":"E1234567890",
    "summary":"Created with Cronofy",
    "description":"You can put notes in here",
    "start":"2016-03-15T15:30:00Z",
    "end":"2016-03-15T16:00:00Z",
    "tzid":"Etc/UTC",
    "location":{
        "description":"Board Room"
    }
}
```

* **Success Response:**

* **Code:** 200 <br />

* **Content:**
  
  ```bash
  {“message”: {“message_text”: “hello world”, “id”: 1}]}}
  ``` 

---
### DELETE Event
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
---
### GET Free/Busy Event
---

Delete the message with the given id

* **URL**

`/free_busy/tzid`

* **Method:**

`GET`

*  **URL Params**

**Required:**

 `*id*`
 
**Optional:**

  `*None*`

* **Data Params**

**Required:**

  `tzid`

**Optional:**

  `*None*`

* **Success Response:**

   `{
    "pages": {
        "current": 1,
        "total": 1
    },
    "free_busy": [
        {
            "calendar_id": "cal_WfHs-c1iVgP3AAKx_RKyPAEDs8zSkRLgWYheKWw",
            "start": "2017-09-26",
            "end": "2017-09-27",
            "free_busy_status": "free"
        },
        {
            "calendar_id": "cal_WfHs-c1iVgP3AAKx_RKyPAEDs8zSkRLgWYheKWw",
            "start": "2017-09-26T03:30:00Z",
            "end": "2017-09-26T04:30:00Z",
            "free_busy_status": "busy"
        }]`
   
* **Code:** 200 <br />
