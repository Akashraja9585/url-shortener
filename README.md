# URL Shortener 🔗

A backend service that takes a long URL and returns a short one. When someone visits the short link, they get redirected to the original URL. Also tracks how many times each link was clicked. Built this to understand how backend APIs and databases work together.

## What it does

- Paste a long URL and get a short link instantly
- Clicking the short link redirects to the original URL
- Tracks click count for each short link
- Handles invalid URLs and missing links gracefully

## Tech used

- Node.js
- Express.js (for building the API)
- SQLite (for storing URL mappings)
- nanoid (for generating unique short codes)

## Getting started

Clone the repo and install dependencies:

    git clone https://github.com/yourusername/url-shortener.git
    cd url-shortener
    npm install

Run the server:

    node index.js

Server runs on http://localhost:3000

## API endpoints

    POST /shorten
    Body: { "url": "https://your-long-url.com" }
    Returns: { "shortUrl": "http://localhost:3000/abc123" }

    GET /:code
    Redirects to the original URL

## Folder structure

    src/
    ├── routes/
    │   └── url.js
    ├── db/
    │   └── database.js
    ├── index.js
    └── package.json

## What I learned

This was my first backend project and it took me a while to understand how Express routing works. Learning how HTTP redirects work (301 vs 302 status codes) was something I didn't expect to dig into but it was really interesting.

Setting up SQLite and writing queries to store and retrieve URL mappings helped me understand how a database fits into a real application. The nanoid library made generating unique short codes simple but I also learned what could go wrong with collisions.

## Future improvements

- Add a simple frontend UI to paste URLs
- Add expiry time for short links
- User login so people can manage their own links
- Custom short code support

## License

MIT
