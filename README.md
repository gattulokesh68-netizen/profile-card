# Profile Card Generator

A form-based web application that allows users to create and display profile cards. Users input their name, bio, and image URL through a form, and the backend processes this data to return a formatted profile card on the frontend.

## Features

- **User Input Form**: Collect name, bio, and image URL from users
- **Backend Processing**: Express.js server validates and processes form data via POST requests
- **Profile Card Display**: Beautifully formatted profile card with image, name, and bio
- **Error Handling**: Client-side and server-side validation with user-friendly error messages
- **Responsive Design**: Works seamlessly on desktop and mobile devices
- **Real-time Feedback**: Immediate visual feedback when cards are generated

## Tech Stack

- **Frontend**: HTML, CSS, JavaScript
- **Backend**: Node.js, Express.js
- **Middleware**: CORS, Body Parser

## Installation

1. Clone the repository:
```bash
git clone https://github.com/gattulokesh68-netizen/rofile-card.git
cd rofile-card
```

2. Install dependencies:
```bash
npm install
```

3. Start the server:
```bash
npm start
```

4. Open your browser and navigate to:
```
http://localhost:3000
```

## Development

To run the server with auto-reload during development:
```bash
npm run dev
```

## How It Works

### Frontend Flow
1. User fills out the form with name, bio, and image URL
2. Form submission triggers a POST request to `/api/profile`
3. Backend validates the data
4. Upon successful response, the profile card is displayed in the preview section

### Backend Flow
1. Express server receives POST request at `/api/profile` endpoint
2. Validates required fields (name, bio, imageUrl)
3. Validates image URL format
4. Returns formatted profile card data with timestamp
5. Handles errors gracefully with appropriate HTTP status codes

## API Endpoints

### POST /api/profile
Creates and returns a formatted profile card

**Request Body:**
```json
{
  "name": "John Doe",
  "bio": "Software developer and tech enthusiast",
  "imageUrl": "https://example.com/image.jpg"
}
```

**Success Response (200):**
```json
{
  "success": true,
  "data": {
    "name": "John Doe",
    "bio": "Software developer and tech enthusiast",
    "imageUrl": "https://example.com/image.jpg",
    "createdAt": "2026-06-30T12:00:00.000Z"
  }
}
```

**Error Response (400/500):**
```json
{
  "success": false,
  "error": "Error message describing what went wrong"
}
```

## Project Structure

```
rofile-card/
├── server.js           # Express server and API endpoints
├── package.json        # Dependencies and scripts
├── .gitignore         # Git ignore rules
├── README.md          # This file
└── public/
    ├── index.html     # HTML form and card layout
    ├── styles.css     # Responsive styling
    └── script.js      # Frontend JavaScript and form handling
```

## Features Details

### Form Validation
- Required field validation
- URL format validation for image URLs
- Client-side and server-side validation

### Card Display
- Animated card appearance
- Hover effects for interactivity
- Responsive image sizing
- Formatted timestamp display

### Error Handling
- User-friendly error messages
- HTTP status codes (400 for validation errors, 500 for server errors)
- Console logging for debugging

## Future Enhancements

- Add image upload capability
- Implement database storage for profiles
- Add edit/delete functionality
- Create profile sharing feature
- Add more customization options (colors, themes)
- Implement user authentication

## License

MIT License

## Author

gattulokesh68-netizen
