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
<img width="1366" height="768" alt="simple-note-thumbnail" src="https://github.com/user-attachments/assets/57035731-cf91-4126-85bf-331efb768081" />



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
