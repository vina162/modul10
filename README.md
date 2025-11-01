# 🎮 Flutter Game Store App

A modern and dynamic Flutter application that displays a collection of *free-to-play games* using API data.  
Users can view the game list on the *Home Page* and navigate to a detailed page using *named routes*.

---

## 🧩 Features

✅ Fetches real-time game data from an API  
✅ Displays game details such as title, genre, platform, and publisher  
✅ Uses *Navigator* with *named routes* for smooth page transitions  
✅ Responsive UI built with *Material Design*  
✅ Clean architecture separating *views* and *logic*

---

## 🧱 Project Structure

```
lib/
├── main.dart              # Entry point with MaterialApp and routes
├── view/
│   ├── home.dart          # Main page displaying game list
│   ├── detail.dart        # Detail page showing game info
```

---

## ⚙️ How It Works

1. The app launches via `main.dart`, initializing a `MaterialApp` with two routes:
   - `'/'` → *Home()* — displays the main game list
   - `'/detail'` → *Detail()* — displays selected game information

2. When a game is selected on the home screen, the app navigates to the *detail page*:
   ```dart
   Navigator.pushNamed(
     context,
     '/detail',
     arguments: gameId,
   );
   ```

3. The *Detail Page* receives the `gameId` through the route argument and loads the detailed game information.

---

## 💡 Code Explanation

### 🔹 main.dart
- Sets up routes and navigation system
- Customizes the *status bar color* using `SystemChrome`
- Initializes `Home` as the default page

```dart
SystemChrome.setSystemUIOverlayStyle(const SystemUiOverlayStyle(
  statusBarColor: Colors.transparent,
  statusBarIconBrightness: Brightness.dark,
));
```

---

## 🖥️ UI Preview

```
-----------------------------------------
|         🎮 Game Store App             |
|---------------------------------------|
|   [ Game 1 Thumbnail  ]  Game Title   |
|   [ Game 2 Thumbnail  ]  Game Title   |
|                                       |
|   → Tap to view details               |
-----------------------------------------
|             Detail Page               |
|   - Title                             |
|   - Genre, Platform, Publisher        |
|   - Description                       |
-----------------------------------------
```

---

## 🧰 Tech Used

- *Flutter SDK*
- *Dart*
- *Material Design*
- *HTTP package* (for API fetching)
- *Navigator Named Routes*
- *SystemChrome for UI customization*

---

## 🧠 Result Summary

This project showcases how to build a simple yet powerful Flutter app that integrates:
- API data fetching,
- UI navigation with named routes,
- and real-time display of dynamic content.

It’s a great foundation for *learning Flutter routing*, *state handling*, and *API integration* in an organized structure.

---

✨ *Built with Flutter — Beautiful UIs, Fast Development, Native Performance.*
