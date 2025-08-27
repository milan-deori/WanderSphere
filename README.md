# WanderSphere

WanderSphere is a Node.js/Express web application for listing, reviewing, and managing travel accommodations. It uses MongoDB for data storage, Passport.js for authentication, and Cloudinary for image uploads.

## Features

- User authentication (signup, login, logout)
- Create, edit, delete listings
- Upload listing images
- Leave reviews and ratings
- Flash messages for feedback
- Responsive UI with EJS templates

## Folder Structure

- `app.js`: Main application entry point
- `controllers/`: Route handlers for listings, reviews, users
- `models/`: Mongoose schemas for Listing, Review, User
- `routes/`: Express routers for listings, reviews, users
- `views/`: EJS templates for frontend
- `public/`: Static assets (CSS, JS)
- `utils/`: Utility functions (error handling, async wrapper)
- `middleware.js`: Custom middleware (auth, validation)
- `cloudConfig.js`: Cloudinary configuration
- `schema.js`: Joi validation schemas
- `init/`: Database seeding scripts

## Getting Started

### Prerequisites

- Node.js
- MongoDB
- Cloudinary account

### Installation

1. Clone the repository.
2. Install dependencies:
   ```sh
   npm install
   ```
3. Set up `.env` with your Cloudinary and MongoDB credentials.

### Running the App

```sh
node app.js
```
or with nodemon:
```sh
npx nodemon app.js
```

## Main Modules

### User Authentication

- `controllers/users.js`: Handles signup, login, logout.
- `models/user.js`: User schema with Passport.js integration.
- `routes/user.js`: User-related routes.

### Listings

- `controllers/listings.js`: CRUD operations for listings.
- `models/listing.js`: Listing schema.
- `routes/listing.js`: Listing routes.

### Reviews

- `controllers/reviews.js`: Add/delete reviews.
- `models/review.js`: Review schema.
- `routes/review.js`: Review routes.

### Middleware & Utilities

- `middleware.js`: Auth, validation, permissions.
- `utils/ExpressError.js`: Custom error class.
- `utils/wrapAsync.js`: Async error wrapper.

### Cloudinary Integration

- `cloudConfig.js`: Cloudinary setup for image uploads.

## Validation

- `schema.js`: Joi schemas for validating listings and reviews.

## Seeding Data

- `init/index.js`: Seeds the database with sample listings.
- `init/data.js`: Sample listings data.

## License

MIT

---
