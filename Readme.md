Authentication Basics Project

This is Node.js Express backend for user authentication with MongoDB.

Features: Signup (email, password, name - hashes password, sets JWT cookie), login and logout routes ready.

Setup:
- npm install
- copy .env.example .env
- Add to .env: MONGO_URI=your mongo url, JWT_SECRET=some secret
- npm run dev

Server on localhost:5000

Endpoints:
- POST /api/auth/signup : body {email, password, name}
- POST /api/auth/login 
- POST /api/auth/logout

Test signup: curl -X POST http://localhost:5000/api/auth/signup -H "Content-Type: application/json" -d '{"email":"test@test.com","password":"pass","name":"Test"}'

Files:
- backend/index.js : server
- backend/controllers/auth.controller.js : signup code
- backend/models/user.model.js : user model
- backend/db/connectDB.js : mongo connect

Ready to use after env setup.

