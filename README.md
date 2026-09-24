<!DOCTYPE html>
<html>
<head>
    <title>eulysis</title>
</head>
<body>
    
    <style>
        body {
            background-image: url("mama.jpg");
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
        }
    </style>
  
    
    <h1>Current Time</h1>
    <div id="clock"></div>

    <script>
        function showTime() {
            let now = new Date();
            let time = now.toLocaleTimeString();

            document.getElementById("clock").innerHTML = time;
        }

        setInterval(showTime, 1000);
        showTime();
    </script>
    
    <h2>My Location</h2>

    <button onclick="getLocation()">Get My Location</button>

    <p id="location">Location will appear here.</p>

    <script>
        function getLocation() {
            if (navigator.geolocation) {
                navigator.geolocation.getCurrentPosition(showPosition, showError);
            } else {
                document.getElementById("location").innerHTML =
                    "Geolocation is not supported by this browser.";
            }
        }

        function showPosition(position) {
            let latitude = position.coords.latitude;
            let longitude = position.coords.longitude;

            document.getElementById("location").innerHTML =
                "Latitude: " + latitude + "<br>" +
                "Longitude: " + longitude;
        }

        function showError(error) {
            document.getElementById("location").innerHTML =
                "Unable to get your location.";
        }
    </script>
    
    <a href="https://youtu.be/HD13eq_Pmp8?si=dHsqr3QJ_pEZ6mgE">youtube</a>



</body>
</html># Eulysis-martin
