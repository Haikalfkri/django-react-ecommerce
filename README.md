# Django React E-Commerce

A full-stack e-commerce web application built with **Django REST Framework** and **React**. The project separates the backend API from the frontend application, providing a foundation for an online shopping experience with a modern web interface and a Python-based backend.

## Overview

Django React E-Commerce demonstrates full-stack development using a RESTful API architecture. The backend handles server-side logic and data management, while the React frontend provides the user interface.

## Tech Stack

### Backend
- **Python** — Backend programming language
- **Django** — Web framework
- **Django REST Framework** — REST API development
- **SimpleJWT** — JWT authentication support
- **PostgreSQL** — Relational database support
- **Pillow** — Image processing

### Frontend
- **React** — Component-based user interface
- **Vite** — Frontend development server and build tool
- **React Router** — Client-side routing
- **Tailwind CSS** — Utility-first styling

## Architecture

The application uses a separated frontend and backend architecture.

```text
django-react-ecommerce/
├── backend/
│   ├── manage.py
│   ├── requirements.txt
│   └── ...
├── frontend/
│   ├── package.json
│   ├── src/
│   └── ...
└── README.md
```

```text
User → React Frontend → Django REST Framework API → Database
```

The frontend communicates with the backend through HTTP requests. Django REST Framework processes API requests and handles data operations.

## Key Capabilities

- **Product catalog foundation** — Supports the development of product browsing experiences.
- **RESTful API** — Backend API architecture for communication between frontend and backend.
- **Authentication support** — JWT authentication dependencies are included in the backend stack.
- **Responsive frontend foundation** — React interface styled with Tailwind CSS.
- **Client-side routing** — Navigation managed with React Router.
- **Database support** — PostgreSQL support for relational data storage.

> The exact availability of individual shopping features depends on the current implementation in the source code. Features such as payment processing or order management should only be listed as implemented if they are present in the repository.

## Getting Started

### Prerequisites

Install the following tools:
- Python
- Node.js and npm
- PostgreSQL, if using a PostgreSQL database

### 1. Clone the Repository

```bash
git clone https://github.com/Haikalfkri/django-react-ecommerce.git
cd django-react-ecommerce
```

### 2. Set Up the Backend

```bash
cd backend
python -m venv venv
```

Activate the virtual environment.

**Windows:**

```powershell
venv\Scripts\activate
```

**macOS / Linux:**

```bash
source venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

### 3. Configure Environment Variables

If the project settings use environment variables, create a `.env` file in the backend directory. For example:

```env
SECRET_KEY=your-secret-key
DEBUG=True
```

Configure database connection settings to match the backend settings and your local PostgreSQL setup. Use the actual variable names expected by the project.

**Security:** Never commit production secrets, database passwords, or private credentials to version control.

### 4. Apply Database Migrations

From the `backend` directory, run:

```bash
python manage.py migrate
```

To create an administrator account if needed:

```bash
python manage.py createsuperuser
```

### 5. Start the Backend Server

```bash
python manage.py runserver
```

The backend development server will be available at:

http://127.0.0.1:8000/

### 6. Set Up the Frontend

Open a separate terminal and navigate to the frontend directory from the repository root:

```bash
cd frontend
npm install
npm run dev
```

Open the local URL printed by Vite in your terminal.

### 7. Configure Frontend API Access

Ensure the frontend API base URL points to the backend server. If the frontend and backend run on different origins, configure Django CORS settings to allow the frontend development origin. Use the API URL and environment variable names expected by the existing project.

## Development Commands

### Backend

Run the Django development server:

```bash
python manage.py runserver
```

Create and apply migrations after changing Django models:

```bash
python manage.py makemigrations
python manage.py migrate
```

### Frontend

Start the development server:

```bash
npm run dev
```

Run the linter, if configured in `package.json`:

```bash
npm run lint
```

Create a production build:

```bash
npm run build
```

## Security Considerations

- Keep secret keys and credentials in environment variables.
- Restrict CORS to trusted origins in production.
- Apply appropriate authentication and authorization to protected API endpoints.
- Set `DEBUG=False` and configure production security settings before deployment.
- Use secure database credentials and access controls.

## Potential Future Improvements

Possible enhancements include:
- Product search, filtering, and category navigation
- Shopping cart and checkout workflows
- Order history and order management
- Product reviews and ratings
- Payment gateway integration
- Automated tests and continuous integration
- Production deployment and monitoring

These are potential improvements, not a claim that they are currently implemented.

## License

No license is specified in this README. Add a `LICENSE` file and update this section if you intend to distribute the project under an open-source license.

---

Built as a full-stack web development project using Django REST Framework and React.
