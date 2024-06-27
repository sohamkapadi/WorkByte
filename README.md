# WorkByte

Welcome to **WorkByte**! This is a job seeking/posting application with a role-based login system. Employers can manage job postings and review applications, while job seekers can search for jobs and apply for them.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Contributing](#contributing)
- [License](#license)

## Features

### Employer Features

1. **View All Jobs**: Employers can view all job postings.
2. **Post a New Job Profile**: Employers can create new job postings.
3. **Review Applications**: Employers can review applications submitted by job seekers.
4. **Edit Job Postings**: Employers can update the details of their job postings.
5. **Delete Job Postings**: Employers can delete job postings they have created.
6. **Mark Job as Expired**: Employers can mark job postings as expired to temporarily hide them.

### Job Seeker Features

1. **View All Jobs**: Job seekers can browse through all available job postings.
2. **Apply for a Job**: Job seekers can submit applications for job postings.
3. **Upload Resume**: Job seekers can upload their resumes for applications.
4. **Review Applications**: Job seekers can view and manage their submitted applications.
5. **Delete Application**: Job seekers can delete their applications if needed.

## Installation

To run **WorkByte** locally, follow these steps:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/workbyte.git
   cd workbyte

2. **Install dependencies:**
# For backend (Node.js)
cd backend
npm install

# For frontend (React)
cd ../frontend
npm install

3. **Set up environment variables:**
   Create a .env file in the backend directory and add the following:

4. **Run the development servers:**
   # In backend directory
    npm run dev

   # In frontend directory
    npm run dev

## Usage
1. **Registration:** Users can sign up as either an employer or a job seeker.
2. **Login:** Users can log in based on their role.
3. **Employer Dashboard:** Employers can manage job postings and review applications.
4. **Job Seeker Dashboard:** Job seekers can browse jobs, apply, and manage applications.

## Front-End Routes
The application is built with React Router for navigation. Here are the routes available in WorkByte:

**/login:** Login page.
**/register:** Registration page.
**/:** Home page.
**/job/getall:** Page to view all job postings.
**/job/:id:** Page to view details of a specific job.
**/job/post:** Page to post a new job (Employer only).
**/job/me:** Page to view jobs posted by the logged-in employer.
**/application/:id:** Page to view a specific job application.
**/application/me:** Page to view the logged-in job seeker's applications.
 *: Not found page for undefined routes.

## API Endpoints
# Authentication
- **POST /api/auth/register:** Register a new user.
- **POST /api/auth/login:** Login for existing users.
- **GET /api/auth/logout:** Logout the currently logged-in user (requires authorization).
- **GET /api/auth/getuser:** Get details of the currently logged-in user (requires authorization).

# Jobs
- **GET /api/jobs/getall:** Get all job postings.
- **POST /api/jobs/post:** Create a new job posting (requires authorization).
- **GET /api/jobs/getmyjobs:** Get jobs posted by the logged-in employer (requires authorization).
- **PUT /api/jobs/update/:id:** Update a job posting (requires authorization).
- **DELETE /api/jobs/delete/:id:** Delete a job posting (requires authorization).
- **GET /api/jobs/:id:** Get details of a specific job (requires authorization).
  
# Applications
- **GET /api/applications/jobseeker/getall:** Get all applications submitted by the logged-in job seeker (requires authorization).
- **GET /api/applications/employer/getall:** Get all applications for jobs posted by the logged-in employer (requires authorization).
- **DELETE /api/applications/delete/:id:** Delete a job application (requires authorization).
- **POST /api/applications/post:** Submit a new application for a job (requires authorization).

## Contributing
We welcome contributions to WorkByte! Please follow these steps:
  1. Fork the repository.
  2. Create a new branch for your feature or bugfix.
  3. Commit your changes.
  4. Push your branch and open a pull request.
For major changes, please open an issue first to discuss what you would like to change.
