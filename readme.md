# Natours Landing Page

A landing page from Jonas Schmedtmann's Advanced CSS Course on Udemy

This app was built using pure CSS, including many modern and up to date features. The layout is fully responsive for multiple screen widths. This is my first project using Sass, which is a great extension of CSS that adds power and elegence to the language. I decided to refactor the original code by adding additional variables, mixins etc. This has made the code more maintainable not only for this project, but also re-usable for future Sass projects. 

The app is deployed and available to use via the link below - 

https://pure-lowlands-81406.herokuapp.com/

I created a simple Express server so that this app can be deployed to Heroku. server.js is simply telling Heroku to use index.html

```
const express = require('express');
const path = require('path');
const port = process.env.PORT || 8080;
const app = express();


app.use(express.static(__dirname));

// If user makes a get request to any address, run this function. 
app.get('*', (req, res) => {
    res.sendFile(path.resolve(__dirname, 'index.html'));
});

app.listen(port);

console.log('server started');
```

