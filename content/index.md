---
title: Home
tags:
  - contents
comments: "false"
---
<title>Filmnt</title>
%% jQuery script %%
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.7.1/jquery.min.js"></script>
%% html2canvas script %%
<script src="script/html2canvas.js"></script>
%% Webcam script %%
<script src="script/cam.js"></script>
%% md-editor script %%
<script src="script/simplemde.min.js"></script>
<script src="script/md-editor.js"></script>
%% tts script %%
<script src="script/tts.js"></script>
%% progressbar script %%
<script>
function getCurrentProgress(){
  const firstDateOfYear = new Date(new Date().getFullYear(), 0, 1);
  const currentDate = new Date();
  return ((((currentDate - firstDateOfYear) / (1000 * 60 * 60 * 24)) * 100) / 365).toFixed(1);}
function updateUI() {const percent = getCurrentProgress();
  const barItem = document.getElementsByClassName('bar')[0];barItem.style.width = `${percent}%`;
  const counterItem = document.getElementsByClassName('value')[0];
  if (percent>100){counterItem.textContent = `100%`}else{counterItem.textContent = `${percent}%`;}}
setInterval(function() {updateUI();return arguments.callee;}(), 1000);
</script>

%% Link %%
<style>#ClockWidget{margin-top:-25px;margin-bottom:-2px;font-size:1.7em;}
h3{margin-top:-15px}#TopBtn,#DownBtn,#threedots{display:none}</style>
%% home navbar icon %%
<button title="Navigation" id="navbar" style="position:fixed;bottom: 40px;float:right;right: 28px;width: 40px;height:40px;opacity:0.3;z-index:1" onclick="openNavbar()"><i class="fa-solid fa-bars fa-xl"></i></button>
%% Links script %%
<script type="text/javascript">
var url = document.getElementById( 'linkshare' );
url.onchange = function() {window.open( this.options[ this.selectedIndex ].value, '_blank');
$('#linkshare').prop('selectedIndex',0);};
</script>
%% Translator script%%
<script>window.ResetTranslate = () => jQuery('#\\:1\\.container').contents().find('#\\:1\\.restore').click();</script>
<script>
    function googleTranslateElementInit() {
        new google.translate.TranslateElement({pageLanguage: 'en'},'google_translate_element');}
</script>
<script type="text/javascript" src="//translate.google.com/translate_a/element.js?cb=googleTranslateElementInit"></script>
%% share&fullcreen button script %%
<script src="script/full-share.js"></script>
%% WhiteNoise Script %%
<script type="text/javascript" src="script/WN.js"></script>
%% Graph Script %%
<script src="script/graph.js"></script>
%% Preview Script %%
<script src="script/preview.js"></script>
%% Excalidraw Script %%
<script src="script/excalidraw.js"></script>
%% Study with me Script %%
<script src="script/study.js"></script>
%% Food Script %%
<script src="script/meal.js"></script>
%% Schedule Script %%
<script src="script/scheduler.js"></script>
%% Navigation bar Script %%
<script src="script/home-navbar.js"></script>




%% ip address & city %%
<h3 ><span id="hello"></span><span id='browser'>Disable AdBlock for greetings… 📛</span></h3>
<script src='script/agent.js'></script>

<h1 style="font-size:26px" id="ClockWidget" onload="showTime()" > </h1> 
<script src="script/clock.js"></script>


