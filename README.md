# Make a webpage

Lets make a webpage for next year's Art Burst (or whatever you want but you need to use your imagination). The page must introduce the
event, show the schedule and the location and provide contact information.

## 1. Create a HTML file

Open Sublime and open a new text file.

Create the skeleton of the new document including the opening tag <html>, the “head” section, the “title”, and the “body” section.  At the end make sure you have a closing tag </html>.   Use opening and closing tags for head, title, and body.  Notice that title is in inside the “head” section.

````
<!DOCTYPE html>
<html>
  <head>
    <title>Art Burst 2018</title>
  </head>
  <body>
    <h1>Art Burst 2018  </h1>
    <p>This is some text for my webpage.</p>
  </body>
</html>
````

Save your file as “index.html”.  You have created an HTML file.  HTML files
contain all the code for a website.


## 2. Open the HTML file in a browser 

In Firefox or Chrome (or another browser) open the index.html file via the menu __File > Open (File)__.  The website’s title will appear in your browser but there is no content in your website yet except the title “Art Burst 2018” and a bit of text.

## 3. Create a document structure 

In the “body” section of your HTML file we will add headings for the three sections of the web page:

* About
* Schedule
* Location
* Contact

Write:

````<h2>About</h2>````

Then repeat this for the other two headings (Schedule, etc.)

Go to the browser and reload the web page to see the result.

##4. Add content to the sections

In the __About__ section we will put text from wikipedia using “paragraph” tags <p> and </p>.

Place one paragraph of text from wikipedia between <p> and </p>.  Repeat for each paragraph.

If you want to leave blank lines between paragraphs use the “break” tag.  You simply type </br>.

If you have no content you can [use dummy text](http://www.lipsum.com/feed/html) and replace it later.

Go to the browser and reload the web page to see the result.

##5. Add a link to the ISU website

Let’s create a link to the ISU website: ``http://isu.nl``

Links in HTML are created using the ``<a></a>`` tags and the ``href=`` attribute.  It’s like this:
<a href=”http://isu.nl”>International school Utrecht</a>

Add this to the file and test the link to see if it works.

Go to the browser and reload the web page to see the result.

##6. Add images

Find some images for your website. For example via [Google](https://www.google.nl/search?q=school+performance+dance+music).

Go to the __About__ section and __Location__ section in your HTML code and add some images using the ``<img>`` tags.  If your image is named photo1.jpg then add an image by typing ``<img src=”photo1.jpg”>``

Go to the browser and reload the web page to see the result.

##7. Add a video
 
Find a video on YouTube for your web page.  Select a video and right click on it.  You can then copy the “embed code” for the video. It looks like this: 

````
<iframe width="854" height="480" src="https://www.youtube.com/embed/bRT9duhV0ME" frameborder="0" allowfullscreen></iframe>
````

Go to the __About__ section in your HTML code and paste in the embed code where you like.

Go to the browser and reload the web page to see the result.

##8. Style your web page

To change the color and alignment of images and text in your website you must add special code into your HTML file.  This code is called CSS.

Open Sublime and open a new text file. Add a little bit of CSS code:

````

body {
  border-color: orange;
  border-width: 10px;
  border-style: double;
  padding: 10px;
  margin: 10px;
}
````

Save your file as __style.css__. Add the following line between the ``<head>
`` and ``</head>`` tags in the HTML file.

````
    <link href="style.css" rel="stylesheet" />
````
Go to the browser and reload the web page to see the result.

## Credits
This workshop was copied from Coderdojo belgium:
https://drive.google.com/drive/folders/0B1Mkb-21rOtlUHp3ZFJ2bHVsVkk?tid=0BxJHvnjGv9_gQk9SLXR3S003Q00

## Resources for further learning
* https://coderdojo.com/resources/
* https://www.codecademy.com
* https://www.freecodecamp.com/challenges/say-hello-to-html-elements

