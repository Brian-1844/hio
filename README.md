# Hiʻo Video 🎥

Caméra vidéo et photo pour téléphone : effets, réglages d'image, zoom, flash, retardateur,
position GPS incrustée, et des fonctions rigolotes (miroir, kaléidoscope, pixel art, pop art,
pluie de tiaré, bulles, poissons, autocollants, texte sur la vidéo, arc-en-ciel).

Retouche après coup : couleurs et effets, recadrage (carré, vertical, paysage), rotation,
couper le début et la fin, titre, **musique** (4 airs intégrés : ukulélé, reggae, électro, piano,
ou ta propre musique). Une photo avec musique devient une petite vidéo qui zoome doucement.
Onglet **🪄 Magie** pour les photos (visage détecté par IA) : rajeunir, vieillir, petites farces
(gros yeux, grosse tête, nez de clown, moustache, lunettes, couronne de fleurs, oreilles de chat,
extraterrestre), aura colorée, et changement de fond (flou, plage de Tahiti, coucher de soleil,
nuit étoilée, studio, couleur, ta photo, sans fond). Dans l'APK, l'IA marche même sans internet.
Mode **3D** : rafale de photos en tournant autour d'un objet, exportée en fichier ZIP pour créer un
modèle 3D (RealityScan, Polycam, Meshroom, Tripo). Zoom avec deux doigts sur les photos.
Partage direct vers WhatsApp, Facebook, etc., bouton de mise à jour, et bouton pour installer
l'icône sur l'écran d'accueil.

- **Version web** : https://brian-1844.github.io/hio/
- **App Android (APK)** : https://github.com/Brian-1844/hio/releases/latest/download/hio-video.apk

## Mettre en ligne (une seule fois)

1. Sur GitHub, crée un dépôt **public** nommé `hio`.
2. Envoie tous les fichiers de ce dossier (dont le dossier caché `.github`).
3. **Settings → Pages** : Source = *Deploy from a branch*, branche `main`, dossier `/ (root)`.
4. **Settings → Actions → General → Workflow permissions** : coche *Read and write permissions*.
5. L'onglet **Actions** construit l'APK tout seul (environ 5 minutes). Il apparaît ensuite dans **Releases**.

## Publier une mise à jour

1. Modifie `index.html`.
2. Augmente le numéro de version au **même** endroit dans ces 3 fichiers :
   `index.html` (`APP_VERSION`), `version.json` et `sw.js` (`CACHE`).
3. Envoie les fichiers sur GitHub. Un nouvel APK est construit automatiquement.
4. Dans l'app, le bouton ⬇ (en haut à droite) affiche un point rouge et propose la mise à jour.

## Bon à savoir

- La caméra ne marche que sur une adresse en `https://` (GitHub Pages le fait).
- **Clé de signature (obligatoire, secrète)** : dans GitHub, *Settings → Secrets and variables → Actions →
  New repository secret*, crée `KEYSTORE_BASE64` (contenu du fichier KEYSTORE_BASE64.txt) et
  `KEYSTORE_PASSWORD` (contenu de KEYSTORE_PASSWORD.txt). Garde aussi le fichier `hio-video-NEW.jks` en
  lieu sûr (clé USB, Google Drive privé) : sans lui, plus de mises à jour possibles. Ne le mets jamais
  dans le dépôt.
- Au premier lancement de l'APK, Android demande d'autoriser l'installation depuis le navigateur,
  puis l'accès à la caméra, au micro et à la position.
