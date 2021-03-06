# Galaxy

![screenshot](https://s1.gifyu.com/images/Screenshot-1205.png)
morning, between 0h and 11h

![screenshot](https://s1.gifyu.com/images/Screenshot-1206.png)
afternoon, between 12h and 17h

![screenshot](https://s1.gifyu.com/images/Screenshot-1204.png)
evening, between 18h and 23h

[Live Demo](https://catgrills.github.io/Galaxy/) of <i>Galaxy</i>.

About
-------------------------------

<i>Galaxy</i> is a startpage featuring a sidebar with three boxes of link, and has  a different background depending of the hour.

A startpage/homepage is a local website, namely you'll be able to access it thanks to files present on your computer (in general, it'll be a .htm file), and some browser like Firefox Mozilla and Google Chrome will allow you to set a custom homepage. What's more, thanks to some add-ons/extensions such as 'New Tab Homepage' for FF or 'New Tab Redirect' for Chrome, you'll be able to set this said startpage as you new tab page (amazing isn't it ?). There are a lot of custom startpage on the net, you can check this list of startpage http://startpages.github.io/ or search some of them on github/deviantart. 

Instruction
-------------------------------

<strong>Step 1 : Right click on the <i>.htm</i> file and open it with a browser of your choice</strong>

<strong>Step 2 : Set the startpage as the homepage </strong>
<ul>

<p>For Mozilla Firefox</p>
<ol> 
<li> go to the settings or copy/paste <i>about:preferences</i> in the URL bar. In <i>General</i>, copy/paste the URL of the startpage (it should be something like <i>file:///C:/Users/[Your name]/Documents/GALAXY/index.htm</i> in <i>Home Page</i> and choose the option <i>Show my home page</i> for <i>When Firefox starts</i>.</li>
<li> download the add-on <i>New Tab Homepage</i> (https://addons.mozilla.org/en-US/firefox/addon/new-tab-homepage/), it'll redirect you to your homepage each time you open a new tab.</li>
</ol>
<br>
<p>For Google Chrome</p>
<ol> 
<li> go to the settings. In <i>Appearance</i>, check <i>show home page</i> and modify the link with the URL of the startpage. </li>
<li> download the extension <i>New Tab Redirect</i> (https://chrome.google.com/webstore/detail/new-tab-redirect/icpgjfneehieebagbmdbhnlpiopdcmna?hl=en). </li>
</li>
</ul>
</ol>

<strong>Step 3 : Install the font </strong>

I use several fonts for the startpage.
<ol>
<li> <a href="http://www.ephifonts.com/free-helvetica-font-helvetica-rounded-complete.html">Helvetica Rounded</a>
<li> <a href="https://www.fontsquirrel.com/fonts/roboto">Roboto</a></li>
<li> <a href="https://www.freejapanesefont.com/kf-himaji/">KFhimaji</a></li>
</ol>

Features
-------------------------------

<span><i>Galaxy</i> has four main features.</span>
<ol>
<li>The sidebar has three buttons, each will make appear onclick a list of links (at least ten links per list).</li>
<li>There are three backgrounds that rotate between each other depending of the hour.</li>
<li>In the search bar, by entering some special keys, such as `-y jazz music`, you'll be able to search directly on youtube and not on Google. Another exemple with `-w moe`, it'll search 'moe' on wikipedia.</li>
<li>The weather widget by location (<a href="https://github.com/xDemonessx/homepage">code source</a>).</li>
</ol>

Customizing
-------------------------------

### Weather Location
- go to http://openweathermap.org/, create an account and generate an API key, then you'll have to call it, to do that copy/paste the following link in your URL bar, and don't forget to replace {APIKEY} by your API key : 

```javascript 
api.openweathermap.org/data/2.5/forecast?id=524901&APPID={APIKEY}
```
- open the `js`folder and edit `weather.js`in a text editor, you'll have to modify the following : replace the chain of characters after the `appid=` by your API key, and of course you'll to modify the city and country name after the `weather?q=`(if you live in London you'll have to write `weather?q=London,uk`)

```javascript
var json_url = "http://api.openweathermap.org/data/2.5/weather?q=Paris,fra&appid=a70d956581f575b02ad518684afb6c13";
```

### Search
- open the `js` folder and edit `search.js` in a text editor , you'll have to modify the following code 
``` javascript
case "-u":
query = query.substr(3);
window.location = "https://userstyles.org/styles/browse?search_terms=" 
break;
```
- first, you have to decide of a website (I will take bato.to) and a special key for this said site : I will take -b, thus you'll have the following code

``` javascript
case "-b":
query = query.substr(3);
window.location = "https://userstyles.org/styles/browse?search_terms=" 
break;
```
- after that, you'll need to replace the value of `window.location`, in the example of batoto you'll have to go to the site and search for something, for example if I'm looking for Hinamatsuri (a pretty gud manga, you should read it asap), the link will be `http://bato.to/search?name=Hinamatsuri&name_cond=c`, you'll have to copy the link before 'Hinamatsuri', namely `http://bato.to/search?name=`, and you'll have the following code 

``` javascript
case "-b":
query = query.substr(3);
window.location = "http://bato.to/search?name=" 
break;
```

Disclaimer
-------------------------------

<span>Source of the illustrations used.</span>
<ol>
<li><a href="https://www.pixiv.net/member.php?id=654533">a y u</a></li>
</ol>


Report
-------------------------------
If you find some issues or bug when using this startpage, don't hesitate to report it in the comments.
