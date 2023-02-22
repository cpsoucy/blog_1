# How to create a bash script that provides boilerplate code

To start, the file itself has to be recognized as a bash script. To achieve this, you need the top of the file to contain the following:

`#!/bin/bash`

This will make the file a **bash** file.

After that, you want to create all the directories (folders) you need, like so:

`mkdir new-project`  
`cd new-project`  
`mkdir images scripts styles site`  
`cd site` 
`mkdir pages posts comments`  
`cd ..`  

The "`cd ..`" at the end navigates you back to the starting directory automatically, so you don't have to do it manually.

Next, use the **touch** command to create the two files you will need:  
`touch index.html`
`touch styles/style.css`  

After this, you can use the **echo** command to run the *index.html* & *style.css* from within the bash script:

`echo '<!DOCTYPE html>' > index.html`  
`echo '<html>' >> index.html`  
`echo '<head>' >> index.html`  
`echo '  <meta charset="utf-8">' >> index.html`  
`echo '  <meta name="viewport" content="width=device-width, initial-scale=1.0">' >> index.html`  
`echo '  <link rel="stylesheet" href="styles/style.css" media="screen" type="text/css">' >> index.html`  
`echo '</head>' >> index.html`  
`echo '<body>' >> index.html`  
`echo '   <h1>If this is red, CSS is working.</h1>' >> index.html`  
`echo '   <h2 id="blue_heading" onclick="changeHeadingColor()">If this is blue after clicked, JavaScript is working.</h2>' >> index.html`  
`echo '   <script> >> index.html`  
`echo '     function changeHeadingColor() {' >> index.html`  
`echo '       var heading = document.getElementById("blue_heading");' >> index.html`  
`echo '       heading.style.color = "blue";' >> index.html`  
`echo '     }' >> index.html`  
`echo '   </script>' >> index.html`  
`echo '</body>' >> index.html`  
`echo '</html>' >> index.html`  

This is the main portion of code, which includes not just HTML, but also embedded javascript to test JS functionality.

Finally, the bash script will load the CSS stylesheet like so:  
`echo 'h1 { color: red; }' > styles/style.css`

To test the functionality of this script, you can use a command like this one to open the file in a browser. Keep in mind that the file path has to be correct:  
`xdg-open C:/Users/cpsou/OneDrive/Documents/GitHub/blog_1/new-project/site/index.html`
