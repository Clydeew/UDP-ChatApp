# 🗨️ Java LAN Chat Application (UDP Multicast)

A lightweight LAN-based chat application built in **Java Swing** using **UDP Multicast**. Designed for simple local-network communication with features such as:

* Emoji picker
* Typing indicator
* Timestamps
* Real-time online status
* Multiclient support via multicast

This app was built using **NetBeans**, utilizing auto-generated `.form` GUI files.

---

## 📁 Project Structure

```
.
├── README.md
├── nbproject/
│   ├── project.properties
│   ├── project.xml
│   └── ... (NetBeans configs)
├── src/
│   └── chatapplication/
│       ├── ChatApp.java
│       ├── ChatApp.form
│       ├── MultiClient.java
│       ├── MulticastClient.java
│       ├── MulticastClient.form
│       ├── OnlineStatus.java
│       └── ReceiveOnlineStatus.java
└── test/
```

---

## ✨ Features

### ✔️ UDP Multicast Networking

* Lightweight LAN chat
* Each message is broadcast to a multicast group
* All clients receive real‑time updates

### ✔️ Emoji Picker

* ASCII/emoticon‑style emoji list
* Clicking inserts emoji into text input

### ✔️ Typing Indicator

* Shows “User is typing…” when another client is typing

### ✔️ Timestamps

* Every message displays its sending time

### ✔️ Online Presence System

* Clients broadcast their username when joining
* Other clients update their Online Users list

### ✔️ GUI Built in NetBeans

* Using Swing + .form auto‑generated layout

---

## 🚀 How to Run

### Requirements

* Java 8+
* NetBeans (recommended)

### Steps

1. Clone the repository:

   ```bash
   git clone https://github.com/Clydeew/UDP-ChatApp.git
   ```
2. Open the project in **NetBeans**.
3. Clean & Build.
4. Run `ChatApp.java`.
5. Input your username.
6. The chat window will open.

To test multiple clients: run several instances at once.

---

## 🧩 Main Components

| File                             | Description                                                       |
| -------------------------------- | ----------------------------------------------------------------- |
| `MultiClient.java`               | Entry point; asks username & launches chat window                 |
| `MulticastClient.java`           | Core chat logic (send/receive UDP, typing signals, online status) |
| `ChatApp.java`                   | Initial GUI window                                                |
| `OnlineStatus.java`              | Handles user online presence                                      |
| `ReceiveOnlineStatus.java`       | Background listener for presence packets                          |
| `MulticastClient$TypingReceiver` | Thread for typing indicator updates                               |

---

## 📝 Developer Notes

* Do **not** edit `initComponents()` — NetBeans manages it.
* Add custom code in separate methods (e.g., `setupEmojiButton()`).
* Networking is multi‑threaded (client listener, typing listener, etc.).

---

## 📌 License

This project is provided for personal and educational use.
