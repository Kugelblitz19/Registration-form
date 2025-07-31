# Registration-form
📌 Overview
This project is a Signup and Login system with OTP-based authentication over email, built using React.js (frontend) and Spring Boot (backend). It provides secure user authentication using email OTP verification during signup and login.

🚀 Features
✅ User Registration with email verification
✅ Login with OTP sent to registered email
✅ Secure Password Hashing (BCrypt)
✅ OTP Generation & Expiry Validation
✅ REST API with Spring Boot & JPA
✅ Frontend built with React.js and Axios for API calls

🛠 Tech Stack
Frontend:
React.js

Axios (for API calls)

React Router

Backend:
Java 17 + Spring Boot

Spring Security (for authentication)

Spring Data JPA + MySQL

JavaMailSender (for email OTP)

📂 Project Structure
bash
Copy
Edit
signup-login-otp/
│
├── backend/ (Spring Boot App)
│   ├── entity/      # User, OTP Entities
│   ├── repository/  # JPA Repositories
│   ├── service/     # Business Logic
│   ├── controller/  # REST Endpoints
│   └── util/        # OTP Generator, Email Sender
│
├── frontend/ (React App)
│   ├── src/
│   │   ├── components/ # Signup, Login, OTP Form
│   │   ├── pages/      # Page Components
│   │   └── api.js      # Axios API functions
│
└── README.md
⚙️ Setup Instructions
🔹 Backend Setup
1️⃣ Clone the repository

bash
Copy
Edit
git clone https://github.com/your-repo/signup-login-otp.git
cd signup-login-otp/backend
2️⃣ Update application.properties

properties
Copy
Edit
spring.datasource.url=jdbc:mysql://localhost:3306/otp_auth
spring.datasource.username=root
spring.datasource.password=yourpassword
spring.mail.host=smtp.gmail.com
spring.mail.port=587
spring.mail.username=youremail@gmail.com
spring.mail.password=your-app-password
3️⃣ Run the backend

bash
Copy
Edit
mvn spring-boot:run
🔹 Frontend Setup
1️⃣ Navigate to frontend folder

bash
Copy
Edit
cd signup-login-otp/frontend
2️⃣ Install dependencies

bash
Copy
Edit
npm install
3️⃣ Start React App

bash
Copy
Edit
npm start
🔑 API Endpoints
Method	Endpoint	Description
POST	/auth/signup	Register new user
POST	/auth/login	Login & send OTP to email
POST	/auth/verify-otp	Verify OTP & authenticate

📬 How It Works
1️⃣ User signs up → Backend sends OTP to email for verification
2️⃣ On login, backend generates OTP and sends to registered email
3️⃣ User enters OTP → If valid & not expired, login is successful

📜 License
This project is free to use for learning and development purposes.
