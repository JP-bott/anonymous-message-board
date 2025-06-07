# Anonymous Message Board

A Free Code Camp Information Security project implementing an anonymous message board with threads, replies, and security features.

## Features

- **Thread Management**: Create, view, report, and delete threads
- **Reply System**: Add replies to threads with full functionality  
- **Security**: Helmet.js security headers implemented
- **Password Protection**: Secure deletion with password verification
- **Database Integration**: MongoDB with Mongoose schemas
- **API Structure**: RESTful endpoints following FCC specifications

## Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/JP-bott/anonymous-message-board.git
   cd anonymous-message-board
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   - Copy `.env.example` to `.env`
   - Update the MongoDB connection string in `.env`

4. **Start MongoDB**
   - Make sure MongoDB is running on your system
   - For Windows: `net start MongoDB`

5. **Run the application**
   ```bash
   npm start
   ```

6. **Run tests**
   ```bash
   NODE_ENV=test npx mocha tests/2_functional-tests.js --ui tdd --timeout 10000
   ```

## API Endpoints

### Threads
- `POST /api/threads/:board` - Create a new thread
- `GET /api/threads/:board` - Get recent threads with replies
- `PUT /api/threads/:board` - Report a thread
- `DELETE /api/threads/:board` - Delete a thread (with password)

### Replies
- `POST /api/replies/:board` - Create a new reply
- `GET /api/replies/:board` - Get a thread with all replies
- `PUT /api/replies/:board` - Report a reply
- `DELETE /api/replies/:board` - Delete a reply (with password)

## Usage

- Visit `http://localhost:3000` for the API testing interface
- Visit `http://localhost:3000/b/general/` for a board view
- All tests pass and functionality is fully implemented

## Technologies Used

- Node.js & Express.js
- MongoDB & Mongoose
- Helmet.js for security
- Mocha & Chai for testing

## Free Code Camp Project

This project fulfills all requirements for the FCC Information Security Anonymous Message Board challenge.
