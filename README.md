Remote Presentation Controller
==============================

Simple Remote Presentation Controller for Reveal.js using Node.js.
Presenter can use their mobile devices to control the slides via the controller web interface.

<img src="http://www.ngo-hung.com/files/images/RemotePresenter.png" />
[Blog Link](http://www.ngo-hung.com/blog/2012/07/16/remote-controller-for-reveal-js-presentation)

## Install

1) Install node.js

2) Run

node app.js

3) Preloaded with 2 sample presentations:

- [http://localhost:3000/demo](http://localhost:3000/demo) : Demo presentation from <http://lab.hakim.se/reveal-js>
- <http://localhost:3000/myppt>

Open another browser window to open the remote controller:

<http://localhost:3000/controller>

Users can issue up, down, left, right commands to navigate through the slides.

To remote control, just use the dropdown to select which presentation to control, then select one of the slides. 


## Note

- config/index.js: configure the list of presentations and its initial slides
- routes/index.js: server logic
- views/controller.ejs: controller client logic
- views/layout.ejs: most of the logic for a normal presentations 
- views/demo.ejs: actual html for 'Demo Presentation'
- views/myppt.ejs: html for 'My Presentation'



notes:
why webpack?

is it right for you? At any level you can reap benefits using webpack but ideally you only NEED to use it if you are writing massive javascript applications 

is webpack the only js package manager on the block? No there has always been browsify, and more recently jspm with SystemJS. I chose webpack because I felt it matched our needs.

why use typescript with webpack? To acheive optimal flexibility, future proofing, and readability.

webpack can be used for bundling anything. javascript, css, images, html

then webpack will remove whitespace and minify to reduce footprint.

webpack helps handle file order dependencies

illustrate via scripts

<head>
    <script src="this.js"></script>
    <script src="that.js"></script>
</head>

transpilation

you can write code in es6 and transpile into es5 using something like babel or it lets you use typescript so you can even use something like coffeescript if you wanted too

webpack can lint your code

combining files

minifying files

maintaing file order

transpilation

linting

other solutions
server side tools such as asp.net budnling features,rails, etc
server side tool combines and minifies them may or may not handle transpiling and don't handle linting

task runners
grunt, gulp
can do almost anything and can do evertyhing if configured correctly. usually browsify is combined with a task runner to accomplish the same thing.

webpack is jsut a specialized task runner

uses loaders to turn a source file into loader and one or more files come out.

transpilation concatenaction and minification

webpack uses npm instead of bower

next pick a module system whether AMD, commonJS or es6

the only restriction is that we can't have circular dependencies

commonjs
var item1 = require('./item1');

cli
config files
dev server
loaders
production builds

CLI

install webpack
npm install webpack -g
webpack input output

config

webpack.config
it is basically a commonjs module
setup entry point
setup output {"filenName":"bundle.js"}



this assumes you've already bought into the idea of architecting your code uising modules to begin with.

next demonstrate what a module structure looks like

illustrate what the structure looks like as a tree from the entry point

go over configuration

show how it bundles to one js

show how you can do annotations

building typings

show minification

typescript loader
