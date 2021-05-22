<script>
	function Startup()
	{
		Retrieve();
	}
	function Retrieve()
	{
		var xhttp = new XMLHttpRequest();
		xhttp.onreadystatechange = function() 
		{
    		if (this.readyState == 4 && this.status == 200) 
			{
       			document.getElementById("subButton").innerHTML = "SUBSCRIBE  " + JSON.parse(xhttp.responseText).items[0].statistics.subscriberCount + "";
       			document.getElementById("subcount2").innerHTML = JSON.parse(xhttp.responseText).items[0].statistics.subscriberCount + " Subscribers";
    		}
		};
		xhttp.open("GET", "https://www.googleapis.com/youtube/v3/channels?part=statistics&id=UCRYB2jgk3xu9DoAkebDnaXA&fields=items/statistics/subscriberCount&key=AIzaSyAbtXB5Uk9z-Dk94UpBfJNT64jSl5GgGe4", true);
		xhttp.send();		
	}
</script>

<body onload="Startup()">
<p align="center">
 <img width="100px" src="./logo.png" align="center" alt="Neuron Browser" />
 <h2 align="center">
    Strayfade
 </h2>
 <p align="center">
    Creating mediocre programs running in C++, C#, JavaScript, and occasionally Python. 
  <a href="https://strayfade.com">
    Visit Strayfade.com
  </a>
 </p>
</p>



  <p align="center">
    
  </p>
</p>