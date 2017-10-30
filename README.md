# Cronofy

API Documentation
=======
https://www.getpostman.com/collections/f411cfe210cce5dfdeeb

---
### GET Messages
---

Return a JSON list of Message objects that are currently being stored.

* **URL**

  `/messages/`

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
  {“messages”: [{“message_text”: “hello world”, “id”: 1}]}
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
