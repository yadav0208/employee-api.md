
# Employee Management API

This API allows you to manage employee records including adding, editing, deleting, searching, and uploading in bulk.

---

## Base URL

`http://localhost:4000`

---

## 📋 Endpoints

### 🔹 Get All Employees  
**GET** `/Users`

Returns a list of all employees.

---

### 🔍 Search Employee by Name  
**GET** `/Users/search/:query`

**Example:**  
`GET /Users/search/Radha`

Returns matching employee records by name.

---

### 🔎 Get Employee by ID  
**GET** `/Users/:id`

Returns an employee by ID.

---

### ➕ Add New Employee  
**POST** `/Users`

**Request Body (JSON):**
```json
{
  "Name": "Rohan",
  "Email": "rohan@shipway.com"
}
```

**Response:**
```json
{
  "id": 1,
  "Name": "Rohan",
  "Email": "rohan@shipway.com"
}
```

---

### 🖊️ Update Employee  
**PUT** `/Users/:id`

**Request Body (JSON):**
```json
{
  "Name": "Updated Name",
  "Email": "updated@gmail.com"
}
```

Updates the employee with given ID.

---

### 🗑️ Delete Employee  
**DELETE** `/Users/:id`

Deletes an employee with the specified ID.

---


## 📁 Status Codes

- `200 OK` – Success
- `201 Created` – New resource created
- `400 Bad Request` – Missing or invalid data
- `404 Not Found` – Employee not found
- `500 Internal Server Error` – Server-side issue


