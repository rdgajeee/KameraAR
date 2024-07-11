# Kamera-AR-Daka-Heldian-2113025020

Penambahan Kamera AR
Daka Heldian
NPM 2113025020
Mata Kuliah Augmented Reality

Source Code:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kamera AR - Daka Heldian</title>
    <script src="https://aframe.io/releases/1.2.0/aframe.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/ar.js"></script> 
    <script>
      AFRAME.registerComponent('move-object', {
        init: function () {
          var el = this.el;
          var step = 0.1; 

          window.addEventListener('keydown', function (event) {
            switch (event.key) {
              case 'ArrowUp':
                el.object3D.position.y += step;
                break;
              case 'ArrowDown':
                el.object3D.position.y -= step;
                break;
              case 'ArrowLeft':
                el.object3D.position.x -= step;
                break;
              case 'ArrowRight':
                el.object3D.position.x += step;
                break;
            }
          });
        }
      });
    </script>

</head>
<body>
    <!-- Penambahan Kamera AR dengan kursor dan kontrol keyboard -->
    <a-scene embedded arjs="sourceType: webcam;">
        <a-box position="6 2 -6" width="4" height="4" depth="4" color="yellow"></a-box>
        <a-entity camera look-controls wasd-controls position="0 1.6 0" cursor="rayOrigin: mouse;"></a-entity>
    </a-scene>

</body>
</html>
