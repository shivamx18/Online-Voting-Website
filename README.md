# Online Voting Website

A Java-based online voting platform with a secure and intuitive interface for users to cast votes in real time. This project aims to create a smooth digital voting experience, leveraging a structured backend, frontend design, and SQL database for efficient data handling.

## Project Structure and Approach

### Backend (Java)

The backend is developed in Java, focusing on modular classes for core components of the voting system.

- **Classes**:
  - **Admin.java**: Manages administrator functions, such as adding or removing candidates, viewing results, and overseeing user registration.
  - **Candidate.java**: Represents each candidate with attributes like name, party, and vote count, allowing for easy storage and retrieval of candidate details.
  - **Voter.java**: Manages voter information, including authentication and eligibility checks.
  - **Vote.java**: Handles individual vote submissions, linking voters to their selected candidates and recording the votes.

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
  - CSS is used to style each page, creating a cohesive and modern design across devices.

### Database (SQL)

An SQL database is used to store and manage data securely and efficiently. The database structure includes tables for users, candidates, votes, and admin information.

- **Database Tables**:
  
  1. **Admin Table**:
     - Stores the details of the administrators who manage the voting process, including authentication.
     - **Fields**:
       - `admin_id` (INT, Primary Key) – Unique identifier for each admin.
       - `username` (VARCHAR) – Username of the admin.
       - `password` (VARCHAR) – Hashed password of the admin.
       - `first_name` (VARCHAR) – First name of the admin.
       - `last_name` (VARCHAR) – Last name of the admin.
       - `email` (VARCHAR) – Email address of the admin.
       - `created_at` (TIMESTAMP) – Timestamp of when the admin was created.

  2. **Candidate Table**:
     - Stores information about the candidates standing for election.
     - **Fields**:
       - `candidate_id` (INT, Primary Key) – Unique identifier for each candidate.
       - `first_name` (VARCHAR) – First name of the candidate.
       - `last_name` (VARCHAR) – Last name of the candidate.
       - `email` (VARCHAR) – Email address of the candidate.
       - `created_at` (TIMESTAMP) – Timestamp of when the candidate was added to the system.

  3. **Voter Table**:
     - Stores information about the eligible voters.
     - **Fields**:
       - `voter_id` (INT, Primary Key) – Unique identifier for each voter.
       - `username` (VARCHAR) – Username of the voter.
       - `password` (VARCHAR) – Hashed password of the voter.
       - `first_name` (VARCHAR) – First name of the voter.
       - `last_name` (VARCHAR) – Last name of the voter.
       - `email` (VARCHAR) – Email address of the voter.
       - `created_at` (TIMESTAMP) – Timestamp of when the voter was registered.

  4. **Vote Table**:
     - Records the votes cast by voters for the candidates.
     - **Fields**:
       - `vote_id` (INT, Primary Key) – Unique identifier for each vote record.
       - `voter_id` (INT, Foreign Key) – References `voter_id` in the **Voter Table**.
       - `candidate_id` (INT, Foreign Key) – References `candidate_id` in the **Candidate Table**.
       - `vote_timestamp` (TIMESTAMP) – Timestamp of when the vote was cast.

- **Approach**:
  - Data integrity is ensured with foreign key constraints, particularly in linking votes to voters and candidates.
  - Efficient queries handle high volumes of data quickly, especially during vote retrieval and result tallying.
  - The database is optimized for fast read/write operations to handle voting sessions seamlessly.
