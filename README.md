# CZADSB Raspberry Pi 4 Ansible

## Popis instalace

### Predpoklady
 - Raspberry Pi 3 (nebo novejsi)
 - Debian Buster Lite release minimalne 2020 02 13
 - Funkcni SSH pripojeni
 - Ansible 2.9+

#### Instalace pomoci ansible z Raspberry Pi
Pokud nemate zadny jiny linux stroj, kde muze bezet ansible, je mozny delat to primo z raspberry pi.
Pak je nutne nainstalovat balicky `apt-get install ansible sshpass`. Nasledne v local.ini zapisujete hosta jako `localhost`

### Instalace zakladniho systemu
 - predpoklada se Rpi s novym cistym image a funkcnim SSH
 - do souboru local.ini doplne IP adresu(y) zarizeni, ktere chcete instalovat
 - spustte instalaci zakladniho systemu `ansible-playbook --ask-pass -i local.ini base_install.yml`
 - po vyzvani zadejte heslo (pravdepodobne vychozi pro uzivatele `pi`)


### Priprava balicku dump1090-fa
 - specialni role pro tvorbu balicku ze zdrojovych kodu
 - nemusite spoustet na vsech prijimacich, staci si pripravit deb balicek na jednom
 - urcena pouze pokud si nechcete prijimac zbytecne zaplacavat balickama pro build
 - spustte build `ansible-playbook --ask-pass -i local.ini build_dump1090.yml`

### Instalace prijimace
 - TODO
