# API Testing Portfolio — ReqRes.in

A complete API test suite built in Postman covering real-world 
testing scenarios including authentication, CRUD operations, 
test assertions, environment variables, and chained requests.

---

## Tech stack

- Postman v11
- ReqRes.in sandbox API
- JavaScript (pm.test assertions)
- Newman (CLI test runner)

---

## What is tested

| Request | Method | Assertions |
|---|---|---|
| Login / Get token | POST | Status 200, token exists |
| List users | GET | Status 200, data is array, all users have email |
| Single user | GET | Status 200, user id matches |
| Create user | POST | Status 201, id generated, name matches |
| User not found | GET | Status 404 |

---

## Test categories covered

- Positive testing — valid inputs return correct responses
- Negative testing — invalid inputs return correct error codes  
- Response time validation — all requests under 2000ms
- Schema validation — correct fields present in every response
- Environment variables — no hardcoded values in collection
- Chained requests — token from login reused across all requests

---

## How to run

**In Postman:**
1. Import `reqres-api-tests.postman_collection.json`
2. Import `reqres-sandbox.postman_environment.json`
3. Select ReqRes Sandbox environment
4. Run collection via Collection Runner

**Via Newman CLI:**
npm install -g newman
newman run reqres-api-tests.postman_collection.json \
  -e reqres-sandbox.postman_environment.json

---

## Test results

- Total requests: 5
- Total assertions: 9
- Pass rate: 100%

---

## Author

Uzair Akhtar — Junior SQA Engineer  
GitHub: github.com/iamlethal27  
Email: m.uzairakhtar03@gmail.com
