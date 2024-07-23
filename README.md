# Nebula

Nebula api serves as a backend for managing cohort statistics, attendance, and student information. The application exposes various endpoints to retrieve and manage data related to cohorts and students.

## Endpoints

### Cohort Statistics

- **GET `/api/cohort/stats/{cohort_name}`**

  Retrieves statistical information about the specified cohort.

  **Parameters:**
  - `cohort_name` (str): The name of the cohort.

  **Response:**
  - JSON object containing cohort statistics.

### Cohort Attendance

- **GET `/api/cohort/attendance/{cohort_name}`**

  Retrieves attendance records for the specified cohort.

  **Parameters:**
  - `cohort_name` (str): The name of the cohort.

  **Response:**
  - JSON object containing attendance records.

### Student Information

- **GET `/api/students`**

  Retrieves a list of all students.

  **Response:**
  - JSON array of student objects.

- **GET `/api/students/{email}`**

  Retrieves information about a specific student using their email address.

  **Parameters:**
  - `email` (str): The email address of the student.

  **Response:**
  - JSON object containing student information.

### Health Check

- **GET `/api/health_check`**

  Checks the health status of the application.

  **Response:**
  - JSON object indicating the health status of the application.

### Database Connection Test

- **GET `/api/test_db_connection`**

  Tests the connection to the database.

  **Response:**
  - JSON object indicating the status of the database connection.

## Getting Started

### Prerequisites

- Python 3.7+
- FastAPI
- Uvicorn

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/CalebYeboah27/Nebula.git
   cd Nebula
   ```

2. Create and activate a virtual environment:

   ```bash
   python3 -m venv env
   source env/bin/activate  # On Windows use `env\Scripts\activate`
   ```

3. Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

### Running the Application

To start the server, run the following command:

```bash
uvicorn app.main:app --reload
```

The application will be available at `http://127.0.0.1:8000`.

## Project Structure

```
.
├── app
│   ├── main.py            # Entry point of the application
│   ├── routers            # Directory containing route definitions
│   │   ├── cohort.py      # Routes related to cohorts
│   │   ├── student.py     # Routes related to students
│   ├── models             # Directory containing data models
│   ├── services           # Directory containing business logic
│   └── db                 # Directory containing database related code
├── requirements.txt       # List of dependencies
├── README.md              # This file
└── ...
```

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

Feel free to customize this README file according to your specific requirements and project details.