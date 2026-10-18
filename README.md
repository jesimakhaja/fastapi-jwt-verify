# RS256 JWT Verification API

Deploy as a Python web service on Render:
- Build command: `pip install -r requirements.txt`
- Start command: `uvicorn main:app --host 0.0.0.0 --port $PORT`
- Endpoint to submit: `https://YOUR-SERVICE.onrender.com/verify`

POST JSON body: `{"token":"<JWT>"}`

The service verifies the RS256 signature, issuer, audience, expiration, and required `sub` and `email` claims.
