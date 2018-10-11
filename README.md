# asianconcerto
watch the index.pug and see the path of css and js files.


1. convert all the htmls into pug and add them into the views folder.
(index.pug is home page. Don't make new home only paste the code into index.pug so that the routes will work properly.)
(give any name to other pages.)

2. check the path of the css and js file.



3. Go to routes folder. Don't change the link for index.   GO TO INDEX.JS
Same as here. add::

router.get('/pagename', function(req, res){
  res.render('pagename', {
    title: 'newtitle'
  });
});

for each page created

This creates a new page in link localhost:/pagename

4. Check the href in the pages. The logo image isnot clickable yet. That will redirect to other page.


No need for changes in app.js as we are adding all the page hrfs in index.js in Routes.



Ma beluka baki milauxu.

sample index.js:


var express = require('express');
var router  = express.Router();

router.get('/', function(req, res) {                                                                                                     
    res.render('index', { title: 'Home' });                                                                                             
});                                                                                                                                     
# Opens the index.pug in localhost:/.

router.post('/about', function(req, res){                                                                                          res.render('about', { title: 'About' });                                                                                                             
});                                                                                                                                      
# opens about.pug in localhost/about


module.exports = router;

Check the link:
https://stackoverflow.com/questions/24458208/nodejs-expressjs-what-is-routes-index-js-and-its-purpose
