#imgPin <a href='#/master/CHANGELOG.md' class='version' title='Whats New?'>v1.0</a>

###Use jquery to add pin this buttons to images on your site

imgPin lets you automatically add "pin this" buttons over images on your website.  Features include:
* - Button revealed on rollover
* - Ability to add custom pin images
* - Different placement options for button
* - Automatically opens in new window, centered and sized


## Installation
Make sure you have [jQuery](http://jquery.com/) included.  To use imgPin in your project simply include the plugin js file and the plugin CSS file.  You may change the CSS rules in any way you like, including customizing hover effects and default positioning - but keep in mind that wrapper DIVs are added around each image - so if you are absolutely positioning your image tags, you will run into problems.

```html
<script type="text/javascript" src="jquery.imgPin.js"></script>
<link type="text/css" rel="stylesheet" href="imgPin.default.css"></script>
```

For deployment use the minified version __instead__:
```html
<script type="text/javascript" src="js/jquery.imgPin.min.js"></script>
```

##Usage
imgPin can be used on any images throughout your site. Use jQuery selectors to choose the images.  Basic Example below:

The HTML:

```html
<div class="images">
  <img src="http://www-static.weddingbee.com/pics/36694/head.jpeg">
  <img src="http://i.kinja-img.com/gawker-media/image/upload/s--ayBAkvRS--/19717ffsen23sjpg.jpg">
  <img src="http://images2.fanpop.com/images/photos/6000000/Random-random-6054526-1280-1024.jpg">
</div>
```

The jQuery:

```html
$('.images img').imgPin();
```

By default the plugin uses the simple "pinit" button from Pinterest.  You can use any image you want with the following:

```html
$('.images img').imgPin({pinImg: 'CUSTOM_IMG_URL'});
```

The other option available is placement of the pinit botton, using values 1-5.

* 1 = top left
* 2 = top right
* 3 = bottom right
* 4 = bottom left
* 5 = center

Example:

```html
$('.images img').imgPin({pinImg: 'CUSTOM_IMG_URL', position: 3});
```

###Note
* Keep in mind that wrapper DIVs are added around each image - so if you are absolutely positioning your image tags, you will run into problems.

##To-Do
* Browser testing
* Responsive testing

I'm open to changes in how this functions - love feedback and suggestions.


##Acknowledgements
* Thank you to [ScrollMagic](https://github.com/janpaepke/ScrollMagic/blob/master/README.md) for use of your lovely README Formatting, and to Modcloth for the use-case.
