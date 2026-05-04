# The Artisans Hub — Firebase Edition

A complete web storefront for customized gifts, trophies, mementos, and photo gifts.
**Now powered by Firebase Firestore** (migrated from Supabase).

---

## 🔥 Firebase Setup

### 1. Enable Firestore
- Go to: https://console.firebase.google.com/project/the-artisans-hub
- Click **Build → Firestore Database → Create database**
- Choose **Start in test mode** (for development)

### 2. Set Security Rules (Firestore → Rules tab)
```
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /products/{document=**} {
      allow read: if true;
      allow write: if true;
    }
    match /orders/{document=**} {
      allow read, write: if true;
    }
  }
}
```

### 3. Deploy to Firebase Hosting
```bash
npm install -g firebase-tools
firebase login
cd the-artisans-hub-firebase
firebase deploy
```

After deploying, your app will be live at: https://the-artisans-hub.web.app

---

## 📁 File Structure

```
the-artisans-hub-firebase/
├── index.html          ← Main storefront
├── logo.jpeg           ← Store logo
├── firebase.json       ← Firebase Hosting config
├── .firebaserc         ← Firebase project config
├── css/
│   └── style.css
├── js/
│   ├── main.js         ← Main app (Firebase Firestore)
│   └── firebase.js     ← Firebase initialization
└── admin/
    ├── index.html      ← Admin panel
    ├── admin.js        ← Admin app (Firebase Firestore)
    └── admin.css
```

---

## 🔐 Admin Login

Username: ADMIN VIBES
Password: VIBES@OAH2026

---

## 📞 WhatsApp

Orders are sent via WhatsApp to: +91 63792 99336
