                ISE (Interface Style Enliner) Documentation
   ________________________________________________________________

    ISE is a language for building interactive web apps quickly, with
    easy-to-use elements and attributes. 

    Do not use JavaScript. We are different from normal JS as we use our own system.

    Always include ISE in your project:

    <script src="https://ise.web.app/load/l.js"></script>  <-- CDN (MUST)
    <link rel='stylesheet' href='https://ise.web.app/load/l.css'>  <-- UI (Optional but better to put.)

------------------------------------------------------------------

                  Elements in ISE:

    <see>        <-- Screen in the App
    <say>        <-- Say text in the App
    <ask>        <-- Ask input in the App | All data here is auto-saved
    <row>        <-- Row in the App
    <cam>        <-- Camera Display in the App
    <bon>        <-- Fluffy Box for the App
    <app>        <-- Creates an App Settings Container Element

------------------------------------------------------------------

                  Element Attributes:

    <see pop='COLOR'>       <-- Sets Global Pop Color in the App
    <see min='COLOR'>       <-- Sets Global Mint Color in the App

    <? pop>                 <-- Make it a Pop Color
    <? min>                 <-- Make it a Mint Color
    <? go='URL'>            <-- Redirect to URL when tapped
    <? do='URL'>            <-- Runs JS when tapped or typed into it
    <? save='mydata' file='txt'> <-- Creates a file with data from `<ask>` that is selected
    <? upload='mydata'>     <-- Uploads file data from `<ask>` that is selected

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

    ui(1)                     <-- Start UI
    bon('ask')                <-- Select Element
    bon.add('ask')            <-- Makes Element

    hide('#mysc')             <-- Toggle Hide
    .at('lbg')                <-- Toggle Attribute
    .rem('lbg')               <-- Remove Attribute
    .put                      <-- Put Element as a Child
    .del                      <-- Remove Element

    server.post               <-- Post Data on Server
    server.put                <-- Put Data on Server
    server.patch              <-- Patch Data on Server
    server.get                <-- Get Data from Server
    server.del                <-- Delete Data on Server
    on.cam                    <-- Turn on Camera
    off.cam                   <-- Turn off Camera
    on.mic                    <-- Turn on Mic
    off.mic                   <-- Turn off Mic

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
