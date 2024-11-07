# ibn-alhaeysm
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Camera Evolution Timeline</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>Camera Evolution Timeline</h1>
    <p>Learn about the development of cameras over time, from the early camera obscura to modern smartphones.</p>
  </header>

  <div class="timeline">
    <!-- Camera Obscura Section -->
    <div class="timeline-item">
      <h2>1. Camera Obscura (Ibn Heysem)</h2>
      <img src="images/camera-obscura.jpg" alt="Camera Obscura" class="timeline-img">
      <p>In the 11th century, Ibn Heysem discovered the principle of the camera obscura, laying the foundation for modern optics.</p>
    </div>

    <!-- Photo Plate Section -->
    <div class="timeline-item">
      <h2>2. Photo Plates (19th Century)</h2>
      <img src="images/photo-plate.jpg" alt="Photo Plate" class="timeline-img">
      <p>In the 19th century, photo plates using light-sensitive chemicals started capturing permanent images.</p>
    </div>

    <!-- Film Camera Section -->
    <div class="timeline-item">
      <h2>3. Film Cameras (20th Century)</h2>
      <img src="images/film-camera.jpg" alt="Film Camera" class="timeline-img">
      <p>Film cameras were developed in the 20th century, making photography portable and more accessible.</p>
    </div>

    <!-- Digital Camera Section -->
    <div class="timeline-item">
      <h2>4. Digital Cameras</h2>
      <img src="images/digital-camera.jpg" alt="Digital Camera" class="timeline-img">
      <p>Digital cameras allowed images to be captured without film, storing photos on digital memory cards.</p>
    </div>

    <!-- Smartphone Camera Section -->
    <div class="timeline-item">
      <h2>5. Smartphone Cameras</h2>
      <img src="images/smartphone-camera.jpg" alt="Smartphone Camera" class="timeline-img">
      <p>Modern smartphones now feature high-resolution cameras, allowing photography on the go.</p>
    </div>
  </div>

  <script src="script.js"></script>
</body>
</html>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  background-color: #f4f4f4;
  color: #333;
  padding: 20px;
}

header {
  text-align: center;
  margin-bottom: 40px;
}

h1 {
  font-size: 36px;
  color: #333;
}

.timeline {
  width: 100%;
  max-width: 1000px;
  margin: 0 auto;
}

.timeline-item {
  background: #fff;
  margin: 20px 0;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.5s ease;
}

.timeline-item:hover {
  transform: translateY(-10px);
}

.timeline-img {
  max-width: 100%;
  height: auto;
  border-radius: 5px;
  margin-bottom: 10px;
}

.timeline h2 {
  font-size: 24px;
  margin-bottom: 10px;
}

.timeline p {
  font-size: 16px;
}
document.addEventListener("DOMContentLoaded", function() {
  const timelineItems = document.querySelectorAll('.timeline-item');
  
  window.addEventListener('scroll', function() {
    const scrollPosition = window.scrollY + window.innerHeight;

    timelineItems.forEach(function(item) {
      if (item.offsetTop < scrollPosition) {
        item.style.opacity = 1;
        item.style.transform = 'translateY(0)';
      } else {
        item.style.opacity = 0;
        item.style.transform = 'translateY(50px)';
      }
    });
  });
});
