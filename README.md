<div align="center">

# Simple Note

### A browser-style cross-platform notes app built with Flutter

[![Flutter](https://img.shields.io/badge/Flutter-3.19+-02569B?style=flat&logo=flutter&logoColor=white)](https://flutter.dev)
[![Dart](https://img.shields.io/badge/Dart-3.3+-0175C2?style=flat&logo=dart&logoColor=white)](https://dart.dev)
[![Firebase](https://img.shields.io/badge/Firebase-Auth%20%2B%20Firestore-FFCA28?style=flat&logo=firebase&logoColor=black)](https://firebase.google.com)
[![Riverpod](https://img.shields.io/badge/Riverpod-2.5-764ABC?style=flat)](https://riverpod.dev)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat)](LICENSE)

**Open notes as tabs · Navigate with an address bar · Sync across devices**


</div>

---
<div align="center">
  
## Try it yourself
  
See it in Action: https://my-simple-note.web.app
  
</div>

---

##  Screenshots

<div align="center">
<img width="1440" height="900" alt="Screenshot 2026-04-26 at 12 02 59 PM (2)" src="https://github.com/user-attachments/assets/4fe6ab17-ee7c-41d2-8c29-86423d467dd1" />
<img width="1440" height="900" alt="Screenshot 2026-04-26 at 12 02 26 PM (2)" src="https://github.com/user-attachments/assets/3017b8fc-bb8b-4f32-8874-76bdcc82b4fc" />
<img width="388" height="747" alt="Screenshot 2026-04-26 at 7 04 03 PM" src="https://github.com/user-attachments/assets/26ec3680-a916-4843-b507-931d1087f584" />
<img width="1312" height="1118" alt="Screenshot 2026-04-26 at 7 03 54 PM" src="https://github.com/user-attachments/assets/3133c245-fc75-45a4-bbf9-98a082f7902c" />


</div>

---

## Architecture

Simple note follows a strict **layered repository architecture**. Lower layers never import upper layers.

```
┌─────────────────────────────────────────┐
│         Widgets & Screens(UI)           │  
├─────────────────────────────────────────┤
│         Riverpod Providers              │ 
├─────────────────────────────────────────┤
│         Repository Layer                │  
├─────────────────────────────────────────┤
│         Models                          │  
├─────────────────────────────────────────┤
│         Hive + flutter_quill + Firebase │ 
└─────────────────────────────────────────┘
```


## Tech Stack

| Package | Purpose |
|---|---|
| `flutter_riverpod` | State management — StreamProvider, StateNotifier, family |
| `hive_flutter` | Local offline storage with type-safe adapters |
| `flutter_quill` | Rich text editor — Delta JSON format |
| `uuid` | UUID v4 for all entity IDs (survives Firestore migration) |
| `image_picker` | Insert images from gallery into notes |
| `firebase_core` | Firebase SDK bootstrap |
| `firebase_auth` | Email + Google authentication |
| `cloud_firestore` | Real-time cloud database |
| `connectivity_plus` | Detect online/offline for sync engine |
| `path_provider` | App documents directory (Hive lock recovery) |


---

<div align="center">

Built with ❤️ using Flutter

</div>
