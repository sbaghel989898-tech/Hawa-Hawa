# 🚀 File Manager Ultra Pro - Cloud Edition ☁️

[![Firebase](https://img.shields.io/badge/Firebase-v12.11.0-orange?logo=firebase)](https://firebase.google.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Interface](https://img.shields.io/badge/UI-Glassmorphism-blueviolet)](#)

Ek modern, fast aur secure web-based file manager jo **Firebase Cloud Storage** ka use karta hai. Isme aap files ko locally preview kar sakte hain aur ek click mein server par upload kar sakte hain.

---

## ✨ Key Features

* **💎 Glassmorphic UI:** Modern blur effect aur clean design.
* **📂 Drag & Drop:** Files ko browse karein ya direct drop karke add karein.
* **🖼️ Smart Preview:** Images aur Videos ko upload se pehle browser mein hi dekhein.
* **☁️ Cloud Upload:** Firebase Storage integration ke saath direct server par files save karein.
* **💾 Local Download:** Files ko rename karke local machine par save karne ka option.
* **📱 Fully Responsive:** Mobile aur Desktop dono par smoothly kaam karta hai.

---

## 🛠️ Tech Stack

| Technology | Usage |
| :--- | :--- |
| **HTML5 / CSS3** | Structure & Glassmorphism Styling |
| **JavaScript (ES6)** | Logic, File Handling & DOM Manipulation |
| **Firebase SDK v12.11.0** | Cloud Storage & Analytics |

---

## 🚀 How to Setup

1.  **Clone the Repo:**
    ```bash
    git clone [https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git](https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git)
    ```

2.  **Firebase Configuration:**
    `index.html` file ke andar apni Firebase details check karein:
    ```javascript
    const firebaseConfig = {
      apiKey: "AIzaSyBHek2pud22n_lRN2UhzFZlKCQGowh7Egs",
      authDomain: "boka-choda-suar-bachha.firebaseapp.com",
      projectId: "boka-choda-suar-bachha",
      storageBucket: "boka-choda-suar-bachha.firebasestorage.app",
      // ... baki details
    };
    ```

3.  **Run the Project:**
    Bas `index.html` file ko kisi bhi browser mein open karein (Live Server extension use karna behtar hai).

---

## 🔒 Firebase Security Rules (Important)

Files upload hone ke liye aapke Firebase Storage Rules aise hone chahiye:

```javascript
service firebase.storage {
  match /b/{bucket}/o {
    match /{allPaths=**} {
      allow read, write: if true; 
    }
  }
}
