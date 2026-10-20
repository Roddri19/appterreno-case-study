# AppTerreno – Field Sales Tracking App (case study)

> Mobile app + admin dashboard to manage field sales reps in real time.
> Built by a small team at **TOANPE SRL** (Sep–Oct 2025), where I worked as a Backend Developer Trainee.
> The source code lives in a private repository owned by the team lead, so this repo documents the project and my contributions instead of the code.

## What it does

- Sales reps log in on the mobile app and their **location is tracked in real time**.
- Clients and sales are registered and shown on a **map** (Google Maps).
- Admins assign sales zones and review routes and reports on a **web dashboard**.
- Reps can jump to **WhatsApp** to contact a client.

## Tech stack

| Layer | Technologies |
|-------|--------------|
| Mobile app | React Native, Expo (SDK 54, Expo Go), React Navigation, expo-location, react-native-maps |
| Web dashboard | React (Vite), later Next.js 15 |
| Backend / data | Firebase Authentication, Cloud Firestore |
| Maps | Google Maps API |
| Workflow | Git flow (`main` / `develop` / `feature/*` / `bugfix/*`), pull requests, Scrum |

## Architecture

```
 Sales rep (Expo app) ──login──▶ Firebase Auth
        │
        └── location every 30 s ──▶ Firestore: usuarios · ubicaciones · clientes · ventas
                                              │
 Admin (web dashboard) ◀──── routes, clients, sales on the map
```

## My contributions (18 commits)

- **Mobile login with Firebase Auth** – login screen, auth context and Firebase setup for the Expo app.
- **Real-time location tracking** – stored the rep's location in Firestore every 30 seconds (feature branch merged via PR #8).
- **Firebase configuration** for the new Firestore database.
- **Project structure refactors** – moved the auth module into `/mobile`, kebab-case naming, removed a git submodule, simplified navigation.
- **Bug fix** – login no longer asking for credentials again, and tracking corrected.

## What I learned

Working in a team with feature branches and pull requests, modeling Firestore collections together with the frontend, and building a mobile app with React Native and Expo end to end.

---
*Rodrigo Leytes · [LinkedIn](https://linkedin.com/in/rodrigoleytes) · [GitHub](https://github.com/Roddri19)*
