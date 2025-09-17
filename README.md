<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Redirection Défense+</title>
  <script>
    window.onload = function () {
      var userAgent = navigator.userAgent || navigator.vendor || window.opera;
      var iosLink = "https://testflight.apple.com/join/mn1f2ggg"; // Lien iOS
      var androidLink = "https://play.google.com/store/apps/details?id=fr.gouv.defense.minarm.defenseplus"; // Lien Android
      var fallbackLink = "https://www.defense.gouv.fr"; // Lien par défaut

      if (/android/i.test(userAgent)) {
        window.location.href = androidLink;
      } else if (/iPad|iPhone|iPod/.test(userAgent) && !window.MSStream) {
        window.location.href = iosLink;
      } else {
        window.location.href = fallbackLink;
      }
    };
  </script>
</head>
<body>
  <p>Redirection en cours...</p>
</body>
</html>
