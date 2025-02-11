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

- now move into src folder and create directories: "mkdir controllers db middlewares models routes utils"

-lets talk about some folder structure 
- controller/controllers you can choose name according to you both are fine. in this folder we write our majourly functionality
- inside db folder we write the how to connect the database, most of the time database connection logic should be written here, any database mongoDB/postgreSQL it's your choice.
- inside the middlewere we write that code that i want to run inbetween, a request comes, before server fulfilled it you want any checking any functionality that should be written in middleware eg. apke pas ik request aayi, aap server se kuch information puch rahe ho,mai ik middleware laga dunga ki ap apni cokkies hme do jis se mai pata karu ki phle ap us information ko lene ke yogya ho ya nhi ho. these such works done by middleware. middleware can be many types.
- inside the model folder  we describe our models
- inside the routes folder we write the routes so that they can be easily handled.
-inside the utils folder we write the utility basic functionality could be used many places in the project we keep it as utility eg. file upload utility,mailing utility,token.
-like nodemon we have another plugin "prettier" it also present in the "VSCODE" but in proffesional grade code many people work on same project so it need better code formating so can avoid the conflicts. it is also "devdependency" so other than vs code we need to add it as per project basis and these setting also.  to install: "npm i -D prettier" after installing we need to add some settings manualy in the code. in root folder need to create a file with name ".prettierrc" in this file we specified the settings that we want to apply in the project. and one another file should be made in root folder that is ".prettierignore" in this file we species the setting that should not change by the prettier.