# URL Shortener Microservice

## Quick start (after extracting)

1. Install dependencies:
   ```bash
   npm install
   ```
2. Start the service:
   ```bash
   npm start
   ```
3. Health check:
   ```bash
   curl http://localhost:3000/health
   ```
4. Create short URL (example):
   ```bash
   curl -s -X POST http://localhost:3000/shorturls \
     -H 'Content-Type: application/json' \
     -d '{"url":"https://example.com/very/long/path"}' | jq
   ```
5. Redirect test (open in browser or use curl):
   ```bash
   curl -I http://localhost:3000/<shortcode>
   ```
6. Get stats:
   ```bash
   curl http://localhost:3000/shorturls/<shortcode> | jq
   ```

Logs are written to `logs/app.log` via the mandatory custom logging middleware.

To change port or base URL, edit `.env` and restart the service.

WORKFLOWS :
<img width="1447" height="773" alt="Screenshot 2025-08-26 153041" src="https://github.com/user-attachments/assets/f59e9507-016d-4c76-a35c-f25bf1c602da" />
<img width="1443" height="832" alt="Screenshot 2025-08-26 153058" src="https://github.com/user-attachments/assets/a69a6ba7-3155-453a-9251-20dbe2ef2be0" />
<img width="1452" height="941" alt="Screenshot 2025-08-26 153114" src="https://github.com/user-attachments/assets/39da2a70-c97d-4d81-870c-644b8730b8d3" />
<img width="1442" height="817" alt="Screenshot 2025-08-26 153131" src="https://github.com/user-attachments/assets/19e7c2cf-446c-4418-8ca6-f1e479a953db" />




