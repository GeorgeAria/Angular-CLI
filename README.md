# Angular-CLI
This repo gives an overview of the Angular CLI.


# Random Tips/Definitions

* If VSCode is the IDE that is being used to make Angular applications, it is best to install
the "Angular Essentials" extention. It will make life easy when making Angular applications.

* Use Prettier (a Visual Studio Code extension) to make your code more visually appealing.
To use it, hold "Shift -> Alt -> F" to make your code "Prettier".

* End to end tests are used to test app behavior through user interaction. They are great to test out use cases and use Protractor with Angular.


## Angular Commands
* ng new (or n) "application name"
Generates a new Angular application
Ex: ng new angularTest

Flag: --directory="directory path" 
Allows you to define a directory to put your Angular files in.
Ex: ng new angularTest --directory=./AngularTest



* ng lint "application-name"
Lints the TypeScript code in your application to make sure that it is production ready.
Ex: ng lint angularTest

Flag: --format stylish
Makes the output of the lint process much more visually appealing.
Ex: ng lint angulartest --format stylish

Flag: --fix
Will try to automatically fix any changes that it catches.
Ex: ng lint angularTest --fix



* npm install webpack-bundle-analyzer --save-dev
Installs a dev dependency that allows developers to see the size of the files in the "dist" folder.
NOTE: --save-dev prevents this from going into the production code.

Also, a stats.json file needs to exist in the "dist" folder for this to work.
To generate one, run the following command:
ng build --stats-json

You can place this in your "package.json" file under the "scripts" key to run the webpack with "npm stats":
("stats": "npx webpack-bundle-analyzer dist/"Application name"/stats.json",)



* ng add @angular/material
Configures Angular Material, a set of UI components, to work with your project



* ng generate @angular/material:material-nav --name nav
This will generate a navigation-based Angular component for your Angular application with the name "nav".


* ng generate @angular/material:material-dashboard --name dashboard
This will generate a dashboard-based Angular component for your Angular application with the name "dashboard".


* ng generate @angular/material:material-table --name customer-list
This will generate a table-based Angular component for your Angular application with the name "customer-list".
NOTE: This will also generate a "data source" file to put in data from an external source (e.g. database, JSON file).




* ng test
Executes tests on all "*.spec.ts" files in the Angular application.
NOTE: The browser will open to show the successes/failures.

Flag: --code-coverage
Generates a "coverage" folder that shows you the results of the tests in its "index.html" file.
This file will show you what lines of code are being used in our tests (e.g. which part of an if/else statement it executed).



* ng update (package name)
Updates a dependecy(ies) within your "package.json" file.
NOTE: go to "https://update.angular.io" to see what you need to do before updating Angular from one version to another.
NOTE: By itself, "ng update" will scan your "package.json" file and tell you what can be updated.

Flag: -dryRun (or d)
Runs through the update without making any changes.

Flag: --all
Updates all of the packages in your "package.json" file.



## Angular Files: Base Folder

* angular.json: The Angular CLI's configuration file.
* editor.config: File used to config the IDE settings (like modifying the indent space size).
* .gitignore: Used by GIT to ignore certain files/folders so that they are not pushed to production.
* package.json: Shows all of the information about the dependencies and the scripts for the application.
* README.md: You're looking at it.
* tsconfig.json: The TypeScript configuration file.
* tslint.json: The file that lints (checks for readability, maintainability and functionality errors) TypeScript code.

## Angular Files: src folder
* index.html: The basic HTML file that will be served to the browser.
* main.ts: TypeScript file that kicks off Angular itself.
