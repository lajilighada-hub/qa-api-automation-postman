# QA API Automation (Postman + Newman)

End-to-end API tests with Postman:
- Chained requests (GET → POST → GET/PUT/DELETE)
- Assertions (status, JSON fields, headers, response time)
- Variables & environments
- Negative tests
- Optional CLI execution via Newman + HTML report

## How to run (Newman)
1. Install Node.js (LTS) and Newman:
   npm install -g newman
2. Run:
   newman run QA_Automation.postman_collection.json -e QA_Env.postman_environment.json -r cli,html
3. Open the HTML report at:
   newman\newman-run-report.html

## Files
- QA_Automation.postman_collection.json  (exported Postman collection)
- QA_Env.postman_environment.json        (exported environment; no secrets in Initial Values)
- newman\newman-run-report.html          (sample report)
- screenshots\                           (images of passing runs)

## Notes
- Demo API: https://jsonplaceholder.typicode.com
- The POST endpoint may not persist; tests allow 200/404 for GET-by-id after create.
