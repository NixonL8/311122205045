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
<img width="1403" height="859" alt="Screenshot 2025-08-26 150551" src="https://github.com/user-attachments/assets/601278b1-7b81-4024-b95a-39d335209d7d" />
<img width="1447" height="773" alt="Screenshot 2025-08-26 153041" src="https://github.com/user-attachments/assets/d55b47ae-f601-41a1-a8c0-98229ea637b1" />
<img width="1452" height="941" alt="Screenshot 2025-08-26 153114" src="https://github.com/user-attachments/assets/deeb89c4-a22e-40b0-9f31-0d62b06908cd" />
<img width="1442" height="817" alt="Screenshot 2025-08-26 153131" src="https://github.com/user-attachments/assets/444ee534-24c5-4dc9-9bf5-11b4ee475c98" />
<img width="1443" height="832" alt="Screenshot 2025-08-26 153058" src="https://github.com/user-attachments/assets/5e2a7961-209e-4796-85a9-b2c820c5d1a6" />


