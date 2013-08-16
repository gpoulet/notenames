This is the fork from [Jojo-Schmitz] (https://github.com/Jojo-Schmitz/notenames)
This projet will probably interest only French speaker.
That's why I won't translate the complete instructions in English.

x x x x x x x x x x x x x x x x x x

Ceci est un fork du projet "Note Name plugin" de [Jojo-Schmitz] (https://github.com/Jojo-Schmitz/notenames)

C'est un plugin qui permet d'afficher � la base les notes en lettre (�criture anglaise) : A pour la, B pour si, etc.
Il est pr�sent de base dans MuseScore (j'utilise la version 1.3).

Jojo-Schmitz a am�lior� celui-ci. Il est cens� remplacer celui de base.

J'ai modifi� le fichier de traduction fran�ais pour r�duire la longueur des chaines
(ex : remplacement de "Fa diese" par "fa#")



INSTRUCTIONS D'INSTALLATION (Windows)
--------------------------

1) T�l�charger le projet ("Download ZIP" en bas � droite")
Normalement le fichier t�l�charg� doit s'appeller "notenames-master.zip"

2) D�compressez l'archive. On devrait donc avoir nos fichiers d�compress� pr�sents dans un dossier /notenames-master/

3) Se rendre dans le r�pertoire /plugins/ pr�sent dans le r�pertoire d'installation
ex : C:\Program Files(x86)\MuseScore\plugins

4) Supprimer le fichier "notenames.js"

5) D�placer le contenu de /notenames-master/ (dossier d�compress�) dans /plugins/ (pr�sent dans le r�pertoire d'installation) :

8�152 notenames.js
7�550 notenames.qml
1�789 Readme.md
<REP> /translations/

6) T�l�charger le framework Qt sur http://qt-project.org/downloads

Prenez cette version : Qt 5.1.0 for Windows 32-bit (MinGW 4.8, OpenGL, 666 MB)
(Il faut obligatoirement avoir MinGW avec Qt)

7) Installer le framework Qt que vous venez de t�l�charger

8) Ouvrir avec un �diteur de texte le fichier C:\Program Files (x86)\MuseScore\plugins\translations\lrelease.cmd

9) Modifier le chemin d'acc�s pour qu'il pointe sur lrelease.exe pr�sent dans le dossier \bin\ de l'installation de minGW

ex : C:/Qt/Qt5.1.0/5.1.0/mingw48_32/bin/lrelease
(C'est bien des Slash, pas des Antislash)

Ce qui donne chez moi en fichier complet :

C:/Qt/Qt5.1.0/5.1.0/mingw48_32/bin/lrelease *.ts
pause

10) Enregistrer les modifications

11) Lancer en faisant un double-clic le fichier C:\Program Files (x86)\MuseScore\plugins\translations\lrelease.cmd

12) Normalement le fichier s'ex�cute et termine sur le message "pause". Appuyez sur la touche ESPACE par exemple. La fen�tre se ferme.

13) Le plugin est � pr�sent utilisable dans MuseScore : Plugins > Notes > Notes Names

Il y a quelques ajustement � faire �videmment pour que �a soit parfait, par exemple mettre la queue des notes en bas, sinon le nom des notes est cach� par celles-ci.

/!\ J'ai les notes qui se chevauchent car �a m'affiche "Fa diese" au lieu de "fa#" /!\
Vous avez mal suivi les instructions : reprenez au 7) >:-D



INSTRUCTIONS D'INSTALLATION (Mac OS) :
---------------------------------------

A venir (contributions les bienvenues)



INSTRUCTIONS D'INSTALLATION (Windows) :
----------------------------------------

A venir (contributions les bienvenues)


==============================================================================

Old Readme from [Jojo-Schmitz] (https://github.com/Jojo-Schmitz/notenames) :
----------------------------------------------------------------------------

This Plugin for MuseScore is derived from the [Note Names plugin] (http://musescore.org/en/handbook/plugins#notenames) that comes as part of MuseScore and is meant to replace that.
It adds the note names of all notes in either the current selection or all voices of all staves in the entire score as staff text (above/below the staff) and uses note names according to the locale MuseScore is configured for rather than just the English note names C, D, E, F, G, A, B.
So the output changes with the setting of Menu -> Edit -> Preferences... -> General -> Language, resp. if that is set to 'System', the output depends on the language setting of your PC.
As a further extensions it also names notes with sharps, double sharps and double flats and the notename moves aside a bit, if it would otherwise collide with the note.

Available locales: English, German, Dutch, Japanese, Italian, French, Spanish, Portuguese, Russian, Romainan, Danish, Norwegian, Swedish, Polish, Slovak, Czech and Greek.

The double sharp and double flat notes as well as Fb, Cb, E# and B# still need translation into Italian, French, Spanish, Portuguese, Russian, Romanian and Greek, help is more than welcome.

If you also want it to show courtesy- and microtonal accidentals, change `false` to `true` in the plugin code. Note however, that none of these have yet been translated, and their 'clear text' names can be rather long (e.g. "mirrored-flat-slash").

To use the plugin, you must first install it according to the [instructions in the Handbook] (http://musescore.org/en/handbook/plugins "Handbook").

The idea for this plugin stems from a [discussion in the forum] (http://musescore.org/en/node/16786), the microtonal extension from [another discussion in the forum] (http://musescore.org/en/node/16870).
