# FriendBook
Social Media Clone App using with express js and Mongodb

🔧 Project Overview:

This project is a simplified social media web application developed using Node.js (Express), MongoDB, EJS templates, and JWT-based authentication. It demonstrates essential features of a typical social platform such as authentication, user profile, posts with images/videos, and UI interactions.

📑 Features Implemented:

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

💪 Technical Stack:

Backend: Node.js, Express.js

Database: MongoDB with Mongoose

Authentication: JWT via cookies

Views: EJS templates with partials

Frontend: Bootstrap 5 + Custom CSS

Media Uploads: Multer (image/video)

📊 Folder Structure:

![image](https://github.com/user-attachments/assets/8c4cded9-d85d-47c5-b3b8-17b6ec1acb0f)

🚪 Logout Route:

router.get('/logout', (req, res) => {
  res.clearCookie('token');
  res.redirect('/api/auth/login');
});

🌐 UI Enhancements Summary:

All images resized to fixed width/height using style="object-fit: cover;"

Post media preview added via JavaScript

Layout improved for responsiveness and aesthetics

Bootstrap cards used for separation of sections

Modal used for post edit

📚 Final Notes:

Ensure .env includes PORT and MONGO_URI

Run: npm install, then npm start

Uploads are stored in /uploads

All views in EJS with header/footer includes


![image](https://github.com/user-attachments/assets/356bba03-86b6-406d-904e-41855bf37659)

![image](https://github.com/user-attachments/assets/8b197231-c277-4019-ba32-7dd5a749d448)

![image](https://github.com/user-attachments/assets/ac537bf1-07b1-4dbc-82d3-d53c0f255e46)

![image](https://github.com/user-attachments/assets/6e2082a7-c084-4a9c-91ee-37a2cfe48d39)


