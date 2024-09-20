### Server

#### controllers

- `register` registers a new user by hashing their password and saving their details in the database.
- `login` authenticates a user by verifying their email and password, and generates a JWT token upon successful login.

#### middleware

- `verifyToken` authenticates JWT tokens from incoming requests to ensure user access.

#### routes

- `auth.js`: handle routes for `/auth`

  - `/auth/login` (POST)

- `users.js`: handle routes for `/users`

  - `/users/:id` (GET)

  - `/users/:id/frineds` (GET)

  - `/users/:id/:friendId` (PATCH)

#### index.js

```javscript
/* ROUTES WITH FILES */
app.post("/auth/register", upload.single("picture"), register);

/* ROUTES */
app.use("/auth", authRoutes);
app.use("/users", userRoutes);
```
