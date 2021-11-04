# VirtualBox Wiseshell Debian 11

Màquina Virtual per a desenvolupament de Truc (C/C++).

## IDE

- Ve preinstal·lat KDevelop 5.6.0.

- Tant *KDevelop* com *Eclipse for C/C++ Developers* funciona perfecte.

- Si instal·les *KDevelop* des d'AppImage versió 5.6.1 no funcionarà.

## GitHub

Pujar canvis a qualsevol repositori en GitHub **ja no es pot fer** (des de 2020 van implementar aquesta mesura de seguretat).

Passes a seguir (Obre un terminal i escriu):

- `git config --global user.name "El teu usuari"`
- `git config --global user.email "El teu email"`
- `ssh-keygen` (fes enter a tot per defecte)

Ara, fes login amb el Firefox de la màquina virtual amb el teu GitHub.

- Clica al teu perfil. Vés a *Settings* -> ([*SSH and GPG Keys*](https://github.com/settings/keys)) i clica a *New SSH Key*.
- Has de posar la teva clau **pública** que has fet amb `ssh-keygen` abans. La clau pública és la que acaba en *.pub*, és a dir, *id_rsa.pub*. La clau privada, anomenada *id_rsa*, **és teva i no l'has de compartir amb ningú**.

Per a introduir la clau pública pots anar amb el gestor de fitxers a `/home/wiseshell/.ssh/` i copiar els continguts del fitxer *id_rsa.pub*. Si no veus la carpeta *.local* al gestor de fitxers, hauràs d'anar al menú i clicar *Visualitza -> Mostra els Fitxers Ocults*.

Si vols fer-ho amb un terminal, pots aplicar la següent ordre:
`cat /home/wiseshell/.ssh/id_rsa.pub`. Et mostrarà tot d'una el contingut del fitxer. Copia'l.

- Vés al navegador i fes CTRL+V a l'apartat de *Key*. Al *Title*, pots posar el que trobis, *Wiseshell SSH* o *Default*, per exemple.
