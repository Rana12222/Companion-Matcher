# Companion-Matcher
 Match Maker
A modern web application for finding potential matches based on shared interests. Built with React and vanilla JavaScript, featuring a beautiful gradient UI and real-time matching capabilities.
 Features

Profile Creation: Create detailed user profiles with name, age, and interests
Smart Matching: Find matches based on shared interests (minimum 2 common interests required)
Shortlisting: Save potential matches to your shortlist
Real-time Stats: View total users, current matches, and shortlisted profiles
Responsive Design: Works seamlessly on desktop and mobile devices
Modern UI: Beautiful gradient design with smooth animations and hover effects

 Project Overview
Match Maker is a single-page application that simulates a dating/friendship matching service. Users can create profiles with their interests, and the app will find potential matches who share at least 2 common interests. The application uses a mock backend with in-memory data storage for demonstration purposes.
Key Components:

Profile Creation Form: Allows users to input their details and interests
Match Search: Find matches for existing users
Match Display: Visual cards showing potential matches with shared interests
Shortlist Management: Save and manage favorite matches

 Setup Instructions
Prerequisites

A modern web browser (Chrome, Firefox, Safari, Edge)
No additional software installation required

Running the Application

Clone the repository
bashgit clone https://github.com/yourusername/match-maker.git
cd match-maker

Open the application
Simply open the index.html file in your web browser:

Double-click the index.html file, or
Right-click and select "Open with" → your preferred browser, or
Use a local server (optional):
bash# Using Python 3
python -m http.server 8000

# Using Node.js (if you have http-server installed)
npx http-server



Start using the app

The application will load with sample users already available
Create your own profile or search for existing users
Try sample usernames: Sanya, Nikhil, Priya, Rahul



 API Route Summary
The application uses a mock API with the following endpoints:
api.createUser(userData)
Creates a new user profile or updates an existing one.
Input:
javascript{
  name: "John Doe",
  age: 25,
  interests: ["tech", "music", "sports"]
}
Output:
javascript{
  success: true,
  user: {
    name: "John Doe",
    age: 25,
    interests: ["tech", "music", "sports"]
  }
}
api.getMatches(username)
Finds potential matches for a given username based on shared interests.
Input:
javascript"John Doe"
Output:
javascript{
  matches: [
    {
      name: "Sanya",
      age: 24,
      interests: ["tech", "music", "reading"],
      sharedInterests: ["tech", "music"]
    },
    {
      name: "Rahul",
      age: 26,
      interests: ["tech", "sports", "movies"],
      sharedInterests: ["tech", "sports"]
    }
  ]
}
