ISE (Interface Style Enliner) Documentation

ISE is a language for building interactive web apps quickly, with easy-to-use elements and attributes.

Start by including ISE in your project:

<script src="https://ise.web.app/load.js"></script>
<link rel='stylesheet' href='https://ise.web.app/load.css'>                -- Only UI

Ways to Interact

ask(message)
Prompts the user for input.
ask("What's your name?").then(name => bon('#body').put(`Hello, ${name}!`));

say(message)
Displays a message on the screen.
say("Welcome to my app!");

clear()
Clears any messages or prompts.
clear();

Ways to Create Your Bon
A “Bon” is any part of your page you can create, change, or interact with.

bon(selector)
Finds something already on your page.
bon("#header").text = "Welcome to ISE!";

bon.add(tag)
Creates new content (button, text, etc.).
const mybon = bon.add();
mybon.text = "Hello, World!";
dom("#body").put(mybon);

.put(content)
Adds content inside another Bon.
bon("#container").put("New content");

.at(attribute, value)
Modifies attributes for a Bon.
bon("#box").at("hide");
bon("#box").at("rbg");

.text
Gets or sets the text inside a Bon.
bon("#title").text = "Hello!";

ISE Elements

<textarea placeholder="Write here..."></textarea>    - Input box for user text.
<a>Click Me</a>                                      - Clickable button.
<p>Welcome to ISE!</p>                               - Paragraph with text.
<bon>Hello, Fluffy World!</bon>                       - A container for content.
<row><bon>Item 1</bon><bon>Item 2</bon></row>         - Horizontal layout.
<setup>Loading...</setup>                            - App initialization.
<md># Markdown Header</md>                           - Displays Markdown content.
<out>Dynamic Output Here</out>                       - Dynamic output.
<style>bon { border: 2px solid black; }</style>        - Custom CSS.
<script>say("ISE is fun!");</script>                  - JavaScript code.

Attributes (Signs)

Colors: Black (b), Blue (l), Red (r), Yellow (y), Green (g), Violet (v), Matte White (m), Pink (p).

Example:
<p r>This is red text.</p>
<bon bbg>This has a black background.</bon>
<bon bbg2>This has a dim black background.</bon>

Corners and Spacing: Margin (m) and Padding (p)
- Small, mid, big sizes: `<bon small-m>` `<bon mid-pt>`
- Corners: 5, 10, 15, 25, 50

Layout
Align elements:
<? center> - Centered layout.
<? left>   - Left-aligned layout.
<? right>  - Right-aligned layout.
<? masonry> - Masonry layout.

Flex (auto layout)
`flex` automatically arranges content in a flexible layout.
<bon flex>Content arranged flexibly</bon>

Layer (1-4)
`layer` sets the stacking order of elements, with `1` being the lowest.
<bon layer="2">Layer 2 content</bon>

Fixed
`fixed` positions an element relative to the viewport.
<bon fixed>Fixed content</bon>

Lock (unable to copy)
`lock` prevents the content from being copied.
<bon lock>This content can't be copied</bon>

Column (col)
`col` sets up a column-based layout.
<row col> 
  <bon>Column 1</bon>
  <bon>Column 2</bon>
</row>

Grid (1-4)
`grid` arranges content into a grid (1-4 columns).
<row grid="3"> 
  <bon>Grid 1</bon>
  <bon>Grid 2</bon>
  <bon>Grid 3</bon>
</row>

Default UI Settings

ui()                          - Set up default UI.
set.cover(imageNumber)         - Set a background cover image.
set.icon(iconNumber)           - Change favicon.
set.title("My App")            - Update page title.
set.key("ISE, web, app")       - Add keywords.
set.info("An app built with ISE.") - Page description.
set.view()                     - Optimize for all devices.

Saving to Storage

save(key, value)               - Store data locally.
save.load(key)                 - Retrieve stored data.
bon("#welcome").put(`Hello, ${save.load("user")}!`);

Files, Data, and URLs

up()                           - Upload file from user.
down(content, filename)        - Download content as a file.
url.set({ page: "home" })      - Update URL with query params.
url.get()                      - Get current URL info.

Talk to Your Server

server.post(url, data)         - Send data to server.
server.get(url)                - Get data from server.
server.put(url, data)          - Update data on server.
server.del(url)                - Delete data from server.

Extra’s

uuid()                        - Generate unique ID.
ran(max)                       - Get random number (up to max).
copy(text)                     - Copy text to clipboard.
rec.start()                    - Start screen recording.
rec.stop()                     - Stop recording and save file.
