# School Sphere - MERN Stack School Management System

A comprehensive school management application built with the MERN stack (MongoDB, Express.js, React.js, Node.js) that simplifies administrative data management for schools.

## 📋 Table of Contents

- [Features](#features)
- [Technology Stack](#technology-stack)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Database Models](#database-models)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## ✨ Features

### General Zone (Public Pages)
- **Home**: Landing page with responsive slider and key highlights
- **About Us**: School information, history, mission, values, and goals
- **Facility**: School infrastructure, classrooms, laboratories, library, sports areas
- **Contact Us**: Complete address, phone, email, and map integration
- **Enquiry**: Interactive form for parents/students to ask questions

### Admin Zone (URL-Only Access)
- **Manage Students**: Complete student record management (add, view, update, delete)
- **Manage Enquiries**: Handle and track enquiries from prospective students
- **Manage Contacts**: View and manage contact messages from the website

### Core Functionality
- Student registration and management
- Enquiry form submission and tracking
- Contact form with backend storage
- Responsive design for all devices
- Secure data handling
- URL-only admin access (no navigation links)

## 🛠 Technology Stack

### Frontend
- **React.js** - UI library
- **React Router** - Client-side routing
- **Bootstrap** - CSS framework
- **Axios** - HTTP client
- **Font Awesome** - Icons

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - NoSQL database
- **Mongoose** - ODM for MongoDB

### Development Tools
- **Vite** - Build tool
- **ESLint** - Code linting
- **npm** - Package manager

## 📋 Prerequisites

Before running this application, make sure you have the following installed:

- **Node.js** (v16 or higher)
- **MongoDB** (v4.4 or higher)
- **npm** or **yarn**

## 🚀 Installation

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/school-sphere.git
cd school-sphere
```

### 2. Backend Setup
```bash
cd Back-end
npm install
```

### 3. Frontend Setup
```bash
cd ../Front-end/school-sphere
npm install
```

## ⚙️ Configuration

### Environment Variables

Create a `.env` file in the `Back-end` directory:

```env
PORT=5000
MONGODB_URI=mongodb://localhost:27017/School_spheredb
```

### MongoDB Setup

1. Start MongoDB service
2. The application will automatically create the database and collections

## 📖 Usage

### Development Mode

#### Start Backend Server
```bash
cd Back-end
npm start
```
Server will run on `http://localhost:5000`

#### Start Frontend Development Server
```bash
cd Front-end/school-sphere
npm run dev
```
Frontend will run on `http://localhost:5173`

### Production Build

#### Build Frontend
```bash
cd Front-end/school-sphere
npm run build
```

#### Start Production Server
```bash
cd Back-end
npm start
```

## 🔗 API Endpoints

### Student Management
- `POST /addstudent` - Add new student
- `GET /allstudents` - Get all students
- `GET /student/:id` - Get student by ID
- `PUT /updatestudent/:id` - Update student
- `DELETE /deletestudent/:id` - Delete student

### Enquiry Management
- `POST /addenquiry` - Add new enquiry
- `GET /allenquiries` - Get all enquiries
- `GET /enquiry/:id` - Get enquiry by ID
- `DELETE /deleteenquiry/:id` - Delete enquiry

### Contact Management
- `POST /addcontact` - Add new contact message
- `GET /allcontacts` - Get all contact messages
- `DELETE /deletecontact/:id` - Delete contact message

## 📊 Database Models

### Student Model
```javascript
{
  name: String,
  age: Number,
  gender: String,
  contact: String,
  email: String,
  class: String
}
```

### Enquiry Model
```javascript
{
  parentName: String,
  studentName: String,
  email: String,
  phone: String,
  grade: String,
  enquiryType: String,
  message: String,
  createdAt: Date
}
```

### Contact Model
```javascript
{
  fullName: String,
  email: String,
  message: String,
  createdAt: Date
}
```

## 📁 Project Structure

```
school-sphere/
├── Back-end/
│   ├── models/
│   │   ├── SRegister.js      # Student model
│   │   ├── Enquiry.js        # Enquiry model
│   │   └── Contact.js        # Contact model
│   ├── index.js              # Main server file
│   └── package.json
├── Front-end/
│   └── school-sphere/
│       ├── public/
│       ├── src/
│       │   ├── components/
│       │   │   ├── Common/
│       │   │   │   ├── Footer.jsx
│       │   │   │   ├── Header.jsx
│       │   │   │   ├── NavBar.jsx
│       │   │   │   └── SliderSection.jsx
│       │   │   ├── manage/
│       │   │   │   ├── ManageStudent.jsx
│       │   │   │   ├── ManageEnquiry.jsx
│       │   │   │   └── ManageContact.jsx
│       │   │   ├── AboutUs.jsx
│       │   │   ├── ContactUs.jsx
│       │   │   ├── Enquiry.jsx
│       │   │   ├── Enquiries.jsx
│       │   │   ├── Facility.jsx
│       │   │   ├── Gallery.jsx
│       │   │   ├── Home.jsx
│       │   │   ├── Registration.jsx
│       │   │   ├── main.jsx
│       │   │   └── App.jsx
│       ├── package.json
│       └── vite.config.js
├── README.md
└── TODO.md
```

## 🎯 Key Features Implementation

### Admin Zone Access
Admin pages are accessible only via direct URLs:
- `/ManageStudent` - Student management
- `/ManageEnquiry` - Enquiry management
- `/ManageContact` - Contact message management

### Form Submissions
- All forms (Registration, Enquiry, Contact) submit data to backend APIs
- Success/error messages displayed to users
- Form validation implemented

### Responsive Design
- Bootstrap framework for responsive layout
- Mobile-friendly navigation and forms
- Optimized for all screen sizes

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Authors

- **Syntax_Squad** - *Initial work*

## 🙏 Acknowledgments

- Bootstrap for responsive design
- Font Awesome for icons
- React community for excellent documentation
- MongoDB for reliable database solutions

---

**Note**: This application is designed for educational purposes and school management. Make sure to configure proper security measures before deploying to production.
