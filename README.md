# Habit Tracker

A full-stack web application for tracking and maintaining daily, weekly, and monthly habits with visualization of progress and streaks.

## Features

- 👤 User authentication (register, login, logout)
- ✅ Create, complete, and delete habits
- 📊 Track streaks and progress
- 📈 Visualize habit completion with charts
- 📱 Responsive design

## Tech Stack

- **Frontend**: EJS templates, Bootstrap 5, Chart.js
- **Backend**: Node.js, Express.js
- **Database**: Supports both MongoDB and Apache Cassandra
- **Authentication**: Session-based with bcrypt password hashing

## Project Structure

```
habit-tracker/
├── config/
│   └── db.js             # Database configuration
├── models/               # MongoDB models (if applicable)
├── public/
│   ├── css/              # CSS stylesheets
│   ├── js/               # Client-side JavaScript
│   └── img/              # Images
├── routes/
│   ├── auth.js           # Authentication routes
│   └── habits.js         # Habit management routes
├── scripts/
│   └── cassandra-setup.js # Cassandra schema setup
├── services/
│   ├── habitService.js   # Habit-related business logic
│   └── userService.js    # User-related business logic
├── views/
│   ├── partials/         # Reusable view components
│   ├── auth/             # Login and register views
│   ├── dashboard.ejs     # Main dashboard view
│   └── progress.ejs      # Progress tracking view
├── .env                  # Environment variables
├── app.js                # Express application entry point
└── package.json          # Project dependencies
```

## Setup Instructions

### Prerequisites

- Node.js (v14+ recommended)
- MongoDB OR Apache Cassandra
- npm or yarn

### Installation

1. Clone the repository:
   ```
   git clone https://github.com/yourusername/habit-tracker.git
   cd habit-tracker
   ```

2. Install dependencies:
   ```
   npm install
   ```

3. Create a `.env` file in the root directory with the following variables:
   ```
   PORT=3000
   NODE_ENV=development
   SESSION_SECRET=your_session_secret
   
   # Choose your database engine: 'mongodb' or 'cassandra'
   DB_ENGINE=mongodb
   
   # MongoDB Configuration (if using MongoDB)
   MONGODB_URI=mongodb://localhost:27017/habit_tracker
   
   # Cassandra Configuration (if using Cassandra)
   CASSANDRA_CONTACT_POINTS=127.0.0.1
   CASSANDRA_DC=datacenter1
   CASSANDRA_KEYSPACE=habit_tracker
   ```

4. Database Setup:
   - For MongoDB: Ensure MongoDB is running
   - For Cassandra:
     ```
     node scripts/cassandra-setup.js
     ```

5. Start the application:
   ```
   npm start
   ```

6. Visit `http://localhost:3000` in your browser

## Usage

1. Register a new account
2. Login with your credentials
3. Create new habits with the "New Habit" button
4. Mark habits as complete when you accomplish them
5. Visit the Progress page to see visualizations of your habit completion rates
6. Maintain your streaks by consistently completing habits!

## Development

To run the application in development mode with automatic restarts:

```
npm run dev
```

## Database Support

### MongoDB

The application uses Mongoose for MongoDB object modeling. Models are defined in the `models` directory.

### Apache Cassandra

For Cassandra, the application uses the native Cassandra driver. Schema setup is handled in `scripts/cassandra-setup.js`.

## Contributing

1. Fork the repository
2. Create your feature branch: `git checkout -b feature/amazing-feature`
3. Commit your changes: `git commit -m 'Add some amazing feature'`
4. Push to the branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

## License

[MIT](LICENSE)

## Contact

Your Name - your.email@example.com

Project Link: https://github.com/03nnn/habit_tracker_NoSql_Implementation/
