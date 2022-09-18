# Firebase Contact Form

Mobile first, responsive contact from that sends data to a firebase database

## create a account on [https://firebase.google.com](https://firebase.google.com)
1. add project
2. get started by adding firebase to your app, choose </>web
3. register app
4. add firebase SDK
    1. ```<script src="https://www.gstatic.com/firebasejs/4.3.0/firebase.js"></script>``` right above ```<script src="main.js"></script>```
    2. add following config on the top of main.js, 
   ```
   var config = {
    apiKey: 'xxx',
    authDomain: 'xxx',
    projectId: 'xxx',
    databaseURL: 'xxx', // database url finds in Realtime Database interface
    storageBucket: 'xxx',
    messagingSenderId: 'xxx',
    appId: 'xxx',
    };
    firebase.initializeApp(config);
    ```
5. set up database，start in test mode, if you choose locked mode, you will need to set the .read and .write to true for read and write data\
   ![database-setup](./screenshoot/firebase-database-setup.jpg 'database-setup')
  
### module 
to gitignore firebase credentials, create a config.js file, then import config.js in main.js, add config.js to .gitignore, then make a 
config.example for illustrating variables 
if get 'Cannot use import statement outside a module' error 
add to script in main.js
```
type='module'
```
