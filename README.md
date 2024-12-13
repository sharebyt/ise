
# ISE (Interface Style Enliner) Documentation

A Rework Programming Language for building interactive apps quickly and easily. 
You don’t need to write JavaScript or Other like in other development.

ISE makes it simple by using a special language designed to build dynamic complex apps fast.
This language is not Compiled or What.

### **How to Use ISE in Your Project**

To use ISE, just add the following code to your project:

```html
<script src="https://ise.web.app/load/l.js"></script>  <!-- This is the ISE script (MUST) -->
<link rel="stylesheet" href="https://ise.web.app/load/l.css">  <!-- Optional UI (but it looks better with it) -->
```

---

## **What Elements Can You Use in ISE?**

ISE gives you a set of easy-to-use elements to create your app. Here are the main ones:

- `<see>`: Shows the main screen in the app.
- `<say>`: Displays text in the app.
- `<ask>`: Asks the user for input. (All data entered here is automatically saved.)
- `<row>`: Creates a row layout in your app.
- `<cam>`: Shows the camera display in the app.
- `<bon>`: A "fluffy box" for any content you want to show.
- `<app>`: Contains settings for your app.

---

## **Adding Colors and Features to Your Elements**

You can customize elements with colors and special features. Here’s how:

- **Global Colors**: 
  - `<see pop="COLOR">`: Changes the main color in your app.
  - `<see min="COLOR">`: Changes the secondary color in your app.

### **Colors You Can Use:**

- **[r]** Red Cherry
- **[l]** Blue Lin
- **[y]** Yellow Mango
- **[v]** Violet Grapes
- **[p]** Pink Peach
- **[g]** Green Grass
- **[m]** Matte White
- **[b]** Black

To set a background color, use `+bg`. For example:

```html
<see pop="rbg">This text has a red background!</see>
```

---

## **What Else Can You Do with ISE?**

Here’s a list of features and what they do. You can use these to control your app and make it work the way you want:

### **Main Functions:**

- `ui(1)`: Starts the UI for your app.
- `bon('ask')`: Select an element (like an input box).
- `bon.add('ask')`: Add a new input box to your app.

### **Element Controls:**

- `hide('#mysc')`: Hides an element (for example, a screen or section).
- `.at('lbg')`: Change an element’s background.
- `.rem('lbg')`: Remove a background from an element.
- `.put`: Add an element inside another one.
- `.del`: Remove an element from the app.

### **Interacting with the Server:**

You can send and get data from a server using these commands:

- `server.post`: Send data to the server.
- `server.put`: Update data on the server.
- `server.patch`: Change specific data on the server.
- `server.get`: Retrieve data from the server.
- `server.del`: Delete data from the server.

### **Camera and Microphone Controls:**

- `on.cam`: Turn on the camera.
- `off.cam`: Turn off the camera.
- `on.mic`: Turn on the microphone.
- `off.mic`: Turn off the microphone.

---

## **App Settings**

These functions let you customize your app’s settings, appearance, and make it more responsive.

- `app.view()`: Makes your app responsive (it will look good on all devices).
- `app.info("My first ISE app")`: Set SEO settings for your app.
- `app.key("apple, fruit")`: Add keywords for search engines.

### **App Customization:**

- `app("My App")`: Set the name of your app.
- `app.icon(1)`: Choose an icon for your app.
- `app.cover(1)`: Set a cover image for your app.

---

## **Final Notes**

With ISE, you don’t need to learn complex code. Just use the elements and commands to build your app visually. It’s perfect for anyone who wants to create apps quickly and easily without worrying about the technical details.

Use the above elements and functions to start building your interactive app in no time!

