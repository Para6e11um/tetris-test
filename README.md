# Tetris Test

Projet de jeu Android natif indépendant en Java, compatible avec Android 6.0 et versions ultérieures.

## Fonctionnalités prévues

- Commandes tactiles : gauche, droite et rotation.
- Descente accélérée et chute immédiate.
- Compteur de points.
- 10 niveaux avec vitesse progressive.
- Écran Game Over et bouton Rejouer.
- Pause et reprise de la partie.

## État du projet

Les sources et la configuration GitHub Actions ont été préparées, mais leur publication dans ce dépôt est bloquée par les droits d’écriture de la connexion GitHub.

Aucune APK n’est encore disponible. Ajouter ce README seul ne crée pas le jeu : il faut également déposer les fichiers du projet, notamment le dossier `app` et le fichier `.github/workflows/android.yml`.

## Télécharger l’APK sur Android

Une fois les fichiers publiés et la compilation réussie :

1. Ouvrir https://github.com/Para6e11um/tetris-test/actions.
2. Choisir le workflow **Android APK**.
3. Ouvrir une exécution réussie, indiquée en vert.
4. Dans **Artifacts**, télécharger **Tetris-Test-APK**.
5. Extraire le ZIP et ouvrir **Tetris-Test.apk**.
6. Si Android le demande, autoriser l’installation d’applications inconnues pour le navigateur ou l’application Fichiers utilisée.

Si la section Artifacts n’apparaît pas sur téléphone, activer la version pour ordinateur du site dans le navigateur.

## Compilation

Outils nécessaires :

- JDK 17.
- Gradle 8.9.
- SDK Android : plateforme 35 et Build Tools 35.0.0.

Commande à exécuter à la racine du projet :

```sh
gradle testDebugUnitTest lintDebug assembleDebug
```

APK générée :

```text
app/build/outputs/apk/debug/app-debug.apk
```

GitHub Actions installera ces outils automatiquement lorsque le workflow sera présent dans le dépôt.

## Signature

L’APK de test sera signée automatiquement en mode debug, sans secret à configurer.

Une clé de signature stable sera nécessaire pour distribuer des mises à jour durables ou préparer une publication sur le Play Store.