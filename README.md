# Express.js-Bascis


------Hello World and Server Starting
  Code :
      const express = require('express');
      const app = express();
      app.get('/', (req, res) => {
          res.send('Hello World');
      });
      app.listen(3000, () => {
          console.log('Server started');
      });
        
  Output :
          <img width="1126" height="64" alt="image" src="https://github.com/user-attachments/assets/e2939d80-7ae8-4792-9140-6ae6b9a07292" />
          <img width="736" height="241" alt="image" src="https://github.com/user-attachments/assets/01cb3527-3fe7-4176-ab17-c81d02ada8c8" />


------Login Authentication by js and html 
  Code :
    login.js
          import express from 'express';
          import path from 'path';
          import { fileURLToPath } from 'url';
          const app = express();
          const __filename = fileURLToPath(import.meta.url);
          const __dirname = path.dirname(__filename);
          app.use(express.urlencoded({ extended: true }));
          app.get('/', (req, res) => {
            res.sendFile(path.join(__dirname, 'folder', 'login.html'));
          });
          app.post('/login', (req, res) => {
            const { username, password } = req.body;
            if (username === 'admin' && password === '1234') {
              res.send('Login Successful ✅');
            } else {
              res.send('Login Failed ❌');
            }
          });
          app.listen(5000, () => {
            console.log('Server running on http://localhost:5000');
          });

  Login.html
        <!DOCTYPE html>
        <html>
        <head>
            <title>Login</title>
        </head>    
        <body>
            <h2>Login Page</h2>
            <form action="/login" method="post">
                <label>Username:</label>
                <input type="text" name="username" required>
                <br><br>
                <label>Password:</label>
                <input type="password " name="password" required>
                <br><br>
                <button type="submit">Login</button>
            </form>
        </body>
        </html>


        
  Output :
            <img width="1765" height="234" alt="image" src="https://github.com/user-attachments/assets/847f6fd3-1000-4a98-83c8-823d6a89ef44" />
            <img width="892" height="500" alt="image" src="https://github.com/user-attachments/assets/11c34137-618b-4ed9-9533-70ce486e0249" />

------Server Creation on js 
        const express = require('express');
        const path = require('path');
        const app = express();
        app.use(express.static(path.join(__dirname, 'static')));
        app.get('/',(req, res) =>{
            res.sendFile(path.join(__dirname,'static','index.html'));
        });
        app.get('/about',(req, res) =>{
            res.sendFile(path.join(__dirname, 'static','about.html'));
       });
       app.get('/contact',(req, res) =>{
            res.sendFile(path.join(__dirname,'static','contact.html'));
       });
       app.listen(8080, () =>{
            console.log('Server running at http://localhost:8080');
       });
  

 Output :
       <img width="1171" height="105" alt="image" src="https://github.com/user-attachments/assets/3dc36250-ba54-455b-9c92-4ebf25d4708f" />
       <img width="1366" height="375" alt="image" src="https://github.com/user-attachments/assets/f9203783-848e-4761-9879-d56c045de996" />


  
          
