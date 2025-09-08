
# CampusLife - College Extracurricular Hub

A comprehensive web application for college students to explore and engage with extracurricular activities, including events, clubs, sports, workshops, and more. This project features a dynamic frontend with a robust backend API.

## 🚀 Features

- **Dynamic Content**: Interactive sections for events, clubs, sports, achievements, workshops, talent showcase, social service, festivals, and competitions.
- **Search Functionality**: Global search across all content sections.
- **Form Submissions**: Registration forms for events, clubs, workshops, and general inquiries.
- **Modal Interactions**: Seamless modal popups for forms, tests, and messages.
- **Responsive Design**: Mobile-friendly layout with hamburger menu and smooth scrolling.
- **RESTful API**: Backend endpoints for form submissions and data retrieval with search, filtering, and pagination.
- **CORS Enabled**: Cross-origin resource sharing for frontend-backend communication.

## 🛠 Tech Stack

### Frontend
- **HTML5**: Semantic markup for structure.
- **CSS3**: Custom styling with responsive design.
- **JavaScript (ES6+)**: Dynamic content population, event handling, and API interactions.

### Backend
- **Node.js**: Runtime environment.
- **Express.js**: Web framework for API development.
- **Body-parser**: Middleware for parsing JSON requests.
- **CORS**: Middleware for handling cross-origin requests.

### Development Tools
- **Nodemon**: For development server with auto-restart.
- **Font Awesome**: Icons for UI elements.
- **Google Fonts**: Poppins font for typography.

## 📁 Project Structure

```
campuslife-backend/
├── public/
│   ├── index.html          # Main HTML file
│   ├── scripts15.js        # Frontend JavaScript
│   └── styles12.css        # CSS styles
├── server.js               # Backend server
├── package.json            # Dependencies and scripts
├── package-lock.json       # Lockfile for dependencies
├── setup_and_run_backend_frontend.bat  # Windows batch script for setup
└── README.md               # This file
```

## 🔧 Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/campuslife-backend.git
   cd campuslife-backend
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Start the development server**:
   ```bash
   npm run dev
   ```

4. **Or start the production server**:
   ```bash
   npm start
   ```

The server will run on `http://localhost:3000`.

## 📖 Usage

1. Open your browser and navigate to `http://localhost:3000`.
2. Explore different sections using the navigation menu.
3. Use the search bar to find specific content.
4. Click on registration buttons to open forms and submit data.
5. The backend will handle form submissions and store them in memory.

## 🔌 API Endpoints

### POST /api/submit-form
Submit form data (e.g., registrations, inquiries).

**Request Body**:
```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "message": "Optional message"
}
```

**Response**:
```json
{
  "message": "Submission successful!",
  "data": { ... }
}
```

### GET /api/submissions
Retrieve submissions with optional search, filtering, and pagination.

**Query Parameters**:
- `search`: Search term for name or email
- `page`: Page number (default: 1)
- `limit`: Items per page (default: 10)

**Example**: `GET /api/submissions?search=john&page=1&limit=5`

**Response**:
```json
{
  "total": 100,
  "page": 1,
  "limit": 5,
  "data": [ ... ]
}
```

## 🧪 Testing

### Manual Testing
Use tools like Postman or curl to test API endpoints:

```bash
# Test form submission
curl -X POST http://localhost:3000/api/submit-form \
  -H "Content-Type: application/json" \
  -d '{"name":"Test User","email":"test@example.com"}'

# Test submissions retrieval
curl "http://localhost:3000/api/submissions?page=1&limit=10"
```

### Automated Testing
Add testing frameworks like Jest for unit and integration tests.

## 🚀 Deployment

1. **Build for production**:
   - Ensure all dependencies are installed.
   - Use a process manager like PM2 for production.

2. **Environment Variables**:
   - Set `PORT` for custom port (default: 3000).

3. **Hosting Options**:
   - Deploy backend to Heroku, Vercel, or AWS.
   - Serve static files from a CDN for better performance.

## 🤝 Contributing

1. Fork the repository.
2. Create a feature branch: `git checkout -b feature-name`.
3. Commit changes: `git commit -am 'Add new feature'`.
4. Push to branch: `git push origin feature-name`.
5. Submit a pull request.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Contact

For questions or support, please open an issue on GitHub or contact the maintainers.

---

**Note**: This is a demo project using in-memory storage. For production use, integrate a proper database like MongoDB or PostgreSQL.
