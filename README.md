Here’s the updated **README.md** file reflecting the frontend and backend branches (`Quiz-App-frontend` and `Quiz-App-backend`):  

---

# Quiz App  

This project is a full-stack Quiz Application developed during an internship at InnoByte Services. It is divided into two parts:  
- **Frontend**: Located in the `Quiz-App-frontend` branch, built with React, Vite, and Tailwind CSS.  
- **Backend**: Located in the `Quiz-App-backend` branch, built with Spring Boot.  

## Frontend  

The frontend is built with **React**, **Vite**, and **Tailwind CSS**, providing a modern and responsive user interface for managing and participating in quizzes.  

### Features  

- View questions  
- Add new questions  
- Delete questions  
- Update questions  
- Create quizzes  
- Submit quizzes and view results  

### Technologies Used  

- **React + Vite**  
- **React Router**  
- **Axios**  
- **Tailwind CSS**  

### API Integration  

The frontend communicates with the backend via RESTful APIs. API methods are configured in `src/api/api.js`.  

#### Example API Methods  

- `fetchAllQuestions()`  
- `addQuestion(question)`  
- `deleteQuestion(id)`  
- `updateQuestion(id, question)`  
- `createQuiz(category, numQ, title)`  
- `getQuizById(id)`  
- `submitQuiz(id, responses)`  
- `getQuizzes()`  

### Running the Frontend  

1. Navigate to the `Quiz-App-frontend` branch:  
   ```bash  
   git checkout Quiz-App-frontend  
   ```  

2. Install dependencies:  
   ```bash  
   npm install  
   ```  

3. Start the development server:  
   ```bash  
   npm run dev  
   ```  

The frontend will start on `http://localhost:5173`.  

---

## Backend  

The backend is built with **Spring Boot**, providing RESTful APIs for managing quizzes and questions.  

### Features  

- Fetch all questions  
- Add a new question  
- Delete a question  
- Update a question  
- Create quizzes  
- Fetch quizzes by ID  
- Submit quizzes and get results  

### Technologies Used  

- **Spring Boot**  
- **JPA/Hibernate**  
- **MySQL**  
- **Lombok**  
- **Maven**  

### Running the Backend  

1. Navigate to the `Quiz-App-backend` branch:  
   ```bash  
   git checkout Quiz-App-backend  
   ```  

2. Configure the database by editing `application.properties`:  

   ```properties  
   spring.application.name=quizapp  
   spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver  
   spring.datasource.url=jdbc:mysql://127.0.0.1:3306/quizapp  
   spring.datasource.username=root  
   spring.datasource.password=Kunal123  
   spring.jpa.hibernate.ddl-auto=update  
   spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQLDialect  
   ```  

3. Build the backend:  
   ```bash  
   mvn clean install  
   ```  

4. Start the backend server:  
   ```bash  
   mvn spring-boot:run  
   ```  

The backend server will start on `http://localhost:8080`.  

### API Endpoints  

#### Question Endpoints  

- **Get all questions**: `GET /question/allQuestions`  
- **Add a new question**: `POST /question/add`  
  **Request Body**:  
  ```json  
  {  
    "questionTitle": "What is Java?",  
    "option1": "Programming Language",  
    "option2": "Operating System",  
    "option3": "Web Browser",  
    "option4": "Database",  
    "rightAnswer": "Programming Language",  
    "difficultyLevel": "Easy",  
    "category": "Programming"  
  }  
  ```  

---

## Branch Structure  

- **`Quiz-App-frontend`**: Contains all files related to the frontend of the application.  
- **`Quiz-App-backend`**: Contains all files related to the backend of the application.  

---

## Prerequisites  

Make sure you have the following installed:  
- **Java 21.0.2**  
- **MySQL**  
- **Node.js and npm**  

---

## Conclusion  

This project leverages modern technologies like React, Vite, Tailwind CSS, Spring Boot, and MySQL to deliver a robust and user-friendly quiz management system.