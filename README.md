# Property Scraper Proxy

A simple proxy server for bypassing anti-scraping protections when scraping property websites.

## Deployment

This proxy is designed to be deployed on Vercel.

1. Fork this repository
2. Connect your Vercel account to the GitHub repository
3. Deploy to Vercel

## Usage

Send a POST request to the deployed endpoint with a JSON body containing the URL to scrape:

```javascript
fetch('https://your-vercel-url/api/proxy', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({ url: 'https://www.example.com/property/123' })
})
.then(response => response.json())
.then(data => {
  // data.html contains the HTML content of the requested URL
  console.log(data);
});
```

## Local Development

1. Install dependencies: `npm install`
2. Run locally: `npm start`
