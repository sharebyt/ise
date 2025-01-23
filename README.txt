█ ▄█▀ █▀
        ▀
ISE (Interface Style Enliner) Documentation
________________________________________________________________

ISE is a language for building interactive software quickly, fast, native, web, with
easy-to-use system. 

When you add this. Do not use it like its JavaScript. We are different from normal JS as we use our own system.

Must include ISE in your project:
<script src="https://ise.web.app/v1.7/l.js"></script>  <-- CDN (MUST)
<link rel='stylesheet' href='https://ise.web.app/v1.7/l.css'>  <-- UI (MUST)

ISE (Interface Style Enliner) is a redo type language which
means it is coded by using it self. ISE uses C, JS, CSS, HTML,
Markdown and Sen UI to create ISE. ISE is a Native HTML liked language but also can work as cdn in your own HTML project.
| ISE is devided in 3 Structure,
1st <app>
The app Settings with js liked syntax. 2nd <body> Where all UI will be put.
Last the <script> . 


------------------------------------------------------------------

3 Structure of ISE

1. `<app>`        <-- The app Settings with js liked syntax.

like
`<app>
app.view();
app("My ISE app TITLE");
app.info("My first ISE app");
app.key("apple, fruit");

app.cover(1);
app.icon(1);
</app>`

2. <body> 
like
`<body>

<see mid mbg center>
<bon>
<say b mid quick>code en</say>
<say b>What App is on your mind?</say>
</bon>
</body
`

3. Script
where all scripting or other features will be coded
<script>
x=()=>{}
</script>

------------------------------------------------------------------

Elements in ISE:

<see>        <-- Screen in the App
<say>        <-- Say text in the App
<ask>        <-- Ask input in the App | All data here is auto-saved
<row>        <-- Row in the App
<cam>        <-- Camera Display in the App
<feed>        <-- Screen Display in the App
<bon>        <-- Fluffy Box for the App
<app>        <-- Creates an App Settings Container Element

------------------------------------------------------------------

Element Attributes:

<see pop='COLOR'>       <-- Sets Global Pop Color in the App
<see min='COLOR'>       <-- Sets Global Mint Color in the App

[pop]                 <-- Make it a Pop Color
[min]                 <-- Make it a Mint Color
[go='URL']            <-- Redirect to URL when tapped
[do='URL']            <-- Runs JS when tapped or typed into it
[save='mydata' file='txt'] <-- Creates a file with data from `<ask>` that is selected
[upload='mydata']     <-- Uploads file data from `<ask>` that is selected

------------------------------------------------------------------

Colors in ISE:

[r] Red Cherry
[l] Blue Lin
[y] Yellow Mango
[v] Violet Grapes
[p] Pink Peach
[g] Green Grass
[m] Matte White
[b] Black

Add +[bg] to make it a background color (e.g., <? lbg>).

------------------------------------------------------------------

Functionality in `<script>`:

Baseline

say('TEXT')               <-- This Will tell the user. With Baseline UI.
ask('TEXT')               <-- This Will ask (Input) the user. With Baseline UI.
ui(1)                     <-- Dynamical Start UI (No need to add it's auto.)
bon('ask')                <-- Select Element
bon.add('ask')            <-- Makes Element

hide('#mysc')             <-- Toggle Hide
.at('lbg')                <-- Toggle Attribute
.rem('lbg')               <-- Remove Attribute
.put(CHILD)               <-- Put Element as a Child
.del(TARGET)              <-- Remove Element

------------------------------------------------------------------

Local

local.set(name, data);         <-- Set data from Local
local.get(name);               <-- Get data from Local

------------------------------------------------------------------

Servers

server.post(url, {data})               <-- Post Data on Server
server.put(url, {data})                <-- Put Data on Server
server.patch(url, {data})              <-- Patch Data on Server
server.get(url, {data})                <-- Get Data from Server
server.del(url, {data})                <-- Delete Data on Server

------------------------------------------------------------------
Hardware

on.cam()                    <-- Turn on Camera
off.cam()                   <-- Turn off Camera

on.feed()                   <-- Turn on Screen Cast
off.feed()                  <-- Turn off Screen Cast

on.mic()                    <-- Turn on Mic
off.mic()                   <-- Turn off Mic

snap('cam')                 <-- Snap a Photo on Camera.
snap('feed')                <-- Screenshot the Display.

rec.start('cam')            <-- Record a Video of Camera.
rec.start('feed')           <-- Record a Video of Display.
rec.stop()

------------------------------------------------------------------

General

uuid()                   <-- Generates a UUID.

ran(9e9)                 <-- Generates a Random Number.

copy('Text')             <-- Will put a data on User Clipboard

key(['ctrl','c'], 
() => {                  <-- Event if key is click on keyboard event will run.
snap('cam')
});

delay(
()=>{
say('What')
}
, 1)                     <-- Will run a Function after a the delay is done,
                             In this sample after Second a func runs.

------------------------------------------------------------------

App Settings Functions:

app.view();               <-- Makes the App Responsive and Native
app.info("My first ISE app"); <-- Sets SEO for App
app.key("apple, fruit");  <-- Set App Settings Keywords

app('My App')             <-- Set Name for App
app.icon(1)               <-- Select Icon for App
app.cover(1)              <-- Select Cover for App

------------------------------------------------------------------

This documentation serves as an overview of ISE's capabilities for building apps
using our simplified, like JavaScript + HTML approach. Get started by including ISE, then
use the provided elements and attributes to build out your app's functionality.
