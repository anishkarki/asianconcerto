# asianconcerto
watch the index.pug and see the path of css and js files.


1. convert all the htmls into pug and add them into the views folder.
(index.pug is home page. Don't make new home only paste the code into index.pug so that the routes will work properly.)
(give any name to other pages.)

2. check the path of the css and js file.



3. Go to routes folder. Don't change the link for index.
Same as here. add::

router.get('/pagename', function(req, res){
  res.render('pagename', {
    title: 'newtitle'
  });
});

for each page created

This creates a new page in link localhost:/pagename

