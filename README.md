# Craftsmen and Small Business Network

**A full-stack platform connecting skilled craftspeople with clients through professional profiles, job opportunities, and direct communication.**

**Computer Science Capstone Project | Lebanese American University (LAU)**

## The Problem

Skilled craftspeople and small service providers often struggle to reach potential customers, while clients may find it difficult to discover suitable professionals, compare their expertise, and manage service requests in one place.

This creates several challenges:
- **Limited visibility:** Craftspeople need an accessible way to showcase their skills, experience, and availability.
- **Fragmented job opportunities:** Clients and service providers need a structured way to publish, discover, and respond to work requests.
- **Disconnected communication:** Discussions, applications, and updates can become difficult to track across separate channels.
- **Limited product discovery:** Small businesses can benefit from easier ways for customers to find items and related offerings.

## Our Solution

**Craftsmen and Small Business Network** brings these interactions into a centralized digital platform. It enables clients to discover craftspeople, review profiles, publish jobs, and communicate with applicants, while giving service providers tools to showcase their work and pursue new opportunities.

The broader capstone also addressed small-business product discovery through an AI-assisted visual matching feature.

## Project Screenshots

The screenshots below are from the Craftsmen Network application documented in my LAU internship report.

### Explore Craftspeople

Browse skilled professionals by trade or search for a particular service.

![Craftsmen Network directory showing searchable trade categories](screenshots/01-craftsmen-directory.png)

### Post a Job Announcement

Clients can create service requests with a description, location, budget, deadline, and contact details.

![Job announcement form with job details and a submission button](screenshots/02-post-job-announcement.png)

### Manage Job Announcements

Users can review their published requests, inspect applicants, and manage listings.

![My Announcements page showing job cards and management controls](screenshots/03-manage-announcements.png)

### Track Applications

Craftspeople can review the jobs they applied to and manage submitted applications.

![My Applications table showing submitted job requests and application actions](screenshots/04-track-applications.png)

## Key Features

### Accounts and Professional Profiles
- User registration, login, and profile management
- Dedicated experiences for clients and craftspeople
- Profiles displaying skills, experience, and professional information
- Authentication and account-related email workflows

### Job Discovery and Applications
- Browse available craftspeople and service categories
- Create and manage job announcements
- Apply to relevant opportunities
- Review applicants and track applications

### Messaging and Community
- User conversations and direct messaging
- Real-time communication components using Socket.IO and WebSockets
- Community posts, comments, and interactions

### Administration
- Administrative dashboards
- User management tools
- Content moderation interfaces

### AI-Assisted Visual Product Matching

An **AI-assisted image-matching feature** for product discovery. The feature was designed to let users provide a product image and discover identical or visually similar items from small-business offerings.


## Technology Stack

| Area | Technologies |
| --- | --- |
| Frontend | HTML, CSS, JavaScript, Tailwind CSS |
| Backend | Node.js, Express.js |
| Database | MongoDB, Mongoose |
| Authentication | JWT, bcrypt |
| Real-time communication | Socket.IO, WebSocket components |
| Email and uploads | Nodemailer, Multer |
| Development tools | Git, GitHub, npm, Vite configuration |

## Project Structure

```text
Craftsmen-Small-Business-Network/
├── backend/
│   ├── middleware/       # Upload and request-handling utilities
│   ├── models/           # MongoDB / Mongoose data models
│   ├── routes/           # API routes
│   ├── public/uploads/   # Default asset and upload directory
│   └── server.js         # Express server
├── frontend/
│   ├── assets/           # Images and visual assets
│   ├── js/               # Client-side scripts
│   ├── pages/            # Web application pages
│   ├── style/            # Styling and page assets
│   └── vite.config.ts    # Frontend tooling configuration
├── screenshots/       # Interface images used in this README
├── .gitignore
└── README.md
```

## Getting Started

### Requirements
- Node.js and npm
- MongoDB connection

### 1. Clone the repository

```bash
git clone https://github.com/talahareb/Craftsmen-Small-Business-Network.git
cd Craftsmen-Small-Business-Network/backend
```

### 2. Install backend dependencies

```bash
npm install
```

### 3. Configure your local environment

Create a local `backend/.env` using `backend/.env.example` as a template:

```dotenv
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_value
EMAIL_USER=your_email_address
EMAIL_PASS=your_email_app_password
PORT=5001
```

Keep real credentials in your local `.env`, never in Git.

### 4. Start the backend

```bash
node server.js
```

Then open `http://localhost:5001` (or your configured port). Some development environments may require additional local configuration.

## Further Development

The project can be extended with:
- Expanded small-business marketplace capabilities
- Broader Arabic–English localization
- Geolocation-based discovery of nearby craftspeople
- Availability calendars and service booking
- Automated recommendations matching service requests with relevant professionals

## Academic Context

Developed as a Computer Science capstone project at **Lebanese American University (LAU)**.

**Acknowledgment:** The original capstone proposal credits Tala Hareb and Abdulaziz Al Sayyed.
