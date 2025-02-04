to<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NVN Music HD</title>
    <link rel="stylesheet" href="style.css">
    <script defer src="script.js"></script>
</head>
<body>
    <header>
        <h1>NVN Music HD</h1>
        <input type="text" id="searchBar" placeholder="Search for songs...">
    </header>
    
    <div id="video-container">
        <div class="video" data-title="Song 1">
            <h2>Song 1</h2>
            <iframe src="https://www.youtube.com/embed/YOUR_VIDEO_ID" allowfullscreen></iframe>
            <p>Lyrics: Lorem ipsum dolor sit amet...</p>
        </div>

        <div class="video" data-title="Song 2">
            <h2>Song 2</h2>
            <iframe src="https://www.youtube.com/embed/YOUR_VIDEO_ID" allowfullscreen></iframe>
            <p>Lyrics: Lorem ipsum dolor sit amet...</p>
        </div>

        <!-- Add more videos here -->
    </div>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    text-align: center;
    background-color: #f4f4f4;
}
header {
    background: #222;
    color: white;
    padding: 20px;
}
#searchBar {
    padding: 10px;
    width: 80%;
    margin-top: 10px;
}
#video-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    padding: 20px;
}
.video {
    background: white;
    margin: 10px;
    padding: 20px;
    width: 300px;
    border-radius: 10px;
}
iframe {
    width: 100%;
    height: 200px;
}document.getElementById("searchBar").addEventListener("keyup", function() {
    let filter = this.value.toLowerCase();
    let videos = document.querySelectorAll(".video");

    videos.forEach(video => {
        let title = video.getAttribute("data-title").toLowerCase();
        if (title.includes(filter)) {
            video.style.display = "block";
        } else {
            video.style.display = "none";
        }
    });
});
