# FriendBook
Social Media Clone App using with express js and Mongodb

Project Overview:

This project is a simplified social media web application developed using Node.js (Express), MongoDB, EJS templates, and JWT-based authentication. It demonstrates essential features of a typical social platform such as authentication, user profile, posts with images/videos, and UI interactions.

Features Implemented:

1. Authentication (JWT + Cookie-based)

Secure login and registration system.

JWT stored in cookies.

Logout route clears the cookie and redirects to login.

2. User Profile System

Each user has a public profile page: /user/:username

Displays:

Profile picture

Name, Username, Bio

All posts by that user

If the logged-in user is the profile owner, shows an "Edit Profile" form (toggle)

3. Post Creation

Users can create posts with text and an optional media file (image or video).

Upload via multer, and media stored in uploads/.

Real-time preview on post form (JavaScript + FileReader).

4. Post Feed + Edit/Delete

All posts are shown in feed on /home

Logged-in user can:

Edit own post via modal

Delete post

Each post shows:

Author info (with profile picture)

Content text

Optional image/video

Date/time

5. Profile Suggestions Sidebar

Right sidebar shows other users as "People you may know".

Option to send friend request (placeholder form).

6. Responsive and Styled UI

Bootstrap 5 used for all layouts

Custom inline styles and responsive cards

Cards use soft shadows, rounded corners

Profile images and post media made consistent size and object-fit: cover

Technical Stack:

Backend: Node.js, Express.js

Database: MongoDB with Mongoose

Authentication: JWT via cookies

Views: EJS templates with partials

Frontend: Bootstrap 5 + Custom CSS

Media Uploads: Multer (image/video)

Folder Structure:

FriendBook/
├── models/
│   ├── User.js
│   └── Post.js
├── routes/
│   ├── auth.js
│   ├── post.js
│   ├── profile.js
│   └── user.js
├── views/
│   ├── layout/
│   │   ├── header.ejs
│   │   └── footer.ejs
│   ├── home.ejs
│   ├── profile.ejs
│   └── login.ejs
├── public/
│   └── images/
├── uploads/
└── server.js

Logout Route:

router.get('/logout', (req, res) => {
  res.clearCookie('token');
  res.redirect('/api/auth/login');
});

UI Enhancements Summary:

All images resized to fixed width/height using style="object-fit: cover;"

Post media preview added via JavaScript

Layout improved for responsiveness and aesthetics

Bootstrap cards used for separation of sections

Modal used for post edit

Final Notes:

Ensure .env includes PORT and MONGO_URI

Run: npm install, then npm start - c   #for start the server and clear cache

Uploads are stored in /uploads

All views in EJS with header/footer includes
