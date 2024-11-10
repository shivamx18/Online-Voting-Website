# Online Voting Website

A Java-based online voting platform with a secure and intuitive interface for users to cast votes in real time. This project aims to create a smooth digital voting experience, leveraging a structured backend, frontend design, and SQL database for efficient data handling.

## Project Structure and Approach

### Backend (Java)

The backend is developed in Java, focusing on modular classes for core components of the voting system. 

- **Classes**:
  - **Admin.java**: Manages administrator functions, such as adding or removing candidates, viewing results, and overseeing user registration.
  - **Candidate.java**: Represents each candidate with attributes like name, party, and vote count, allowing for easy storage and retrieval of candidate details.
  - **Vote.java**: Handles individual vote submissions, linking users to their selected candidates and recording the votes.

- **Approach**:
  - Each Java class encapsulates specific functionalities, making the system modular and easy to maintain.
  - Business logic for managing users, voting processes, and vote counting is implemented in these Java files.
  - The backend connects to an SQL database to handle data persistence and retrieval.

### Frontend (HTML, CSS, JavaScript)

The frontend is designed to be user-friendly and responsive, built with HTML, CSS, and JavaScript.

- **Pages**:
  - **Login/Register**: Simple forms for user authentication, allowing secure access to the voting system.
  - **Vote Page**: Displays available candidates, letting users submit their vote in a few clicks.
  - **Confirmation Page**: Confirms a successful vote submission with a thank-you message.

- **Approach**:
  - The frontend captures and validates user input using JavaScript before sending it to the backend.
  - AJAX is used for smooth, asynchronous data submission to the backend, ensuring a responsive user experience.
  - CSS is used to style each page, creating a cohesive and modern design across devices.

### Database (SQL)

An SQL database is used to store and manage data securely and efficiently. The database structure includes tables for users, candidates, votes, and admin information.

- **Database Tables**:
  - **Users**: Stores user credentials and profile information.
  - **Candidates**: Contains candidate details such as ID, name, party, and vote count.
  - **Votes**: Records each user’s vote, linking it to their ID and selected candidate.
  - **Admin**: Holds administrator credentials and permissions.

- **Approach**:
  - Data integrity is ensured with foreign key constraints, especially in linking votes to users and candidates.
  - Efficient queries handle high volumes of data quickly, particularly during vote retrieval and result tallying.
  - The database is optimized for quick read/write operations to handle voting sessions seamlessly.
