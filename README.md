# QR Code Generation & Scanning System

A full-stack MERN application for generating, scanning, and managing QR codes.

## Features

- User authentication (signup/login)
- Generate QR codes for URLs or text
- Scan QR codes using device camera
- View history of generated QR codes
- Download QR codes as images
- Copy QR code content to clipboard
- Share QR codes via email
- Filter QR codes by date range
- Paginated QR code history

## Tech Stack

- **Frontend:** React (Vite) + Material-UI + Axios
- **Backend:** Node.js + Express
- **Database:** MongoDB + Mongoose
- **Authentication:** JWT
- **QR Code Generation:** qrcode
- **QR Code Scanning:** react-qr-reader
- **Email:** Nodemailer

## Prerequisites

- Node.js (v14 or higher)
- MongoDB
- npm or yarn

## Setup Instructions

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd qr-code-system
   ```

2. Install server dependencies:
   ```bash
   cd server
   npm install
   ```

3. Install client dependencies:
   ```bash
   cd ../client
   npm install
   ```

4. Create environment variables:
   - Copy `.env.example` to `.env` in the server directory
   - Update the following variables:
     ```
     PORT=5000
     MONGODB_URI=your_mongodb_connection_string
     JWT_SECRET=your_jwt_secret
     EMAIL_USER=your_email@gmail.com
     EMAIL_PASS=your_email_app_password
     ```

5. Start the development servers:

   Server:
   ```bash
   cd server
   npm run dev
   ```

   Client:
   ```bash
   cd client
   npm run dev
   ```

6. Access the application:
   - Frontend: http://localhost:3000
   - Backend: http://localhost:5000

## API Endpoints

### Authentication
- `POST /api/auth/signup` - Register a new user
- `POST /api/auth/login` - Login user

### QR Codes
- `POST /api/qrcodes/generate` - Generate a new QR code
- `GET /api/qrcodes` - Get all QR codes (with pagination & filters)
- `DELETE /api/qrcodes/:id` - Delete a QR code
- `POST /api/qrcodes/:id/share` - Share QR code via email

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License. 