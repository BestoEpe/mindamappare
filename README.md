# mindamappare

https://replit.com/@BestoEpe/mindamappare#script.js

mindmap juttu



html
-------------------------------------------------
<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>apina</title>
    <link href="style.css" rel="stylesheet" type="text/css" />
  </head>
  <style>
   img {
    widht: 1297,334;
    height: 641,52;
  }
   
  </style>
  <body>

    <div id="orange"> </div>
    
    <img src="neukkari.png" usemap="#image-map">
  
    <map name="image-map">

      
      <area target="" alt="huone 1" title="" href="" coords="84,693,955,765" shape="rect" onmouseover="">


    </map>

 <script src="script.js"> </script>

<p><a
 href="https://github.com/BestoEpe/mindamappare/edit/main/README.md">
<img onmouseover="bigImg(this)" onmouseout="normalImg(this)" border="0" src="red.png" alt="Smiley" width="10" height="10">
</a></p>

<script>
function bigImg(x) {
  x.style.height = "90px";
  x.style.width = "90px";
}

function normalImg(x) {
  x.style.height = "10px";
  x.style.width = "10px";
}
</script>

  </body>
</html>
-------------------------------------------------------------
js
--------------------------------------------------------------
link()
async function link() {
  let url = 'https://api.thingspeak.com/channels/1630408/feeds.json?results=1'

  const fetchResults = await fetch(url);
  const jsonResult = await fetchResults.json();
  const feedsResults = jsonResult.feeds;


for (const i in feedsResults) {
  console.log(feedsResults[i].field1)

  if (feedsResults[i].field1 == 1) {
    console.log("varattu")
    document.getElementById("green").setAttribute("id", "orange");}
    
  else {console.log("vapaa")
  document.getElementById("orange").setAttribute("id", "green");}
  }
}
----------------------------------------------------------
css
--------------------------------------------------------
#green {
  width: 69px;
  height: 67px;
  background-color: green;
  border: 2px rgb(0, 0, 0);
  position: absolute;
  top: 699px;
  left: 888px;
  padding: 5px;

  opacity: 0.5;
  pointer-events: none;
}

#orange {
  width: 69px;
  height: 67px;
  background-color: rgba(255, 73, 1, 0.986);
  border: 2px rgb(0, 0, 0);
  position: absolute;
  top: 699px;
  left: 888px;
  padding: 5px;

  opacity: 0.5;
  pointer-events: none;
}
------------------------------------------------------------

