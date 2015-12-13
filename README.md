# ember-fps
<b>Ember.js for Polish students<b/>

***

This tutorial provides an introduction to the Ember.js - a framework for creating ambitious web applications. We'll build a simple web app using Ember and Node as a runtime environment for JavaScript. Before we'll start make sure that you've got a working knowledge of:
* HTML
* CSS
* JavaScript

It would be great if you know something about an ECMAScript 6 syntax. That's the newest standard of JavaScript and our framework uses it.

We'll be working with Linux's command line, but if you're a Windows user, don't worry! Magical skills aren't needed.

***

<b>Installing Node and npm</b>

Open a terminal and install nodejs and npm packages. Every command should be executed with sudo or as root user.

If you're a Debian/Ubuntu/Mint user, it would be something like that:

<code>apt-get install nodejs npm</code>

If you prefer Fedora:

<code>dnf install nodejs npm</code>

And if you're into Arch:

<code>pacman -S nodejs npm</code>

Node.js is a JavaScript runtime. Ember (like many other web app frameworks and libraries ) requires Node for working. npm is Node's package ecosystem. It works similarly to apt or aptitude in Debian but is dedicated to deal with web apps' dependencies.

Now watch carefully! We've installed nodejs from package called (sic!) nodejs, but we want Ember to work with <b>Node</b> app. Ember would be confused if it's looking for Node and can't find it. That's because Node binary's not on your $PATH. Let's change a symlink to solve that!

<code>ln -s /usr/bin/nodejs /usr/bin/node</code>

Now let's check if it works:

<code>node --version</code>
<code>npm --version</code>

If it does - it's time to install Ember!

<b>Installing Ember</b>

Just install ember-cli using npm:

<code>npm install -g ember-cli</code>

If your npm throws errors, you probably have to use sudo.

Now check if Ember works:

<code>ember -v</code>

If you had to install Ember with sudo, you'll probably have to use it also with ember-cli. That's confusing (especially that we'll be using bower). But first things first.

If you see something like:
<code>version: 1.13.13</code>
or just:
<code>version: 2.2.0</code>
it's OK.

Now let's create our first Ember app!

***

<b>Creating an app</b>

Open your terminal and type:

<code>ember new my-first-app</code>

Instead of [my-first-app] you can type whatever you want. Sure!

Wait a minute. Ember works hard for you!

If you see something like:

<code>Successfully initialized git.</code>

<code>Installing packages for tooling via npm...</code>

<code>Installed packages for tooling via npm.</code>

<code>Installed browser packages via Bower.</code>

Congratulations! You've just created your first Ember app!

If something went wrong check if you've got installed git package. Maybe Bower doesn't work? Then try type:

<code>bower install</code>

Bower is package manager for the web, but since it's a user command, it doesn't require sudo. If your OS sends you permission errors when using bower without sudo, run it with --allow-root option:

<code>sudo bower install --allow-root</code>

***

<b>Running server</b>

Now open my-first-app folder:

<code>cd my-first-app</code>

And run Ember server:

<code>ember server</code>

Open your browser and type:

<code>http://localhost:4200/</code>

4200 is the default port for Ember server.

If you see:

<code>Welcome to Ember</code>

Everything works!

Now it's time to spend a few minutes and learn something about MVC (Model View Controller) in Ember. If you know Ruby on Rails, make yourself at home!

<a href="http://guides.emberjs.com/v2.2.0/getting-started/ember-cli/">Core Concepts</a>
