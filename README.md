# Quacker
Learn more about courses offered about RPI before taking them.

### **Step 1: Testing the Application**

To test the full MERN stack, follow these steps:

1. **Backend**: Your backend server is running at `http://localhost:5000`. If you visit `http://localhost:5000/api/users` in your browser, you should see the list of users from MongoDB (if any exist).

2. **Frontend**: Your React app is running at `http://localhost:3000`. When you open this in the browser, it should display the list of users fetched from the backend.

3. **Add Users to MongoDB**: To see data on the frontend, you can either manually insert users into your MongoDB database or extend your backend to handle **POST** requests to add new users. Here’s an example of how you can add a route to create new users:

   * **Create a POST route in `userRoutes.js`**:

   ```javascript
   // routes/userRoutes.js

   const express = require('express');
   const User = require('../models/userModel');
   const router = express.Router();

   // GET route
   router.get('/', async (req, res) => {
     try {
       const users = await User.find();
       res.json(users);
     } catch (error) {
       res.status(500).send('Server error');
     }
   });

   // POST route to create a new user
   router.post('/', async (req, res) => {
     const { name, email } = req.body;
     try {
       const newUser = new User({ name, email });
       await newUser.save();
       res.status(201).json(newUser);
     } catch (error) {
       res.status(400).send('Error adding user');
     }
   });

   module.exports = router;
   ```

   * **Update the frontend to create a user**. You can add a form in React to send POST requests to add users.

---

### **Step 2: Extend the Application (Optional)**

Here are some potential next steps for extending the MERN app:

1. **Add CRUD functionality**: You can create routes for creating, updating, and deleting users in MongoDB.
2. **Add user authentication**: Implement **JWT authentication** (JSON Web Tokens) to secure your API and create login/registration functionality.
3. **Frontend improvements**: Add forms, validations, and improve the UI with libraries like **Material UI** or **Bootstrap**.
4. **Deploy the application**: Once you are happy with the app, you can deploy it. For example, you can deploy:

   * The backend on services like **Heroku**, **Render**, or **DigitalOcean**.
   * The frontend on **Netlify** or **Vercel**.
   * Use **MongoDB Atlas** for the database.

---

// GET route to fetch all users
router.get('/', async (req, res) => {
  try {
    const users = await User.find(); // Fetch all users
    res.status(200).json(users); // Respond with the user data
  } catch (error) {
    res.status(500).json({ message: 'Server error' });
  }
});

This route will fetch all users stored in the users collection and return them as a JSON response.