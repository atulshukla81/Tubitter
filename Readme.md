# Tubitter backend

This is Tubitter Backend with Javascript

-[Model Link](./Model%20design/diagram.png)

- .gitkeep file is helps empty folder in git tracking so that they also can  be pushed beacause empty folder not be tracked and push.


 - in market alot of .gitignore genrators present in the market here that helps in genrating gitignore files according to the project in standard way you can also customize it. i am using "https://mrkandreev.name/snippets/gitignore-generator/" this one.

 - .env file, this file is enviornment variable file, when we push the things into production then these enviornment variable pickedup from system  not the files because they can secure. when we push .env in git, git also gives warning so only for showcasing i am writing another .env file with name .env.sample

 - we have created an folder with name of src in root folder it totally depend on you if you want keep all the directory files in root folder or in the src folder for better code radability and  better code organization i am using src folder.

 - now time to some work on package.json file  and write some scripts  how to open and run this project.  for this project i am using import  syntax not reqire syntax. in java theire are two ways of importing one is common js and other one is module js , foe this project i am using module js because we can maitain consistency.  so we added "type": "module".
 - for the autorestarting of the server after the every changes on the code we are using nodemon  as devdependency. to install it "npm i -D nodemon" . after installing it node modules folder  and package-lock.json file added to the root dirctory of the project. 
 - when install the nodemon then a block of line should be added automatically in the package.json file but in my project it not added automatically so after the verifying the installation manually added :  "devDependencies": {
    "nodemon":"^3.1.9"
  }
  and under the scipts in package.json added:  "dev":"nodemon src/index.js" 
  - .env file and "type":"module" in package.json have some issue,because we can't import it so it can be require only so need to resolve them  so for resolve it later stage but for now i am : 

