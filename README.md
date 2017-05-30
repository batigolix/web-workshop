# Make a webpage

Lets make a webpage for next year's Art Burst (or whatever you want but you need to use your imagination). The page must introduce the
event, show the schedule and the location and provide contact information.
 
## 1. Create a web page

Open Sublime and open a new text file.

Create the skeleton of the new document including the opening tag `<html>`, the __head__ section, the __title__, and the __body__ section.  At the end make sure you have a closing tag `</html>`. Use opening and closing tags for head, title, and body.  Notice that title is in inside the __head__ section.

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
contain all the content (text, images, videos etc.) and the structure for a website. HTML stands for __Hypertext markup language__.

## 2. Open the HTML file in a browser 

In Firefox or Chrome (or another browser) open the index.html file via the menu __File > Open (File)__.  The website’s title will appear in your browser but there is no content in your website yet except the title __Art Burst 2018__ and a bit of text.

## 3. Create a document structure 

In the “body” section of your HTML file, using the `<h2>` tag we will add headings for the three sections of the web page:

* About
* Schedule
* Location
* Contact

Also include a `id` attribute that we need later on for the menu.

Write:

````<h2 id="about">About</h2>````

Then repeat this for the other two headings (schedule, etc.).

Go to the browser and reload the web page to see the result.

## 4. Add content to the sections

In the __About__ section we will put text from wikipedia using “paragraph” tags `<p>` and `</p>`.

Place one paragraph of text from wikipedia between `<p>` and `</p>`. Repeat for each paragraph.

If you want to leave blank lines between paragraphs use the __break__ tag.  You simply type `</br>`.

If you have no content you can [use dummy text](http://www.lipsum.com/feed/html) and replace it later.

Go to the browser and reload the web page to see the result.

## 5. Add a link. 

Let’s create a link to the ISU website: __http://isu.nl__

Links in HTML are created using the `<a></a>` tags and the `href=` attribute.  It’s like this:
`<a href="http://isu.nl">`International school Utrecht`</a>`.

Add this to the file and test the link to see if it works.

Go to the browser and test the link to see how it works.

Add a menu to the top of the document:

<ul>
    <li>Home</li>
    <li class="c-nav__item"><a class="c-link" href="#news">News</a></li>
    <li class="c-nav__item c-nav__item--right">Contact</li>
</ul>

## 6. Add a menu.

Add a menu so that visitors can easily navigate to the four sections.

First let’s create a list of the different sections of your website using the list tags `<ul></ul>` and `<li></li>`.

At the top of your website (after the `<body>` tag) add the following list of links:

````
<ul>
  <li><a href="#about">About</a></li>
  <li><a href="#schedule">Schedule</a></li>
  <li><a href="#location">Location</a></li>
  <li><a href="#contact">Contact</a></li>
</ul>
````
 
## 7. Add images

Find some images for your website. For example via [Google](https://www.google.nl/search?q=school+performance+dance+music). Or [Lorem pixel](http://lorempixel.com/) for dummy images.

Go to the __About__ section and __Location__ section in your HTML code and add some images using the ``<img>`` tags.  If your image is named photo1.jpg then add an image by typing ``<img src=”photo1.jpg”>``

Go to the browser and reload the web page to see the result.

## 8. Add a video
 
Find a video on YouTube for your web page.  Select a video and right click on it.  You can then copy the “embed code” for the video. It looks like this: 

````
<iframe width="854" height="480" src="https://www.youtube.com/embed/bRT9duhV0ME" frameborder="0" allowfullscreen></iframe>
````

Go to the __About__ section in your HTML code and paste in the embed code where you like.

Go to the browser and reload the web page to see the result.

## 9. Style your web page

To change the styling such as color, fonts and alignment of images and text in your website you must add styling code into your HTML file.  This code is called CSS (cascading style sheet).

Open Sublime and open a new text file. Add a little bit of CSS code:

````
body {
    border-color: orange;
    border-width: 10px;
    border-style: double;
    padding: 10px;
    margin: 10px;
    background: url(http://boris.doesb.org/img/notebook.png);
    background-color: white;
}

img {
    border-color: RebeccaPurple;
    border-width: 4px;
    border-style: solid;
    margin: 10px;
    width: 250px;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}

ul {
    list-style-type: square;
}

h1, h2, h3 {
    color: RebeccaPurple;
}

````

Save your file as __style.css__. Add the following line between the `<head>
` and `</head>` tags in the HTML file.

````
    <link href="style.css" rel="stylesheet" />
````
Go to the browser and reload the web page to see the result.

## 10. Use classes

To apply specific CSS you must use classes in the HTML code. Add the class __location__ to the `<h2>` heading __Location__.

It should look as follows:

````
<h2 class="location">Location</h2>

````

Now add the following snippet to the CSS file. 

````
.location {
    font-size: 150%;
    background: DarkOrange;
    color: Black;
    padding: 8px;
}
````

Go to the browser and reload the web page to see the result.

## 11. Use a framework

Web developers are lazy people that do not like repeating jobs. So they bundle re-usable code in packages that are available on the internet. Such packages are called frameworks.

Include a framework by adding the following line between the `<head>
` and `</head>` tags in the HTML file.

````
<link rel="stylesheet" href="https://unpkg.com/blaze">
````

Add the class `c-text`  to the `<body>` tag.
Add the class `c-heading`  to the `<h2>` tags.

Replace the navigation from step 6 with:

````
<ul class="c-nav c-nav--inline">
  <li class="c-nav__item"><a class="c-link" href="#about">About</a></li>
  <li class="c-nav__item"><a class="c-link" href="#schedule">Schedule</a></li>
  <li class="c-nav__item"><a class="c-link" href="#location">Location</a></li>
  <li class="c-nav__item c-nav__item--right"><a class="c-link" href="#contact">Contact</a></li>
</ul>
````
By using these additional classes you apply the styling of the framework.

Go to the browser and reload the web page to see the result.


## Credits
This workshop was copied from Coderdojo belgium:
https://drive.google.com/drive/folders/0B1Mkb-21rOtlUHp3ZFJ2bHVsVkk?tid=0BxJHvnjGv9_gQk9SLXR3S003Q00

## Resources for further learning
* https://coderdojo.com/resources/
* https://www.codecademy.com
* https://www.freecodecamp.com/challenges/say-hello-to-html-elements

