Libsite-Header-Lite
===================

Simple HTML minimal/lite header and footer. Includes both a static html version and a Twitter Bootswatch version (Bootstrap 2.3).

Intended for use with GW Library tools like FindIt, Launchpad and SRRS and also vendor tools like Libguides that let you drop basic skinning via the admin UI.

The Bootstrap bootswatch includes Font Awesome (version 4.1)! http://fontawesome.io/get-started

Implementation
--------------

The code is heavily commented. Start by looking at the html framework for your intended version:

Bootswatch html: bootswatch.html (example: http://gwdev-zut.wrlc.org/libheader/Libsite-Header-Lite/bootswatch.html)

Static html: page.html (example: http://gwdev-zut.wrlc.org/libheader/Libsite-Header-Lite/page.html)

> **App Assets server**: all of the static files can be pulled directly from the App Assets server: http://gwappassets-prod.wrlc.org/app-assets/libheader/2_002/ (where 2_002 is the Libsite-Header-Lite version you want to pull). The file structure is the same:

> *Example: http://gwappassets-prod.wrlc.org/app-assets/libheader/2_002/css/libheader7_lite.css*

> The only local file you will need is the favicon file

Bootswatch Version
------------------

Include the following in your &lt;head&gt; &lt;/head&gt; :

```
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>GW Libraries Bootswatch</title><!-- your page title -->
        <meta name="viewport" content="width=device-width, initial-scale=1.0"><!-- important! -->
        <meta name="description" content=""><!-- optional -->
        <meta name="author" content=""><!-- optional -->
            
        <!-- styles -->
        <!-- these are the stylesheets: first one grabs the Bootstrap cdn stylesheet, the other two are for the Library theme -->
        <link href="http://netdna.bootstrapcdn.com/twitter-bootstrap/2.3.1/css/bootstrap-combined.min.css" rel="stylesheet" media="all">
        <!-- Font Awesome! http://fontawesome.io/get-started -->
        <link href="//netdna.bootstrapcdn.com/font-awesome/4.1.0/css/font-awesome.min.css" rel="stylesheet">
        <link href="//gwappassets-prod.wrlc.org/app-assets/libheader/2_002/css/libheader7_lite.css" rel="stylesheet" media="all">
        <link href="//gwappassets-prod.wrlc.org/app-assets/libheader/2_002/css/libheader7_lite_bootswatch.css" rel="stylesheet" media="all">
	    <!-- print styles are included in base libheader7_lite.css --> 
  
        <!-- js links are at the bottom of the page -->
            
        <!-- IE css mods and HTML5 shim, for IE6-8 support of HTML5 elements --><!-- important! -->
        <!--[if lt IE 9]>
        <link href="//gwappassets-prod.wrlc.org/app-assets/libheader/2_002/css/libheader7_lite_ie.css" rel="stylesheet">
        <script src="http://html5shiv.googlecode.com/svn/trunk/html5.js"></script>
        <![endif]-->
                                
        <!-- Fav and touch icons -->
        <link rel="shortcut icon" href="favicon.ico">
        <link rel="apple-touch-icon" href="img/apple-touch-icon-iphone.png"><!-- optional, and this is just the min version -->

        <!-- Google Analytics -->
        <!--
        <script>
        var _gaq = _gaq || [];
        _gaq.push(
        // site Analytics account
        ['_setAccount', 'UA-XXXXX-1'], 
        ['_trackPageview'],
        // aggregated Analytics account
        ['aggregate._setAccount', 'UA-XXXXX-2'],
        ['aggregate._trackPageview']
        );

        (function() {
        var ga = document.createElement('script'); ga.type = 'text/javascript'; ga.async = true;
        ga.src = ('https:' == document.location.protocol ? 'https://ssl' : 'http://www') + '.google-analytics.com/ga.js';
        var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(ga, s);
        })();
        </script>
        -->
        
    </head>

```

Then add the header to the &lt;body&gt; :

```
<header class="navbar-fixed-top"><!-- this is the Libsite7 Lite Header -->
    <div id="libheader-container">
        <div id="libheader" class="container">
            <div class="libheader-logo hide-lo"><a href="http://www.gwu.edu" target="_blank" title="GWU website"><img src="//gwappassets-prod.wrlc.org/app-assets/libheader/2_002/img/gwheaderlogo.png" alt="logo: The George Washington University" /></a></div>
            <div class="libheader-liblink"><a href="http://library.gwu.edu" target="_blank" title="GW Libraries website">GW Libraries</a></div>

            <!-- optional links can go here (note: use short text, test it doesn't bump into the GW logo) -->
            <div class="libheader-link"><a href="#" target="_blank" title="">Placeholder Link 1</a></div>
            <!-- this is an optional 'bullet' to place between links -->
            <div class="bullet">&bull;</div>
            <div class="libheader-link"><a href="#" target="_blank" title="">Placeholder Link 2</a></div>
            <!-- end optional links -->

            <!-- optional bootstrap user icons, example placement -->
            <div class="libheader-icon">
                <i class='icon-off icon-white'></i>&nbsp;<a href="/logout/">logout</a>
            </div>
            <div class="libheader-icon">
                <i class='icon-cog icon-white'></i>&nbsp;<a href="/change_password/">settings</a>
            </div>
            <div class="libheader-icon">
                <i class='icon-user icon-white'></i>&nbsp;guest
            </div>
            <!-- end optional bootstrap user icons -->
        </div>
    </div>
</header><!-- end Libsite7 Lite Header -->

```
And the footer:

```
<footer class="navbar-fixed-bottom"><!-- the Libsite7 Lite Footer -->
    <div id="libfooter-container">
        <div id="libfooter" class="container">
            <div class="libfooter-text">
                <div id="footer-contact">
                    <span class="address"><a href="http://library.gwu.edu" target="_blank" title="GW Libraries Website">GW Libraries</a> &#8226; 2130 H Street NW &#8226; Washington DC 20052</span> &#8226; <span class="tel">202.994.6558</span> &#8226; <a href="mailto:gelman@gwu.edu" target="_blank" title="">gelman@gwu.edu</a>
                </div>
                <div id="footer-utility">
                    <span><a href="#">Utility Link 1</a></span>
                    <span> &#8226; </span>
                    <span><a href="#">Utility Link 2</a></span>
                    <span> &#8226; </span>
                    <span><a href="#">Utility Link 3</a></span>
                </div>
            </div>
        </div>
    </div>
</footer><!-- end Libsite7 Lite Footer -->
```

Include js call at the bottom (for faster page load) or add this into the &lt;head&gt; :

```
<!-- javascript placed at the end of the document so the pages load faster -->
<script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.3/jquery.min.js"></script> 
<script src="http://netdna.bootstrapcdn.com/twitter-bootstrap/2.3.1/js/bootstrap.min.js"></script><!-- important :) -->

```
