# Craftsmen and Small Business Network

**A full-stack web platform connecting skilled craftspeople with clients and supporting local business communities.**

**Academic project:** Computer Science Capstone, Lebanese American University (LAU)  
**Project team:** Tala Hareb and Abdulaziz Al Sayyed

## Project Overview

The **Craftsmen and Small Business Network** aims to make skilled services easier to discover and access. Clients can explore craftsperson profiles, publish job opportunities, and communicate with potential service providers. Craftspeople can showcase their skills, browse opportunities, and apply to relevant jobs.

The broader capstone vision also included a small-business marketplace, bilingual Arabic–English access, and AI-assisted product discovery. These ideas are described in the original project proposals; the available repository snapshot contains the main network application and its frontend and backend code.

## Main Features

### User Accounts and Profiles
- Registration, login, and profile management
- Different user experiences for clients and craftspeople
- Skills and portfolio information for craftspeople
- Email-related authentication flows

### Craftsmen and Job Network
- Search and browse craftsperson profiles
- Create and view job announcements
- Submit applications and bids for available jobs
- Review applications and track their status

### Communication and Community
- Conversations and messaging between users
- Real-time communication components using Socket.IO and WebSockets
- Community posts, comments, and reactions

### Administration
- Administrative dashboard pages
- User management and content moderation interfaces

### AI-Assisted Visual Product Matching
The capstone also **included an AI-powered image-matching feature, according to the project team**. Its intended workflow allowed a user to upload an image of a product and find identical or visually similar items associated with small businesses.

**Repository note:** The AI model, inference code, or external matching-service integration is **not present in the available source-code snapshot**. Therefore, this README records the feature as part of the team's reported implementation, but does not claim that it can be reproduced or evaluated using the files in this repository. No particular model, library, or accuracy figure is asserted.

## Technology Stack

| Area | Technologies |
| --- | --- |
| Frontend | HTML, CSS, JavaScript, Tailwind CSS |
| Backend | Node.js, Express.js |
| Database | MongoDB, Mongoose |
| Authentication | JWT, bcrypt |
| Communication | Socket.IO, WebSocket components |
| Email and file uploads | Nodemailer, Multer |
| Development | Git, GitHub, npm; Vite configuration |

## Repository Structure

```text
Craftsmen-Small-Business-Network/
├── backend/
│   ├── middleware/       # Request handling and uploads
│   ├── models/           # MongoDB/Mongoose models
│   ├── routes/           # REST API endpoints
│   ├── public/uploads/   # Placeholder asset; user uploads excluded
│   └── server.js         # Express server and real-time communication
├── frontend/
│   ├── assets/           # Images and other assets
│   ├── js/               # Client-side JavaScript
│   ├── pages/            # Application pages
│   ├── style/            # Styles and page assets
│   └── vite.config.ts    # Frontend tooling configuration
└── package.json
```

## Running the Project Locally

**Prerequisites:** Node.js, npm, and a MongoDB database. These instructions describe the source structure; the application has not been independently tested on a clean machine for this README.

1. Clone the repository and open the backend folder:

   ```bash
   git clone https://github.com/talahareb/Craftsmen-Small-Business-Network.git
   cd Craftsmen-Small-Business-Network/backend
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Configure the environment variables used by the backend in a **local, untracked** `backend/.env` file:

   ```dotenv
   MONGODB_URI=your_mongodb_connection_string
   JWT_SECRET=your_secret_value
   EMAIL_USER=your_email_address
   EMAIL_PASS=your_email_credential
   PORT=5001
   ```

4. Start the backend:

   ```bash
   node server.js
   ```

5. Open `http://localhost:5001` in your browser, or use your configured port.

**Setup note:** `server.js` imports the `ws` package, which is not listed as a direct dependency in the archived backend `package.json`. A local setup might therefore require installing that package separately.

## Project Scope and Future Work

The capstone proposals also identify possible extensions, including:

- Expanded small-business marketplace and collaboration features
- Full Arabic–English localization
- Geolocation-based discovery of nearby service providers
- Craftspeople availability calendars and appointment scheduling
- Automated matching of job requests to relevant service providers

These are **proposed or future capabilities** unless otherwise indicated above. The reported AI visual product-matching feature is listed separately under Main Features rather than as a future idea.

## Academic Context and Credits

This project was developed as a Computer Science capstone at **Lebanese American University**, with **Tala Hareb and Abdulaziz Al Sayyed** credited in the project proposal.

The README distinguishes the original project vision, components represented in the archived source code, and AI functionality reported by the project team. Individual contributions are not assigned beyond what the supplied project documents establish.

## Security and Data Handling

This public-facing source snapshot intentionally excludes the original `backend/.env`, generated dependencies, and previous user-uploaded files. Use `backend/.env.example` as a template, and never commit working secrets or personal data. Any original credentials that are still valid should be rotated or revoked before publishing, even though they are not included here.

This is an academic demonstration, not a production security-hardened application. Its runtime features have not been independently tested in a fresh environment; running it requires local configuration. The project also includes third-party-style illustrative images whose redistribution rights should be checked before public release.
