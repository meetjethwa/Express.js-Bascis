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
  
