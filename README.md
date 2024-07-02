VeloChat

VeloChat is a secure, fast, and user-friendly chat application designed to facilitate real-time communication with robust security features. It supports encrypted messaging and file sharing, ensuring that your conversations remain private and secure.

Features
User Authentication: Secure login using an existing authentication server.
Real-time Messaging: Instant messaging with live updates and typing indicators.
File Sharing: Share images and MP4 videos with friends and colleagues.
Encryption: All chats and files are encrypted using AES encryption.
Message Expiry: Messages are deleted for users after 2 days, although they remain in the database for compliance purposes.
Database: MySQL for persistent data storage.
Tech Stack
Frontend: Angular
Backend: Java 17, Spring Boot, JPA
Database: MySQL
Security: AES encryption
Setup Instructions
Prerequisites
Node.js and npm installed
Java 17 installed
MySQL installed and running
Maven installed
Backend Setup
Clone the repository:

sh
Copy code
git clone https://github.com/yourusername/velochat.git
cd velochat/backend
Configure the MySQL database in src/main/resources/application.properties:

properties
Copy code
spring.datasource.url=jdbc:mysql://localhost:3306/velochat
spring.datasource.username=root
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update
Build and run the backend:

sh
Copy code
mvn clean install
mvn spring-boot:run
Frontend Setup
Navigate to the frontend directory:

sh
Copy code
cd ../frontend
Install dependencies:

sh
Copy code
npm install
Run the frontend server:

sh
Copy code
ng serve
Running the Application
Ensure the backend server is running on http://localhost:8080.
Open a browser and navigate to http://localhost:4200 to access the VeloChat frontend.
Setup and Run Script
Create a .bat file named setup_and_run.bat with the following content to automate the setup and running process:

bat
Copy code
@echo off
echo Setting up and running VeloChat...

REM Navigate to the backend directory and set up the backend
cd backend
echo Building backend...
mvn clean install

echo Running backend...
start cmd /k "mvn spring-boot:run"

REM Navigate to the frontend directory and set up the frontend
cd ../frontend
echo Installing frontend dependencies...
npm install

echo Running frontend...
start cmd /k "ng serve"

echo VeloChat setup complete. The backend is running on http://localhost:8080 and the frontend is running on http://localhost:4200

exit
To use the script:

Save the .bat file in the root directory of your project.
Double-click the .bat file to execute it. This will open two new terminal windows, one for the backend and one for the frontend.
Contributing
We welcome contributions from the community. To contribute:

Fork the repository.
Create a new branch (git checkout -b feature/your-feature).
Commit your changes (git commit -m 'Add some feature').
Push to the branch (git push origin feature/your-feature).
Open a Pull Request.
License
This project is licensed under the MIT License. See the LICENSE file for details.

Contact
For any queries or issues, please contact us at support@velochat.com.
