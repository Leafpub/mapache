# Mapache for [Leafpub](https://github.com/Leafpub/leafpub/) by GodoFredo ported by Marc

> Minimalist Material Design and Elegant theme for [Leafpub](https://github.com/Leafpub/leafpub/).

### Free theme for Leafpub

Forked from [Mapache](https://github.com/godofredoninja/Mapache) and ported for Leafpub.

![](./documentation/mapache-screenshot.png)


## Mapache Support for Web Browsers
Mapache supports the following web [browsers](http://caniuse.com/#search=flexbox)

## Featured
- Responsive layout
- Blog navigation
- Page 404
- Cover images for blog, tag and author
- links to followers in social media
- Related Articles (6 articles)
- Video Post Format
- Image post Format
- 5 articles featured in the home of the page section sidebar
- 5 articles latest posts in the (author - tag - post) section sidebar
- Support for comments (Facebook or Disqus)
- Support for counter comments (Facebook or Disqus)
- Buttons to share the article
- Counter shared articles on Facebook
- YouTube, Vimeo, kickstarter -> Video Responsive
- Reading progress indicator

### Replace Favorite icon
Create an image icon with these dimensions with the name icon.png `155px * 155px` in ` Copy your new favorite icon to ./assets/img/icon.png`


## Mapache settings

- Copy the below script to Settings -> Advanced -> Leafpub Footer section.

### Social Links
Add the Social Links only for the services you want to appear in the header section of your website. Pay attention as enabling too many services will cause menu problems.

### Title 
This section will display the desired title name in the browser tab

### YouTube Subscribe Button
This section enables the YouTube Post format. Add the Channel Name and Channel ID which can be found here [YouTube Advanced Settings](https://www.youtube.com/account_advanced)

``` html
<script>
/* links to followers in social media */
var followSocialMedia = {
	'google': 'https://...',
	'youtube': 'https://...',
	'instagram': 'https://...',
	'snapchat': 'https://...',
	'dribbble': 'https://...',
	'github': 'https://...',
	'linkedin':'https://...',
	'spotify':'https://...',
	'codepen':'https://...',
	'behance':'https://...',
	'flickr':'https://...',
	'pinterest':'https://...',
	'feed':'https://...',
}

/* Title for home Page */
var title_home = '... your title ...';

/*Youtube button subscribe for post video format*/
var youtube = {'YOUR_CHANNEL_NAME':'YOUR_CHANNEL_ID'}

/*Disqus for Comments*/
var disqusShortname = 'YOUR_DISQUS_SHORTCUT_HERE';

/* enable reading indicator */
var enableReadingIndicator = true;
</script>

<!-- Disqus Comments Count-->
<script id="dsq-count-scr" src="//YOUR_DISQUS_SHORTCUT_HERE.disqus.com/count.js" async></script>

```
## Enable Disqus or Facebook Comments
This seciton will cover how to cover Disqus of Facebook commenting into the theme. Only enable either Disqus or Facebook comments.

### Disqus Comments
To enable Disqus comments update the code in Settings -> Advanced -> Leafpub Footer.

Insert your [Disqus shortname](https://shortname.disqus.com/admin/) in both the comments and Disqus comment count sections.

To ensure the Disqus comment count is working correctly verify that the Disqus settings -> Comment & Community Configuration is set as seen below.
![](./documentation/disqus_comment_count.png)

### Facebook Comments
To use facebook comments, skip the configuration Disqus.

This enables comments and comment counter

1. Add the code in Settings -> Advanced -> Leafpub Header

```html
<style>
	.mapache-disqus{
		display: none !important;
	}
	.mapache-facebook{
		display: inline !important;
	}
</style>
```
2. Add the code Settings -> Advanced -> Leafpub Footer

```html
	<div id="fb-root"></div>
	<script>
	(function(d, s, id) {
	  var js, fjs = d.getElementsByTagName(s)[0];
	  if (d.getElementById(id)) return;
	  js = d.createElement(s); js.id = id;
	  js.src = "//connect.facebook.net/en_US/sdk.js#xfbml=1&version=v2.6";
	  fjs.parentNode.insertBefore(js, fjs);
	}(document, 'script', 'facebook-jssdk'));
	</script>
```

![](./documentation/code-footer.png)


## Change Theme Style
To change the color of the Mapache theme select one of the theme styles below and copy it into the Setting -> Advanced -> Leafpub Header

```html
<!-- Theme indigo -->
<link rel="stylesheet" href="/assets/css/themes/indigo.css"/>
<!-- Theme dark blue -->
<link rel="stylesheet" href="/assets/css/themes/dark-blue.css"/>
<!-- Theme blue semi dark -->
<link rel="stylesheet" href="/assets/css/themes/blue-semi-dark.css"/>
<!-- Theme blue -->
<link rel="stylesheet" href="/assets/css/themes/blue.css"/>
<!-- Theme Grey -->
<link rel="stylesheet" href="/assets/css/themes/grey.css"/>
<!-- Theme dark cyan -->
<link rel="stylesheet" href="/assets/css/themes/dark-cyan.css"/>
<!-- Theme purple -->
<link rel="stylesheet" href="/assets/css/themes/purple.css"/>
<!-- Theme teal -->
<link rel="stylesheet" href="/assets/css/themes/teal.css"/>
<!-- Theme Green -->
<link rel="stylesheet" href="/assets/css/themes/green.css"/>

<!-- For theme white add two-color logo 230px * 130px -->

<!--
	***** 230px *****
	*				*
	***************** 130px
	*				*
	*****************
-->


<link rel="stylesheet" href="/assets/css/themes/white.css"/>

```

![](./documentation/img-four.png)


### Edit Sidebar
Add you own custom content into the side bar by editing the `./partials/sidebar.hbs` file.

```html

<div class="sidebar-items">
	<div class="sidebar-title">...your title...</div>
	... your content ...
</div>

<!-- Add your content here - block fixed -->
<div class="sidebar-items">
	<div class="fixed">
		... your content fixed ...
	</div>
</div>

```


### Buttons
Format your hyperlinks with some really cool buttons. Check out the different button options here. Add these buttons directly into your blog posts.

```html
... <a class="external" href="http://..." >Your link external</a> ...

<a class="btn external" href="http://..." >link external</a>

<a class="btn btn-download" href="http://..." >download</a>

<a class="btn btn-download-cloud" href="http://..." >download</a>
```
![](./documentation/buttons.png)


### Warning - Note - Success
Add some more styling options to your articles text with these three styles. 

```html
<p class="warning"> ... your text warning ... </p>

<p class="note"> ... your text note ... </p>

<p class="success"> ... your text success ... </p>
```
![](./documentation/note.png)


## Video Post Format
If you want to have a video post format, you only have to add the tag `video-post-format` . The first video in the article will be large in size.

![](./documentation/video.png)

## Image Post Format
If you want to have a image post format, you only have to add the tag `image-post-format` The Featured image will become large in size


### Credits
- [Normalize](https://necolas.github.io/normalize.css/)

## Copyright & License

Copyright (c) 2016 GodoFredo - Released under the [MIT license](LICENSE).
