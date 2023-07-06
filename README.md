# StudyNotion

StudyNotion is a fully functional ed-tech platform that enables users to create, consume, and rate educational content. The platform is built using the MERN stack.


## System Architecture 

The StudyNotion ed-tech platform consists of three main components: the front end, the back end, and the database. The platform follows a client-server architecture, with the front end serving as the client and the back end and database serving as the server.

### Frontend 

The front end of StudyNotion has the following pages:

#### For Students:

- Homepage: This page has a brief introduction to the platform, as well as links to the course list and user details.
- Course List: This page has a list of all the courses available on the platform, along with their descriptions and ratings.
- Wishlist: This page displays all the courses a student has added to their wishlist.
- Cart Checkout: This page allows the user to complete the course purchase.
- Course Content: This page has the course content for a particular course, including videos, and other related material.
- User Details: This page has details about the student's account, including their name, email, and other relevant information.
- User Edit Details: This page allows students to edit their account details.

#### For Instructors:

- Dashboard: This page has an overview of the instructor's courses, as well as the ratings and feedback for each course.
- Insights: This page has detailed insights into the instructor's courses, including the number of views, clicks, and other relevant metrics.
- Course Management Pages: These pages allow the instructor to create, update, and delete courses, as well as manage the course content and pricing.
- View and Edit Profile Details: These pages allow the instructor to view and edit their account details.

### Backend

StudyNotion uses a monolithic architecture, with the backend built using Node.js and Express.js, and MongoDB as the primary database.

#### Features and Functionalities of the Back-end:

- User authentication and authorization: Students and instructors can sign up and log in to the platform using their email addresses and password. The platform also supports OTP (One-Time Password) verification and forgot password functionality for added security.
- Course management: Instructors can create, read, update, and delete courses, as well as manage course content and media. Students can view and rate courses.
- Payment Integration: Students will purchase and enroll on courses by completing the checkout flow that is followed by Razorpay integration for payment handling.
- Cloud-based media management: StudyNotion uses Cloudinary, a cloud-based media management service, to store and manage all media content, including images, videos, and documents.
- Markdown formatting: Course content in document format is stored in Markdown format, which allows for easier display and rendering on the front end.


## API Design

The StudyNotion platform's API is designed following the REST architectural style. The API is implemented using Node.js and Express.js. It uses JSON for data exchange and follows standard HTTP request methods such as GET, POST, PUT, and DELETE.

Some API endpoints and their functionalities:
- /api/auth/signup (POST) - Create a new user (student or instructor) account.
- /api/auth/login (POST) – Log in using existing credentials and generate a JWT token.
- /api/auth/verify-otp (POST) - Verify the OTP sent to the user's registered email.
- /api/auth/forgot-password (POST) - Send an email with a password reset link to the registered email.
- /api/courses (GET) - Get a list of all available courses.
- /api/courses/:id (GET) - Get details of a specific course by ID.
- /api/courses (POST) - Create a new course.
- /api/courses/:id (PUT) - Update an existing course by ID.
- /api/courses/:id (DELETE) - Delete a course by ID.
- /api/courses/:id/rate (POST) - Add a rating (out of 5) to a course.



