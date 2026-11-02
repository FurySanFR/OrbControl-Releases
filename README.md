# OrbControl

Pilote la lumière de présence **Luxafor Orb** sans le logiciel Luxafor : l'Orb prend la couleur de votre statut
Teams, ou celle que vous choisissez, depuis l'icône près de l'horloge.

**[Télécharger la dernière version](https://github.com/FurySanFR/OrbControl-Releases/releases/latest)** (fichier
`OrbControl-Setup-vX.Y.Z.exe`)

## Installer

1. Téléchargez `OrbControl-Setup-vX.Y.Z.exe` depuis la [dernière version](https://github.com/FurySanFR/OrbControl-Releases/releases/latest).
2. Lancez-le. Si Windows affiche « Windows a protégé votre ordinateur », cliquez **Informations complémentaires**,
   puis **Exécuter quand même** : l'installeur est signé (« FurySan code signing »), mais ce certificat n'est pas
   connu de Windows.
3. Cliquez **Installer**. Aucun droit administrateur n'est demandé : OrbControl s'installe pour vous seul
   (`%LOCALAPPDATA%\Programs\OrbControl`). L'option « pour tous les utilisateurs » demande, elle, les droits
   administrateur.
4. OrbControl se lance : son icône apparaît près de l'horloge (au besoin dans la flèche des icônes cachées). Il
   démarre ensuite avec Windows.

Il vous faut Windows 11 (64 bits ; Windows 10 n'a pas été essayé) et un Luxafor Orb branché en USB. Fermez le
logiciel Luxafor s'il est installé : un seul programme à la fois peut piloter l'Orb.

## Utiliser

Tout se fait par un **clic droit sur l'icône** :

| Entrée | Effet |
|---|---|
| En tête (grisée) | La lumière actuelle et qui la pilote. |
| Disponible, Occupé, En réunion, Ne pas déranger, De retour bientôt, Absent, Éteindre | Choisir la lumière à la main. |
| Durée › | Combien de temps tient le prochain choix : 15 min, 30 min, 1 h, jusqu'à nouvel ordre. |
| Retour en auto | Rendre la main au suivi automatique (Teams) avant la fin de la durée. |
| Automatique › | Les sources suivies (Statut Teams, Réunion Teams…) et « Changer aussi mon statut Teams » (cochée par défaut). |
| Installer la mise à jour | Visible quand une nouvelle version est prête. |
| Quitter | Ferme OrbControl et éteint l'Orb. |

Couleurs : vert = Disponible, rouge = Occupé, En réunion, Ne pas déranger, orange = De retour bientôt, Absent.

« Ouvrir OrbControl » n'ouvre encore rien : la fenêtre arrivera dans une prochaine version.

## Suivi de Teams

L'Orb et Teams restent synchronisés dans les deux sens : un statut choisi dans le menu de l'icône change aussi votre
statut Teams (le temps de la durée choisie, puis Teams reprend son statut automatique), et un statut changé dans
Teams change la lumière, même après un choix fait dans le menu (quelques secondes après ce choix, le temps que Teams
l'applique). « En réunion » n'existe pas dans Teams : choisi dans le menu, il tient jusqu'à la fin de sa durée. Pour que le menu ne touche pas à Teams,
décochez « Changer aussi mon statut Teams » dans Automatique ›.

OrbControl suit le **nouveau Teams** (Teams pour le travail ou l'école) ouvert sur ce poste : il lit son journal local
et son statut affiché, sans compte, sans connexion à Microsoft et sans rien envoyer. « Changer aussi mon statut
Teams » demande Teams ouvert et en français.

## Mises à jour

Rien à faire : au démarrage, OrbControl cherche une nouvelle version ici, la télécharge, vérifie sa signature et
l'installe sans fenêtre (l'Orb s'éteint deux secondes, puis reprend). Une version trouvée en cours de journée
s'installe au démarrage suivant, ou tout de suite par « Installer la mise à jour » dans le menu de l'icône.
Installé pour tous les utilisateurs, OrbControl se met à jour au clic seulement.

## Vie privée

- Rien ne quitte votre poste : la seule connexion sortante est la recherche de mise à jour sur ce dépôt.
- L'interface locale d'OrbControl n'écoute que `127.0.0.1` (ce poste) et demande un jeton.
- Réglages et journal : `%LOCALAPPDATA%\OrbControl`.

## Désinstaller

Paramètres › Applications › **Applications installées** › OrbControl › Désinstaller. Pour tout effacer, supprimez
ensuite le dossier `%LOCALAPPDATA%\OrbControl` (réglages et journal).

## Problème ?

| Ce que vous voyez | Que faire |
|---|---|
| L'Orb ne s'allume pas | Rebranchez-le ; fermez le logiciel Luxafor s'il tourne. |
| L'Orb ne suit pas Teams | Vérifiez que Teams est ouvert et que « Statut Teams » est coché dans Automatique ›. |
| Pas d'icône près de l'horloge | Lancez OrbControl depuis le menu Démarrer. |

Sinon, contactez la personne qui vous a transmis OrbControl, en joignant le fichier
`%LOCALAPPDATA%\OrbControl\orbcontrol.log`.

---

OrbControl n'est pas affilié à Luxafor ni à Microsoft.
