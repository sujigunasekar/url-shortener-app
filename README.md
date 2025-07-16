##  Steps Involved in This Project
### 1.  Project Setup
Created the React project using create-react-app

Installed dependencies: @mui/material, @emotion/react, @emotion/styled, react-router-dom

Configured .env file to force app to run on localhost:3000

### 2.  Folder Structure Setup
```
url-shortener-app/
├── public/
├── src/
│   ├── components/
│   │   ├── LoggerMiddleware.js
│   │   └── UrlShortenerForm.js
│   ├── pages/
│   │   ├── HomePage.jsx
│   │   └── StatsPage.jsx
│   ├── App.js
│   └── index.js
└── package.json
```
### 3.  Routing Configuration
App.js sets up React Router with two routes:

/ → Homepage with URL shortener form

/stats → (Placeholder for future stats page)

### 4.  Core Component: UrlShortenerForm.js
Started with a single entry and allowed up to 5 concurrent entries

State contains originalURL, duration, customAlias, and output

Input handlers update state dynamically

### Submit handler:

Validates non-empty URL

Generates a shortcode (or uses custom if provided)

Simulates short URL and logs using LoggerMiddleware

Results displayed below each form entry

### 5.  Logger Middleware

const logger = (msg) => console.log(`[${new Date().toISOString()}] ${msg}`);
export default logger;
Logs user actions with timestamps

Used in every shortcode generation

### 6.  Extending Entries
Add button lets user add up to 5 URL forms

Includes validation to prevent exceeding the limit

### 7.  App Launch Workflow
Clone repo & navigate to project directory

Run npm install

Set port to 3000 using:

PowerShell: $env:PORT=3000; npm start

CMD: set PORT=3000 && npm start

App will open on http://localhost:3000

