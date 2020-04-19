#Tehtävä 3 / janniojala

Tehtävän aloitus alkoi 19.4.2020 klo 13.20.

a) MarkDown. Tee tämän tehtävän raportti MarkDownina.
Helpointa on tehdä raportti GitHub-varastoon, 
jolloin md-päätteiset tiedostot muotoillaan
automaattisesti.

Käytin tehtävään Teron ohjetta(http://terokarvinen.co
m/2016/publish-your-project-with-github

Ensiksi täytyi luoda GitHubin sivuille käyttäjätunnus, johon luodaan uusi kansio jonka pystyy kloonaamaan Ubuntuun ja Ubuntusta verkkoon luotuun kansioon. Kun käyttäjätunnus on luotu loin uuden kansion, annoin sen nimeksi h3, laitoin sen publiciksi, annoin pienen selityksen ja lisäsin GNU General Public License v3.0.
Asensin tämän jälkeen git ohjelman Ubuntulle komennoilla:
	sudo apt-get update
	sudo apt-get -y install git

Ohjelman asennuksen jälkeen kerroin git oman nimeni ja sähköposti osoitteeni komennoilla:
	git config --global user.email janni.ojala@hotmail.fi
	git config --global user.name "Janni Ojala"

Jotta git muistaisi salasanasi yhden tunnin, voidaan tämä tehdä komennolla:
	git config --global credential.helper "cache --timeout=3600"

Tämän jälkeen menin takaisin githubin sivuille ja menin luomaani kansioon ja sieltä valitsin kohdan clone or download. Otin sieltä kansion URL-osoitteen ja se oli 
Sitten Ubuntun terminalissa täytyi lisätä kyseinen clone ja se lisätään komennolla:
	git clone https://github.com/janniojala/h3.git
Clonattuun kansioon pääsee komennoilla:
	cd h3/

Kun kansioon on tehty muutoksia, se pitää ottaa voimaan komennoilla:
	git add. && git commit
Tämän jälkeen halusin päivittää muutokset verkossa sijaitsevalle github kansioon ja ne tehdään komennoilla:
	git pull && git push
