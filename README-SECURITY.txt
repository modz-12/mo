Anime Mods - Firebase Security Patch

1) Deploy Firestore rules:
   firebase deploy --only firestore:rules

2) IMPORTANT:
   The first admin must be created manually from Firebase Console by setting
   users/{AUTH_UID}.role = "admin" and verified = true.

3) The browser MUST NOT contain an admin/moderator password.
   Roles are assigned only by an existing admin.

4) The Firebase web config/apiKey is not a secret. Keep Firestore rules strict.

5) Client-side XP is still inherently tamperable without a trusted backend.
   For production-grade XP/reputation, move XP/stat mutations to Cloud Functions.

6) Deleting a Firestore users document does not delete the Firebase Auth account.
   Full account deletion requires Firebase Admin SDK / Cloud Functions.
