# Anime Mind 3.0 — projet Android

Ce dossier contient le projet Android Studio qui embarque le jeu Anime Mind et ses images dans une application Android native avec WebView.

## Générer l'APK
1. Installe Android Studio sur un ordinateur.
2. Décompresse `AnimeMindAndroid.zip`.
3. Dans Android Studio, choisis **Open** et sélectionne le dossier `AnimeMindAndroid`.
4. Attends la synchronisation Gradle et l'installation éventuelle du SDK Android 35.
5. Ouvre **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
6. Android Studio générera l'APK debug dans `app/build/outputs/apk/debug/app-debug.apk`.
7. Transfère `app-debug.apk` sur ton téléphone Android et ouvre-le pour l'installer. Si Android le demande, autorise l'installation depuis cette source.

## Configuration
- Nom : Anime Mind
- Identifiant : `com.animemind.game`
- Version : 3.0
- Android minimum : Android 6.0 (API 23)
- Orientation : portrait

## Note importante
Ce paquet est le projet source Android prêt à être compilé, pas un APK déjà compilé. L'environnement de création utilisé ici ne contient pas Android SDK / Gradle, donc il ne peut pas produire ni signer directement le fichier APK. La mini-IA reste la base locale intégrée au jeu ; elle n'est pas un service IA connecté au cloud.


## Compilation automatique dans le cloud (sans installer Android Studio)
Le dossier `.github/workflows/build-apk.yml` permet de compiler l'APK avec GitHub Actions.
1. Crée un compte GitHub si nécessaire, puis un nouveau dépôt (repository) privé ou public.
2. Sur GitHub, envoie le contenu de ce dossier `AnimeMindAndroid` dans le dépôt (bouton **Add file > Upload files**). Vérifie que le dossier `.github/workflows` est bien inclus.
3. Ouvre l'onglet **Actions** du dépôt.
4. Choisis **Build Anime Mind APK**, puis **Run workflow**.
5. À la fin du processus, ouvre l'exécution terminée et télécharge l'artefact **AnimeMind-APK**.
6. Décompresse l'artefact téléchargé : il contient `app-debug.apk`. Envoie-le sur ton téléphone et ouvre-le pour l'installer.

GitHub compile le projet sur ses serveurs ; ce workflow ne publie pas l'application sur le Play Store. L'APK debug est destiné à l'installation et aux essais personnels.
