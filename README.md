updated ISE documentation in Markdown format, reflecting the changes 

# ISE (Interface Style Enliner) Documentation

ISE is a language for building interactive web apps quickly, with easy-to-use elements and attributes. **Do not use JavaScript**. We use our own system which is different from normal JS.

Always include ISE in your project:

```html
<script src="https://ise.web.app/load/l.js"></script>  <!-- CDN (MUST) -->
<link rel="stylesheet" href="https://ise.web.app/load/l.css">  <!-- UI (Optional but better to put) -->
```

---

## Elements in ISE

- `<see>`: Screen in the App
- `<say>`: Say text in the App
- `<ask>`: Ask input in the App (All data here is auto-saved)
- `<row>`: Row in the App
- `<cam>`: Camera Display in the App
- `<bon>`: Fluffy Box for the App
- `<app>`: Creates an App Settings Container Element

---

## Element Attributes

- `<see pop="COLOR">`: Sets Global Pop Color in the App
- `<see min="COLOR">`: Sets Global Mint Color in the App

### Colors:
- **Pop**: `<? pop>`
- **Mint**: `<? min>`
- **Redirect**: `<? go="URL">` (Redirect to URL when tapped)
- **Run JS**: `<? do="URL">` (Runs JS when tapped or typed into it)
- **Save**: `<? save="mydata" file="txt">` (Creates a file with data from `<ask>` that is selected)
- **Upload**: `<? upload="mydata">` (Uploads file data from `<ask>` that is selected)

### Color Options:
- `[r]`: Red Cherry
- `[l]`: Blue Lin
- `[y]`: Yellow Mango
- `[v]`: Violet Grapes
- `[p]`: Pink Peach
- `[g]`: Green Grass
- `[m]`: Matte White
- `[b]`: Black

To apply as background color, use `+bg`:

```html
<? lbg
```

---

## Functionality in `<script>`

- `ui(1)`: Start UI
- `bon('ask')`: Select Element
- `bon.add('ask')`: Makes Element

### Element Manipulation:

- `hide('#mysc')`: Toggle Hide
- `.at('lbg')`: Toggle Attribute
- `.rem('lbg')`: Remove Attribute
- `.put`: Put Element as a Child
- `.del`: Remove Element

### Server Functions:

- `server.post`: Post Data to Server
- `server.put`: Put Data to Server
- `server.patch`: Patch Data on Server
- `server.get`: Get Data from Server
- `server.del`: Delete Data from Server

### Camera and Microphone:

- `on.cam`: Turn on Camera
- `off.cam`: Turn off Camera
- `on.mic`: Turn on Microphone
- `off.mic`: Turn off Microphone

---

## App Settings Functions

- `app.view()`: Makes the App Responsive and Native
- `app.info("My first ISE app")`: Sets SEO for the App
- `app.key("apple, fruit")`: Set App Settings Keywords

### App Customization:

- `app("My App")`: Set Name for App
- `app.icon(1)`: Select Icon for App
- `app.cover(1)`: Select Cover for App

---

This documentation provides an overview of how to use ISE to build interactive web apps without JavaScript. Use the elements and attributes to quickly design and implement dynamic features in your app.
```

This Markdown version matches the updated elements, attributes, and functions for ISE based on your description. Let me know if you need further modifications!
