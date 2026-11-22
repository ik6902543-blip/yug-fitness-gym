YUG FITNESS GYM — FIREBASE WEB UPDATE

Included:
- index.html: Firebase Email/Password login, member signup, owner dashboard, fee/expiry updates, owner-recorded payments, member view.
- firestore.rules: secure rules matching this starter's data structure.

IMPORTANT SETUP:
1. Replace the existing GitHub Pages repository index.html with this index.html.
2. In Firebase Authentication > Settings > Authorized domains, add:
   ik6902543-blip.github.io
   (If it is already listed, leave it.)
3. In Firestore > Rules, replace current rules with firestore.rules and Publish.
4. The owner account UID must already exist as a document in the admins collection:
   Collection: admins
   Document ID: OWNER_FIREBASE_AUTH_UID
   Fields: role (string) = owner
5. Owner must sign in using the exact email used to create the Firebase Auth owner account.
6. Members sign up themselves using Member Signup. The owner then sets monthly fee and expiry from the owner dashboard.

SECURITY / LIMITATIONS:
- This is an MVP starter, not a fully audited production application.
- Do not store real member data until testing with a separate owner account and test member account is successful.
- The rules let members create only their own basic profile; only the owner can change fee/expiry or write payment history.
- Owner account creation/admin promotion must remain controlled by the gym owner.
- Payment records are manual owner confirmation only. UPI payments are NOT automatically verified.
- No automatic SMS OTP, no online payment gateway, no automatic reminders, and no native APK in this starter.
- Firebase Spark has usage limits. Do not enable billing without understanding possible charges.
- Keep regular exports/backups of important records.
- Firebase web apiKey is client configuration, not a password. Never publish service-account private keys or passwords.
