# VirtualBox Wiseshell Debian 11

Màquina Virtual per a desenvolupament de Truc (C/C++).<br/>
VirtualBox versió 6.1.26.

**Requeriments**: 2048 MB de memòria RAM lliures.

## Setup

- Descarrega't la màquina virtual [aquí](https://github.com/wiseshell-net/wiseshell-vm/releases/download/1.0.0/Debian_11_WiseShell_Development_VM.zip).
- Descomprimeix el fitxer.
- Obre VirtualBox.
- Fes al menú i fes clic a *Màquina* i després a *Afegeix*.
- Vés al lloc on tens descarregada la màquina virtual i localitza el fitxer *.vbox* (t'ho hauria d'indicar la pròpia finestra del VirtualBox).
- Arranca la màquina i comprova que tot funciona.

## Login

- Nom d'usuari: wiseshell
- Contrasenya: wiseshell

## IDE

- Ve preinstal·lat KDevelop 5.6.0.

- Tant *KDevelop* com *Eclipse for C/C++ Developers* funciona perfecte, tot i que Eclipse pot resultar una mica lent si s'instal·la en la màquina virtual.

- Si instal·les *KDevelop* des d'AppImage versió 5.6.1 no funcionarà (llibreries massa antigues).

### KDevelop

- Vés al Menú i clica *Project → Import Project...*
- Selecciona el projecte de Truc. Assegura't que estigui seleccionat CMake com a fitxer de compilació.
- Per a començar a programar amb el projecte, obre la pestanya que trobaràs a l'esquerra de tot, que posa *Projects* (en lletres girades).
- Per a executar el projecte en un terminal, has d'anar al menú *Run → Configure Launches...*. Marca *Truc* com a *Project Target*. Després, marca l'opció d'executar en un terminal extern (el terminal intern no accepta inputs de l'usuari). Omple la casella de text amb `xfce4-terminal -e %exe`.

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