%% Carousel (Weather, Map, Stock %%
<style>
.slideshow-container {position: relative;margin: auto;display:block;height:100%;width:100%;margin-top:6px;margin-bottom:-10px;}
.prev, .next {cursor: pointer;position: absolute;top: 35%;width: auto;padding: 5px;color:#646464;font-weight: bold;font-size: 20px;transition: 0.6s ease;border-radius: 0 3px 3px 0; user-select: none;}
.next {right: 0;border-radius: 3px 0 0 3px;}
</style>

<div class="slideshow-container" >
<div class="Slides">
<a class="weatherwidget-io" href="https://forecast7.com/en/35d54129d31/ulsan/" data-label_1="울산" data-label_2="WEATHER" data-font="Noto Sans" data-icons="Climacons Animated" data-theme="weather_one" target=”_blank”> </a>
</div>

<div class="Slides">
<div id="mapping"></div>
</div>

<div class="Slides">
<iframe width="100%" height="450" src="https://embed.windy.com/embed.html?type=map&location=coordinates&metricRain=default&metricTemp=default&metricWind=default&zoom=5&overlay=wind&product=ecmwf&level=surface" frameborder="0"></iframe>
</div>

<a class="prev" onclick="plusSlides(-1)"><i class="fa-solid fa-chevron-left fa-xl"></i></a>
<a class="next" onclick="plusSlides(1)"><i class="fa-solid fa-chevron-right fa-xl"></i></a>
</div>

<script src="script/carousel.js"></script>
<script>
!function(d,s,id){var js,fjs=d.getElementsByTagName(s)[0];if(!d.getElementById(id)){js=d.createElement(s);js.id=id;js.src='https://weatherwidget.io/js/widget.min.js';fjs.parentNode.insertBefore(js,fjs);}}(document,'script','weatherwidget-io-js'); setInterval('__weatherwidget_init()', 900000);

document.getElementById('switchLocation').addEventListener('change', function(){
      var widget = document.querySelector('.weatherwidget-io');
      widget.href = 'https://forecast7.com/en/'+this.value;
      widget.dataset.label_1 = this.options[this.selectedIndex].text;
      __weatherwidget_init();  
});

document.getElementById( 'switchLocation' ).onchange = function() {$('#switchLocation').prop('selectedIndex',0);};
</script>

%% embed %%
%% buttons %%
<span><button class="fullbtn">Fullscreen</button></span>

<style>
.fullbtn {float:right;height:30px;background-color: #007BFF;color: #fff; border: none; border-radius: 5px;cursor: pointer;transition: background-color 0.3s;}  
.fullbtn:hover {background-color: #0056b3;}
</style>

%% fullscreen btn %%
<script>
var button = document.querySelector('.fullbtn');
button.addEventListener('click', fullscreen);
// when you are in fullscreen, ESC and F11 may not be trigger by keydown listener. 
// so don't use it to detect exit fullscreen
document.addEventListener('keydown', function (e) {
  console.log('key press' + e.keyCode);
});
// detect enter or exit fullscreen mode
document.addEventListener('webkitfullscreenchange', fullscreenChange);
document.addEventListener('mozfullscreenchange', fullscreenChange);
document.addEventListener('fullscreenchange', fullscreenChange);
document.addEventListener('MSFullscreenChange', fullscreenChange);

function fullscreen() {
  // check if fullscreen mode is available
  if (document.fullscreenEnabled || 
    document.webkitFullscreenEnabled || 
    document.mozFullScreenEnabled ||
    document.msFullscreenEnabled) {
    
    // which element will be fullscreen
    var iframe = document.querySelector('#container iframe');
    // Do fullscreen
    if (iframe.requestFullscreen) {
      iframe.requestFullscreen();
    } else if (iframe.webkitRequestFullscreen) {
      iframe.webkitRequestFullscreen();
    } else if (iframe.mozRequestFullScreen) {
      iframe.mozRequestFullScreen();
    } else if (iframe.msRequestFullscreen) {
      iframe.msRequestFullscreen();
    }
  }
  else {
    document.querySelector('.error').innerHTML = 'Your browser is not supported';
  }
}

function fullscreenChange() {
  if (document.fullscreenEnabled ||
       document.webkitIsFullScreen || 
       document.mozFullScreen ||
       document.msFullscreenElement) {
    console.log('enter fullscreen');
  }
  else {
    console.log('exit fullscreen');
  }
  // force to reload iframe once to prevent the iframe source didn't care about trying to resize the window
  // comment this line and you will see
  var iframe = document.querySelector('iframe');
  iframe.src = iframe.src;
}
</script>





%% content %%
<div id="container">
<div><iframe id="content" src="2025-notebook.pdf" width="100%" height="1200"  frameborder="0" allowtransparency="true" marginwidth="0" marginheight="0"></iframe></div>
<div class="error"></div>
</div>
<style>#container {text-align: center;height: 100%;margin-top:4px}.error {font-weight: bold;font-size: 20px;padding: 20px;}</style>


