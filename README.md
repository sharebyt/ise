
<link rel='stylesheet' href='https://ise.web.app/load.css'>
# ISE (Interface Style Enliner) Documentation  

**ISE** is a language for building interactive web apps quickly. With easy-to-use elements and attributes, you can design and build dynamic apps efficiently. It’s protected by the **WEBOPL** license.

Start by including ISE in your project:  
```html
<script src="https://ise.web.app/load.js"></script>
```

---

## **Ways to Interact**  
### **`ask(message)`**  
Prompts the user for input.  
```javascript
ask("What's your name?").then(name => bon('#body').put(`Hello, ${name}!`));
```

### **`say(message)`**  
Displays a message on the screen.  
```javascript
say("Welcome to my app!");
```

### **`clear()`**  
Clears any messages or prompts.  
```javascript
clear();
```

---

## **Ways to Create Your Bon**  
A "Bon" is any part of your page you can create, change, or interact with.  

### **`bon(selector)`**  
Finds something already on your page.  
```javascript
bon("#header").text = "Welcome to ISE!";
```

### **`bon.add(tag)`**  
Makes something new, like a button or text.  
```javascript
const newDiv = bon.add("div");
newDiv.text = "Hello, World!";
bon("#body").put(newDiv);
```

### **`.put(content)`**  
Adds something inside another Bon.  
```javascript
bon("#container").put("Here is new content.");
```

### **`.at(attribute, value)`**  
Adds or modifies attributes for a Bon.  
```javascript
bon("#box").at("hidden"); // Hides the box
bon("#box").at("class", "highlight"); // Adds a class to the box
```

### **`.text`**  
Changes or retrieves the text inside a Bon.  
```javascript
bon("#title").text = "Hello!";
```

---

## **ISE Elements**  
These special elements simplify app building.  

- **`textarea`**: An input box for user text.  
  ```html
  <textarea placeholder="Write here..."></textarea>
  ```
- **`a`**: A clickable button.  
  ```html
  <a>Click Me</a>
  ```
- **`p`**: A text paragraph, also styled like `md` (Markdown).  
  ```html
  <p>Welcome to ISE!</p>
  ```
- **`bon`**: A fluffy box for any content.  
  ```html
  <bon>Hello, Fluffy World!</bon>
  ```
- **`row`**: A horizontal layout.  
  ```html
  <row>
    <bon>Item 1</bon>
    <bon>Item 2</bon>
  </row>
  ```
- **`setup`**: For app initialization.  
  ```html
  <setup>Loading...</setup>
  ```
- **`md`**: Displays Markdown-style content.  
  ```html
  <md># Markdown Header</md>
  ```
- **`out`**: Dynamic output.  
  ```html
  <out>Dynamic Output Here</out>
  ```
- **`style`**: Adds custom CSS.  
  ```html
  <style>
    bon { border: 2px solid black; }
  </style>
  ```
- **`script`**: Embeds JavaScript code.  
  ```html
  <script>
    say("ISE is fun!");
  </script>
  ```

---

## **Attributes (Signs)**  

### **Colors**  
Set colors for text or backgrounds:  
- **Black (`b`)**, **Blue (`l`)**, **Red (`r`)**, **Yellow (`y`)**, **Green (`g`)**, **Violet (`v`)**, **Matte White (`m`)**, **Pink (`p`)**.  

Examples:  
- Set text color:  
  ```html
  <p r>This is red text.</p>
  ```  
- Background color (`bg`):  
  ```html
  <bon bbg>This has a black background.</bon>
  ```  
- Dimmed colors: Add `2`.  
  ```html
  <bon bbg2>This has a dim black background.</bon>
  ```

---

### **Corners,Spacing (Margins and Padding)**  
Use margins and padding to control spacing:  
- **Sizes**: `small`, `mid`, `big`.  
- **Position**:  
  - `t` = Top  
  - `b` = Bottom  
  - `l` = Left  
  - `r` = Right
`m` = Margin All sides  
`p` = Pad All sides  

Examples:  
- Margin:  
  ```html
  <bon small-m>This box has a small margin.</bon>
  ```  
- Padding:  
  ```html
  <bon mid-pt>This box has mid padding at the top.</bon>
  ```
Corner Sizes:
'5' 5% | '10' 10% | '15' 15% | '25' 25% | '50' 50% 
- Corner:  
```html
<bon bdr="15">This box has mid padding at the top.</bon>
```

---

### **Layout**  
Arrange elements easily with these options:  
- Centered: `<row center>`  
- Left: `<row left>`  
- Right: `<row right>`  
- Masonry Layout: `<row masonry>`  

Example:  
```html
<row center>
  <bon>Item 1</bon>
  <bon>Item 2</bon>
</row>
```

---

## **Default UI or Set It Your Way**  
### **`ui()`**  
Sets up the default UI.  
```javascript
ui();
```

### **`set.cover(imageNumber)`**  
Sets a background cover image.  
```javascript
set.cover(1);
```

### **`set.icon(iconNumber)`**  
Changes the page favicon.  
```javascript
set.icon(2);
```

### **`set.title(title)`**  
Updates the page title.  
```javascript
set.title("My App");
```

### **`set.key(keywords)`**  
Adds keywords for the page.  
```javascript
set.key("ISE, web, app");
```

### **`set.info(description)`**  
Updates the page description.  
```javascript
set.info("An app built with ISE.");
```

### **`set.view()`**  
Optimizes the page for all devices.  
```javascript
set.view();
```

---

## **Saving to Storage**  
### **`save(key, value)`**  
Stores data locally.  
```javascript
save("user", "John");
```

### **`save.load(key)`**  
Retrieves stored data.  
```javascript
bon("#welcome").put(`Hello, ${save.load("user")}!`);
```

---

## **Files, Data, and URLs**  

### **`up()`**  
Uploads a file from the user.  
```javascript
up().then(file => bon("#fileName").put(file.name));
```

### **`down(content, filename)`**  
Downloads content as a file.  
```javascript
down(bon("#myinput").text, "example.txt");
```

### **`url.set(query)`**  
Updates the URL with query parameters.  
```javascript
url.set({ page: "home" });
```

### **`url.get()`**  
Gets the current URL information.  
```javascript
bon("#urlInfo").put(url.get());
```

---

## **Talk to Your Server**  

### **`server.post(url, data)`**  
Sends data to the server.  
```javascript
server.post("/api/save", { name: "ISE" });
```

### **`server.get(url)`**  
Gets data from the server.  
```javascript
server.get("/api/data").then(data => bon("#data").put(data));
```

### **`server.put(url, data)`**  
Updates data on the server.  
```javascript
server.put("/api/update", { name: "New Name" });
```

### **`server.del(url)`**  
Deletes data on the server.  
```javascript
server.del("/api/delete");
```

---

## **Extra's**  

### **`uuid()`**  
Generates a unique ID.  
```javascript
bon("#id").put(uuid());
```

### **`ran(max)`**  
Gives a random number up to the max.  
```javascript
bon("#random").put(ran(100));
```

### **`copy(text)`**  
Copies text to the clipboard.  
```javascript
copy("ISE is awesome!");
```

### **`rec.start()`**  
Starts screen recording.  
```javascript
rec.start();
```

### **`rec.stop()`**  
Stops recording and saves the file.  
```javascript
rec.stop();
```
