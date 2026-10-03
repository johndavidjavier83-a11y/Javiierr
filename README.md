# JD Academic Portfolio — Firebase Edition

A responsive black-and-blue academic portfolio for John David Javier. Visitors can view/download published files, while only the authenticated owner account can upload or delete content.

## Sections
- Home / About Me
- Quiz
- Long Quiz
- Examinations: Midterms and Finals
- Activities
- Projects
- Image and document uploads per category

## Owner account
The website is configured for this Firebase Authentication email:
`johndavidjavier83@gmail.com`

**Do not put the password in HTML, CSS, JavaScript, GitHub, or this ZIP.** Create the Firebase Authentication user in the Firebase Console and set the password there. The password should remain private and is never needed in the website source code.

## Firebase setup
1. Open Firebase Console and create a Firebase project.
2. Add a Web App.
3. Enable **Authentication → Sign-in method → Email/Password**.
4. In **Authentication → Users**, create `johndavidjavier83@gmail.com` and set the private password you chose.
5. Enable **Firestore Database**.
6. Enable **Storage**.
7. Open `script.js` and replace the `PASTE_YOUR_*` Firebase Web App values with your project configuration.
8. Publish `firestore.rules` in Firestore Rules.
9. Publish `storage.rules` in Storage Rules.
10. Host the folder on GitHub Pages, Firebase Hosting, Netlify, Vercel, or another static host.

### Important security model
The email appears in the client because the UI needs to know which signed-in account is the owner, but this is **not** the security boundary. Firestore and Storage rules require an authenticated Firebase user whose email is exactly `johndavidjavier83@gmail.com`. Visitors can read files, but unauthenticated visitors cannot create, update, or delete them.

### Firebase configuration
Firebase web configuration values are not passwords or service-account secrets. They identify the web app. Never put a Firebase service-account private key in this project.

## Profile photo
Put your photo at:
`images/profile.jpg`

If no photo is present, the Home section automatically shows the JD fallback.

## Upload limits
The current JavaScript limits uploads to 25 MB per file. Supported examples include images, PDF, Word, PowerPoint, Excel, text, and ZIP files.

## Public visitor behavior
Visitors do not need a login to view the portfolio or open/download published files. Only the Owner button opens the Firebase sign-in area.
