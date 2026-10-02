# Zenith

Zenith is a lightweight full-stack blog CMS built with Express, MongoDB, and a vanilla HTML/CSS/JavaScript frontend.

## Features

- List posts
- Read an individual post
- Create posts
- Update posts
- Delete posts
- Serve the static frontend
- Reuse the MongoDB connection across warm serverless executions

## Architecture

Browser -> Vanilla frontend -> Express API -> MongoDB

## API

| Method | Endpoint | Purpose |
|---|---|---|
| GET | /api/posts | List posts |
| GET | /api/posts/:id | Fetch one post |
| POST | /api/posts | Create a post |
| PUT | /api/posts/:id | Update a post |
| DELETE | /api/posts/:id | Delete a post |

## Stack

- Node.js
- Express
- MongoDB
- Vanilla JavaScript
- HTML/CSS
- Vercel-compatible deployment

## Setup

Create .env with:
MONGO_URI=your_mongodb_connection_string
NODE_ENV=development
PORT=3000

Then run:
npm install
npm start

Open http://localhost:3000.

## Structure

Zenith/
  public/
    index.html
    script.js
    style.css
  server.js
  package.json
  vercel.json

## Security

Keep MongoDB credentials in environment variables. Validate and authorize write operations before exposing the API publicly.

The repository already contains the core implementation; this commit documents it rather than changing its architecture.
