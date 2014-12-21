# Steps for creating app

1. new folder
2. express -c compass (new express with sass CSS) (for this to work you need to have installed the express generator with `npm install -g express-generator). Keep in mind that you'll need to have ruby installed and you will need to install compass itself.
http://dl.bintray.com/oneclick/rubyinstaller/
rubyinstaller-2.1.5.exe?direct
I had some trouble with SSL issues and followed the luislavena thing below and it worked.
http://stackoverflow.com/questions/19150017/ssl-error-when-installing-rubygems-unable-to-pull-data-from-https-rubygems-o/
https://gist.github.com/luislavena/f064211759ee0f806c88
http://compass-style.org/install/
3. npm install
4. NOT WORKING: new server folder and put bin, routes, views and app.js
5. NOT WORKING: change line in app.js to app.use(express.static(path.join(__dirname, '../public')));
6. git init
7. Add .gitignore through sublime
8. Create .bowerrrc with 
{
    "directory": "public/bower_components"
}

9. bower init (accept defaults)
10. bower install bootstrap --save
<s>11. I added a public/index.html</s>
12. I changed the arrangement of hte routes/index.js following this link:
<s>http://cwbuecheler.com/web/tutorials/2014/restful-web-app-node-express-mongodb/</s>

13. You should be able to start the server with `nodemon` or `npm start`. Note that I believe the starting directory for the server is driven by the 'start' in the `package.json` file. nodemon will 'know' where to start by reading the package.json but you could also type `nodemon bin/www`. Actually, I added 

`"start": "nodemon ./bin/www"` to package.json and now I can do npm start

14. Keep in mind the that the render will put an index.html in your public folder. So if there is already an index.html file then it will use this (at least it appears so).

15. I took some jade templates from https://github.com/primaryobjects/Node.js-Bootstrap-Starter-Template/tree/master/views and then the sticky footer from view-source:http://getbootstrap.com/examples/sticky-footer-navbar/

16. Type npm install pg --save
17. I ended up having to comment out the favicon require and the line about the favicon for the moment.

18. git remote add origin https://github.com/zross/expresspostgres.git
git push -u origin master


