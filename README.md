


# Spring Boot + MongoDB Auth Demo

This is a demo backend project using **Spring Boot**, **MongoDB Atlas**, and basic **User API** endpoints (`signup`, `getAllUsers`, etc).

---

## 🛠️ Project Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/Dimuthnilanjana/signup-web-backend.git
````

---

### 2. Create `application.properties`

> Do **NOT** commit your real credentials — this file is ignored via `.gitignore`.

Create a file at:

```
src/main/resources/application.properties
```

Add the following content (replace with your actual MongoDB connection):

```properties
# MongoDB Atlas Configuration
spring.data.mongodb.uri=mongodb+srv://<username>:<password>@<cluster>.mongodb.net/auth_db?retryWrites=true&w=majority
spring.data.mongodb.database=auth_db

# Optional Server Port
server.port=8080
```

✅ You can refer to `application-example.properties` for the structure.

---

### 3. Install Dependencies and Build

```bash
./mvnw clean install
```

Or if you have Maven installed globally:

```bash
mvn clean install
```

---

### 4. Run the Application

```bash
./mvnw spring-boot:run
```

Then visit:
📍 `http://localhost:8080`

---

### 5. Test with Postman

#### ➤ Create a New User

**POST** `http://localhost:8080/api/users/create`
**Headers:** `Content-Type: application/json`
**Body:**

```json
{
  "username": "user",
  "email": "user@example.com",
  "password": "123456"
}
```

#### ➤ Get All Users

**GET** `http://localhost:8080/api/users/all`

---

### 🔒 Security Note

`application.properties` is included in `.gitignore` to prevent leaking sensitive data.
Always keep your database credentials secure and never commit them to version control.



## ✅ Technologies Used

* Spring Boot 3.5.3
* MongoDB Atlas
* Java 17
* Maven
* Lombok


