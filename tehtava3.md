**Tehtävä 3 / janniojala**

Tehtävän aloitus alkoi 19.4.2020 klo 13.20.

**a) MarkDown. Tee tämän tehtävän raportti MarkDownina.Helpointa on tehdä raportti GitHub-varastoon, jolloin md-päätteiset tiedostot muotoillaan automaattisesti.**

Käytin tehtävään Teron ohjetta(http://terokarvinen.co
m/2016/publish-your-project-with-github

Ensiksi täytyi luoda GitHubin sivuille käyttäjätunnus, johon luodaan uusi kansio jonka pystyy kloonaamaan Ubuntuun ja Ubuntusta verkkoon luotuun kansioon. Kun käyttäjätunnus on luotu loin uuden kansion, annoin sen nimeksi h3, laitoin sen publiciksi, annoin pienen selityksen ja lisäsin GNU General Public License v3.0.
Asensin tämän jälkeen git ohjelman Ubuntulle komennoilla:
    *sudo apt-get update*
    *sudo apt-get -y install git*

Ohjelman asennuksen jälkeen kerroin git oman nimeni ja sähköposti osoitteeni komennoilla:
    *git config --global user.email janni.ojala@hotmail.fi*
    *git config --global user.name "Janni Ojala"*

Jotta git muistaisi salasanasi yhden tunnin, voidaan tämä tehdä komennolla:
    *git config --global credential.helper "cache --timeout=3600"*

Tämän jälkeen menin takaisin githubin sivuille ja menin luomaani kansioon ja sieltä valitsin kohdan clone or download. Otin sieltä kansion URL-osoitteen ja se oli 
Sitten Ubuntun terminalissa täytyi lisätä kyseinen clone ja se lisätään komennolla:
    *git clone https://github.com/janniojala/h3.git*
Clonattuun kansioon pääsee komennoilla:
    *cd h3/*

Kun kansioon on tehty muutoksia, se pitää ottaa voimaan komennoilla:
    *git add. && git commit*
Tämän jälkeen halusin päivittää muutokset verkossa sijaitsevalle github kansioon ja ne tehdään komennoilla:
    *git pull && git push*

**b) Näytä omalla git-varastollasi esimerkit komennoista ‘git log’, ‘git diff’ ja ‘git blame’. Selitä tulokset.**

Aloitin komennolla git log. Se kertoo mitä git:llä on tehty. Alapuolella git log tulos:

commit 0237ebf0e01670ae19a78f596ee3ea3cf8c05b90 (HEAD -> master, origin/master, origin/HEAD)
Author: Janni Ojala <janni.ojala@hotmail.fi>
Date:   Sun Apr 19 13:48:06 2020 +0300

    Add file

commit 605e570773c826a500315b953c659fc9f5345ae8
Author: janniojala <63713350+janniojala@users.noreply.github.com>
Date:   Wed Apr 15 16:47:18 2020 +0300

    Initial commit

Se kertoo tarkemmin,commit numeron,  kuka muutoksia on tehnyt(Janni Ojala <janni.ojala@hotmail.fi>, milloin niitä on tehty(Sun APr 19 13:48:06 2020 +0300) ja mikä commit on tehty(Add file). Alapuolella on toinen samanlainen, mutta käyttäjä on ollut eri, päivä eri ja eri commit tehty.

Seuraavaksi oli testasin komentoja git diff. Diff kertoo muutokset mitä tiedostoissa on tehty. + mikäli rivejä on lisätty ja - mikäli rivejä on poistettu. Alapuolella oma tulokseni git diffistä.

diff --git a/harjoitus3.md b/harjoitus3.md
index 42bcec3..374b631 100644
--- a/harjoitus3.md
+++ b/harjoitus3.md
@@ -32,3 +32,24 @@ Kun kansioon on tehty muutoksia, se pitää ottaa voimaan komennoilla:
        git add. && git commit
 Tämän jälkeen halusin päivittää muutokset verkossa sijaitsevalle github kansioon ja ne tehdään komennoilla:
        git pull && git push
+
+b) Näytä omalla git-varastollasi esimerkit komennoista ‘git log’, ‘git diff’ ja ‘git blame’. Selitä tulokset.
+
+Aloitin komennolla git log. Se kertoo mitä git:llä on tehty. Alapuolella git log tulos:
+
+commit 0237ebf0e01670ae19a78f596ee3ea3cf8c05b90 (HEAD -> master, origin/master, origin/HEAD)
+Author: Janni Ojala <janni.ojala@hotmail.fi>
+Date:   Sun Apr 19 13:48:06 2020 +0300
+
+    Add file

Viimeisenä oli vuorossa git blame. Git blame selvittää tiedostossa, kuka on tehnyt muutoksia. Itse käytin Git blameä tähän tiedostoon komennolla:
    *git blame harjoitus3.md*

Ja vastaus oli tämä:

0237ebf0 (Janni Ojala       2020-04-19 13:48:06 +0300  1) #Tehtävä 3 / janniojala
0237ebf0 (Janni Ojala       2020-04-19 13:48:06 +0300  2) 
0237ebf0 (Janni Ojala       2020-04-19 13:48:06 +0300  3) Tehtävän aloitus alkoi 19.4.2020 klo 13.20.
0237ebf0 (Janni Ojala       2020-04-19 13:48:06 +0300  4) 
0237ebf0 (Janni Ojala       2020-04-19 13:48:06 +0300  5) a) MarkDown. Tee tämän tehtävän raportti MarkDownina.
0237ebf0 (Janni Ojala       2020-04-19 13:48:06 +0300  6) Helpointa on tehdä raportti GitHub-varastoon, 
0237ebf0 (Janni Ojala       2020-04-19 13:48:06 +0300  7) jolloin md-päätteiset tiedostot muotoillaan
0237ebf0 (Janni Ojala       2020-04-19 13:48:06 +0300  8) automaattisesti.
0237ebf0 (Janni Ojala       2020-04-19 13:48:06 +0300  9) 
0237ebf0 (Janni Ojala       2020-04-19 13:48:06 +0300 10) Käytin tehtävään Teron ohjetta(http://terokarvinen.co
0237ebf0 (Janni Ojala       2020-04-19 13:48:06 +0300 11) m/2016/publish-your-project-with-github
:

Siinä näkyy, että minä olen tehnyt tiedostoon muutoksia noihin aikoihin.

**c)Tee tyhmä muutos gittiin, älä tee commit:tia. Tuhoa huonot muutokset ‘git reset –hard’. Huomaa, että tässä toiminnossa ei ole peruutusnappia.**

Ennen tyhmän muutoksen tekemistä päivitin tekemäni vanhat muutokset komennolla:

   *git add . && git commit; git pull && git push*
Tämän jälkeen tein tyhmän muutokset komennolla:
    *git config  --global user.name "Tyhma"*
Tämän jälkeen tein komennon git add ., jotta muutos lisättäisiin. Jätin kuitenkin git commitin tekemättä. 
Kun tyhmä muutos oli lisätty, oli aika resetoida edelliseen commit -tilaan komennolla:

​    *reset --hard*
Komennosta tuli tälläinen tulos, joka kertoi että on palattu edelliseen commit -tilanteeseen:
HEAD is now at dd338c6 Add files

**d) Tee uusi salt-moduli. Voit asentaa ja konfiguroida minkä vain uuden ohjelman: demonin, työpöytäohjelman tai komentokehotteesta toimivan ohjelman.**

Valitsin asennettavaksi ohjelmaksi neofetch, joka tekee sys-tiedostoja ja siitä voi seurata niiden tietoja.
Asensin ohjelman ensiksi käsin komennoilla:
    *sudo apt-get update*
    *sudo apt-get install neofetch*

Tämän jälkeen menin polkuun /etc/neofetch ja muokkasin siellä ollutta config.conf tiedostoa.
Muokkasin config.conf tiedostosta kohtaa #info "GPU Driver" gpu_driver  # Linux/macOS only ja otin siitä # pois, jotta kyseinen sääntö tuli voimaan. 

Kun tämä oli tehty kopioin sen /srv/salt kansiooni komennolla:
    *sudo cp /etc/neofetch/config.conf /srv/salt*

Sitten poistin ohjelman komennolla:
    *sudo apt-get purge neofetch*

Kun ohjelma poistettu. Menin /srv/salt polkuu ja loin neofetch.sls -tilan ja muokkasin sen tämän näköiseksi:

neofetch:
  pkg.installed

/etc/neofetch/config.conf:
  file.managed:
    - source: salt://config.conf  

neofetchservice:
  service.running:
    - name: neofetch
    - watch:
      - file: /etc/neofetch/config.conf 

Tallensin tilan ja testasin sen läpi menevyyttä komennolla:
    sudo salt '*' state.apply neofetch

Kaikki muut toiminnot menivät läpi, mutta service.running ei. En saanut sitä toimimaan. Yritin etsiä -tilasta kirjoitusvirheitä ja saada sitä toimimaan. Testasin myös, että toimivatko vanhat tilani edelleen. Apache toimi normaalisti. Asensin neofetchin vielä käsin toiselle virtuaalikoneelle, jossa sitä ei ole ollut ja testasin asennuksen jälkeen komennolla *sudo systemctl status neofetch*, eikä service ollut. Mietinkin, että luoko kyseinen ohjelma service toimintaa ollenkaan?

          ID: neofetch
    Function: pkg.installed
      Result: True
     Comment: All specified packages are already installed
     Started: 16:22:20.948399
    Duration: 854.556 ms
     Changes:   
----------
          ID: /etc/neofetch/config.conf
    Function: file.managed
      Result: True
     Comment: File /etc/neofetch/config.conf is in the correct state
     Started: 16:22:21.805648
    Duration: 14.822 ms
     Changes:
----------
          ID: neofetch.service
    Function: service.running
        Name: neofetch
      Result: False
     Comment: The named service neofetch is not available
     Started: 15:51:20.662875
    Duration: 19.941 ms
     Changes: 

Muuten muutokset onnistuivat ja testasin ohjelmaa komennolla:
    neofetch
Vastauksena tuli tälläinen:
            .-/+oossssoo+/-.               janni@janni-VirtualBox 
        `:+ssssssssssssssssss+:`           ---------------------- 
      -+ssssssssssssssssssyyssss+-         OS: Ubuntu 18.04.4 LTS x86_64 
    .ossssssssssssssssssdMMMNysssso.       Host: VirtualBox 1.2 
   /ssssssssssshdmmNNmmyNMMMMhssssss/      Kernel: 5.3.0-46-generic 
  +ssssssssshmydMMMMMMMNddddyssssssss+     Uptime: 3 hours, 16 mins 
 /sssssssshNMMMyhhyyyyhmNMMMNhssssssss/    Packages: 1721 
.ssssssssdMMMNhsssssssssshNMMMdssssssss.   Shell: bash 4.4.20 
+sssshhhyNMMNyssssssssssssyNMMMysssssss+   Resolution: 800x600 
ossyNMMMNyMMhsssssssssssssshmmmhssssssso   DE: Xfce 
ossyNMMMNyMMhsssssssssssssshmmmhssssssso   WM: Xfwm4 
+sssshhhyNMMNyssssssssssssyNMMMysssssss+   WM Theme: Greybird 
.ssssssssdMMMNhsssssssssshNMMMdssssssss.   Theme: Greybird [GTK2/3] 
 /sssssssshNMMMyhhyyyyhdNMMMNhssssssss/    Icons: Elementary-xfce-darker [GTK2/3] 
  +sssssssssdmydMMMMMMMMddddyssssssss+     Terminal: xfce4-terminal 
   /ssssssssssshdmNNNNmyNMMMMhssssss/      Terminal Font: Monospace 12 
    .ossssssssssssssssssdMMMNysssso.       CPU: AMD Ryzen 5 2500U with Radeon Vega Mobile Gfx (1) @ 1.996GHz 
      -+sssssssssssssssssyyyssss+-         GPU: VMware SVGA II Adapter 
        `:+ssssssssssssssssss+:`           Memory: 1025MiB / 1987MiB 
            .-/+oossssoo+/-.               GPU Driver: vmwgfx, vmwgfx 

​                                                                   

Lopetin tehtävien tekemisen 19.4.2020 klo 16.20 ja aikaa meni yhteensä 3 tuntia.

**Lähteet:**

Publish Your Project With GitHub
http://terokarvinen.com/2016/publish-your-project-with-github

