# Login Page with Firebase Authentication

An Android app with Login, Sign Up, and Welcome screens using **Firebase Authentication** for email/password based user registration and login.

---

## Output Screenshots

<p align="center">
  <img src="https://github.com/user-attachments/assets/76b7ced2-3395-4dee-a893-2266f5954ed8" width="22%"/>
  <img src="https://github.com/user-attachments/assets/1f0ba705-99df-4d69-bbd8-1686016f17cc" width="22%"/>
  <img src="https://github.com/user-attachments/assets/23ba917a-cd7f-4579-8355-62a3a08abe0d" width="22%"/>
  <img src="https://github.com/user-attachments/assets/5fc3f31b-d89b-4f09-a7a7-94168c128d6a" width="22%"/>
</p>

---

## Features

- **Firebase Auth** — email/password login and registration
- **LoginActivity** — Email + Password fields, validates empty inputs
- **SignupActivity** — Username + Email + Password, min 6 char password check
- **WelcomeActivity** — displays logged-in user's email, Logout button
- Navigation: Login ↔ Signup (tap link), Login → Welcome (on success), Logout → Login
- Error messages shown inline on EditText fields
- Toast messages for success/failure

---

## Project Structure

```
src/main/java/project/loginpage/
├── LoginActivity.kt      ← Email/password login with Firebase Auth
├── SignupActivity.kt     ← New user registration
├── WelcomeActivity.kt    ← Post-login screen with email display + logout
├── MainActivity.kt       ← Entry point (redirects to Login)
├── User.kt               ← User data model
└── UserDatabaseHelper.kt ← Database helper utility
```

---

## Flow

```
App Launch
    └─► LoginActivity
            ├─ [Login success]  ──► WelcomeActivity ──► [Logout] ──► LoginActivity
            └─ [Sign Up link]   ──► SignupActivity
                                        └─ [Registration success] ──► LoginActivity
```

---

## Requirements

- Android Studio Hedgehog or later
- Min SDK: 24
- Language: Kotlin
- Service: Firebase Authentication
- Theme: Material Components Purple (`#6200EE`) + DarkActionBar
