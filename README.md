silent_watcher
==============

Readme :D
--------------
Every once in a while we need to learn a bit about someone. 
Simply clone this and run it on a server (like Heroku), and you can get the public information of anyone who goes to the page, just from them clicking the link :D

This simple nodejs project will log all of the users who visit the URL it is uploaded and save their public information, such as IP Address, Location (as precise as public can get), and more! All you have to do is go to {your_site}/database to view the data of people who have visited. 

Index.html is customizable. Make it look like whatever you want. You can make it look like a completely different site if you'd like! It logs all of the information as soon as the user connects. 

It is based off of node-js-sample.

Highlights:
+	Silently logs all users who enter site
+	Records Date/Time entered, Timezone, IP Address, Latitude, Longitude, Continent, City, ZIP Code, Language, Device Specs, Screen Height, and Screen Width
+	Viewable Database to see logs via ./database


Requirements
--------------
Make sure you have:
+	Node.js
+	NPM

Running Locally
--------------
Make sure you have node.js installed
```javascript
git clone git@github.com:heroku/node-js-sample.git # or clone your own fork
cd node-js-sample
npm install
npm start
```

To Upload to Heroku
------------------
If you want to make your own instance of this on your own url, here's a quick guide on how to upload it:

Requirements:
+	Heroku Command Line Tools

```javascript
heroku create
git push heroku master
heroku open
```

What if I Don't Want People to be Able to Access the Data via /database?
------------------
Just remove these lines and you can just access it via heroku command line (or whatever other host you use)

```javascript
app.get('/database', function(request, response) {
  response.sendFile(path.join(__dirname+'/database.html'));
})
```
