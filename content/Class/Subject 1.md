---
tags:
  - contents
---
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
%% Preview Script %%
<script src="script/preview.js"></script>
%% Excalidraw Script %%
<script src="script/excalidraw.js"></script>
%% Excalidraw Script %%
<script src="script/graph.js"></script>
%% Study with me Script %%
<script src="script/study.js"></script>
%% Food Script %%
<script src="script/meal.js"></script>
%% Schedule Script %%
<script src="script/scheduler.js"></script>
%% Navigation bar Script %%
<script src="script/navbar.js"></script>

%% buttons %%
<span>
<button id="Link" onClick="document.getElementById('content').src = 'Subject-1/seat.pdf'" >Seat</button>
<span></span>
<button id="Link" onClick="document.getElementById('content').src = 'Subject-1/textbook.pdf'" >Textbook</button>
<span></span>
<button id="Link" onClick="document.getElementById('content').src = 'Subject-1/act.pdf'" > Task</button>
<span></span>
<button id="Link" onClick="document.getElementById('content').src = 'Subject-1/eval.pdf'" >Evaluation</button>
<br>
<button id="Link" onClick="document.getElementById('content').src ='https://excalidraw.com'" >Excalidraw</button>
<span></span>
<button id="Link" onClick="openPreview()" >Preview</button>
<span></span>
<button id="Link" onClick="openGraph()" >Graph</button>
<span></span>
<button id="Link" onClick="document.getElementById('content').src = 'Subject-1/note-1.pdf'" >Note-1</button>
<span></span>
<button id="Link" onClick="document.getElementById('content').src = 'Subject-1/note-2.pdf'" >Note-2</button>
<span></span>
<button id="Link" onClick="document.getElementById('content').src = 'Subject-1/note-3.pdf'" >Note-3</button>
<span></span>
<button class="fullbtn">Fullscreen</button> 
</span>

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
<div><iframe id="content" src="Class/Subject-1/seat.pdf" width="100%" height="1200"  frameborder="0" allowtransparency="true" marginwidth="0" marginheight="0"></iframe></div>
<div class="error"></div>
</div>
<style>#container {text-align: center;height: 100%;margin-top:4px}.error {font-weight: bold;font-size: 20px;padding: 20px;}</style>
