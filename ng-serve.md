## So what does `npm start` do anyways?

When you type in npm start, it goes and looks into your package.json and runs whatever is defined under “start” in the “scripts”.
So, if your package.json looks like this:

`{
“name”: “hello-world”,
“version”: “0.0.1”,
“license”: “MIT”,
“scripts”: {
“ng”: “ng”,
“start”: “ng serve –proxy-config proxy.conf.json”,
“build”: “ng build”,
“test”: “standard && ng test”,
“lint”: “ng lint”,
“e2e”: “ng e2e”
}`
 
Running npm start would run the `ng serve`.

If no “start” property is specified on the “scripts” object, it will run node server.js.

which means it will call the start scripts inside the package.json

ng serve is provided by `angular/angular-cli` to start angular2 apps which created by angular-cli. when you install angular-cli, it will create ng.cmd under C:\Users\name\AppData\Roaming\npm (for windows) and execute "%~dp0\node.exe" "%~dp0\node_modules\angular-cli\bin\ng" %*

So using npm start you can make your own execution where is ng serve is only for angular-cli

references: http://stackoverflow.com/a/40190781
