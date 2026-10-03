# YT-NEXUS — site de téléchargement

Page statique hébergée sur GitHub Pages : https://abdoul273.github.io/yt-nexus-site/

Le bouton et le compteur lisent l'API publique des releases de `Abdoul273/yt-nexus-site` :

- `yt-nexus.apk` : arm64-v8a (gros bouton, presque tous les téléphones) ;
- `yt-nexus-armv7.apk` : armeabi-v7a (lien « version compatible »).

Le compteur additionne les téléchargements de ces deux fichiers sur toutes les releases publiques, et se rafraîchit toutes les 90 secondes.

## Publier une nouvelle version

Après `flutter build apk --release --split-per-abi` dans `YT-DOWNLOAD/mobile` :

```fish
./publier
```

Le script lit la version dans `pubspec.yaml`, renomme les APK et crée la release `vX.Y.Z`.
