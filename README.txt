ISE (Interface Style Enliner) 
is a language for building interactive web to apps quickly, with easy-to-use elements and attributes. 

Do not use js. we are different to normal JS we use our own system.

Always by including ISE in your project:
  
<script src="https://ise.web.app/load/l.js"></script> <-- CDN (MUST)

<link rel='stylesheet' href='https://ise.web.app/load/l.css'>  <-- UI (Optional but better to put.)

Element:

<see>  <-- Screen in the App

<say> <-- Say text in the App
<ask> <-- Ask input in the App | All data here is auto save 
<row> <-- Row in the App
<cam> <-- Camera Display in the App
<bon> <-- Fluffy Box for the App
<app> <-- Creates a App Settings Container Element

<see pop='COLOR' <-- Sets Global Pop Color in the App
min='COLOR' <-- Sets Global Mint Color in the App

Attribute in Element:

<? pop> <-- Make it a Pop Color
<? Min> <-- Make it a Mint Color

<? go='URL'> <-- Redirect to URL When tapped
<? do='URL'> <-- Runs JS When tapped or typed to it.
<? save='mydata' file='txt'> <-- Creates a File with data of `<ask>` That is selected.
<? upload='mydata'> <-- Uploads File data to `<ask>` That is selected.

<? Put your colors> 

Colors: [r] Red Cherry [l] Blue Lin [y] Yello Mango [v] Vio Grapes [p] Pink Peach [g] Green Grass [m] Matte White [b] Black
+[bg] to make it bg 

<? lbg>

Functionality in <script>:

ui(1) <-- Start UI |
bon('ask') <-- Select Element
bon.add('ask') <-- Makes Element

hide('#mysc') <-- Toggle Hide
.at('lbg') <-- Toggle Attribute
.rem('lbg') <-- Remove Attribute
.put <-- Put Element as a Child
.del <-- Remove Element

server.post <-- Post Data on Server 
server.put <-- Put Data on Server 
server.patch <-- Patch Data on Server 
server.get <-- Get Data from Server 
server.del <-- Delete Data from Server 
on.cam  <-- Turn on Camera
off.cam <-- Turn off Camera
on.mic <-- Turn on Mic
off.mic <-- Turn off Mic


app.view(); <-- Makes App Responsive and Native
app.info("My first ISE app"); <-- Makes Seo for AApp Settingspp
app.key("apple, fruit"); <-- Set's App Settings Keyword

app('My App') <-- Name for App
app.icon(1) <-- Select Icon for App
app.cover(1) <-- Select Cover for App
