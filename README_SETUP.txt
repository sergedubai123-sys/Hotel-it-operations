HOTEL IT OPERATIONS WEB APP — SETUP

FILES
- index.html: the app
- supabase_setup.sql: database tables and pilot policies
- README_SETUP.txt: this guide

TEST LOCALLY
1. Extract the ZIP.
2. Open index.html in a modern browser.
3. Try the checklist and issue reporting.
Local demo mode saves data only in that browser; it is NOT shared with teammates.

SET UP SHARED DATA
1. Ask your manager / IT security team whether an external hosted database is approved.
2. Create an approved Supabase project at https://supabase.com/.
3. In Supabase, open SQL Editor, paste the contents of supabase_setup.sql, and run it.
4. Find your Project URL and anon/public key in project settings. Never use the service_role key in a browser.
5. Open the app, choose Team Setup, enter the URL and public key, and click Connect shared database.
6. Deploy index.html to a web host approved by your organization, then share that deployed URL with your IT staff.
7. Test on a second device to confirm records are shared.

SECURITY WARNING
The supplied SQL policies allow public reading/writing for pilot testing. Anyone with access to the app may be able to read or change records. Do NOT use this setup for production without IT/security approval. Before production, add staff authentication and restrictive row-level security policies. Do not include passwords, guest details, payment data, or other sensitive information in issue notes. The browser app must never contain a service_role key.

LIMITATION
This is a starter app, not a formal audit-grade system. In shared mode it loads the latest saved checklist row, and it does not yet provide staff login or a complete audit trail. Ask your IT team to harden it before using it as an official operational control.
