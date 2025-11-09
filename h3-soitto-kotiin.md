# H3 Soitto Kotiin.

## Lue ja tiivistä

-	Luin läpi Karvinen 2021: Two Machine Virtual Network, Karvinen 2018: Salt Quickstart ja Karvinen 2023: Salt Vagrant.
-	Ensimmäisessä tekstissä tuli esille, miten ladataan Vagrant, miten sillä luodaan uusia virtuaalikoneita, ohjataan niitä, poistutaan ja tuhotaan Vagrant virtuaaliyhteyden.
-	Salt Quickstart-tekstissä lukee miten ladataan Salt master ja Salt slave ja miten kumpaakin käytetään ohjaamalla niitä komennoilla.
-	Salt Vagrant tekstissä kerrotaan miten pyörittää useita virtuaalikoneita vagrantilla, miten ohjata orjia, miten kerätä informaatiota ja miten suorittaa komentoja idempotenttina. Infraa koodina osuutta käytetään myös tarkistamalla, että orjat toimivat.

## Hello Vagrant!

- Vagrant asennettu komennolla $ sudo apt-get install vagrant:
<img width="711" height="59" alt="image" src="https://github.com/user-attachments/assets/508bdd49-3d34-4758-9bd1-3092feb0c4d3" />

- VirtualBoxia ei löydy ollenkaan asennettavana, yritin googlettaa minkä takia ei löydy Debian 13 Trixielle.
<img width="755" height="306" alt="image" src="https://github.com/user-attachments/assets/ca393b1f-3df7-43d1-a06b-0aa6deccff87" />

- Sain selville miten lataan Virtualboxin Debian 13 Trixielle noudattamalla osoitteessa: https://linuxiac.com/how-to-install-virtualbox-on-debian-13-trixie löytyviä ohjeita.
<img width="1002" height="340" alt="image" src="https://github.com/user-attachments/assets/89359671-7dc7-4dfe-9dc7-5481d0bc8628" />
<img width="932" height="181" alt="image" src="https://github.com/user-attachments/assets/ed3770e8-bf69-49ea-8fb2-7965a3a42793" />
<img width="780" height="78" alt="image" src="https://github.com/user-attachments/assets/771db357-ed2b-4ae3-914d-e731e7df7801" />

- Oli kieltämättä pientä säätöä saada virtualbox Debian 13, mutta nyt se näyttää olevan joten voin jatkaa testaamalla Vagrantia.


- Teen Vagrantfilen

<img width="583" height="37" alt="image" src="https://github.com/user-attachments/assets/e6d5709a-259e-4eb9-83a5-cf625395d8fe" />
<img width="859" height="485" alt="image" src="https://github.com/user-attachments/assets/8a6796f9-e3bc-4e46-8491-5d4c934546dd" />



- Testaan Vagrantfileä

<img width="795" height="267" alt="image" src="https://github.com/user-attachments/assets/42803b73-d413-46f1-ad6d-6c3b2a0b78f3" />

- Jotain ihmeellistä tapahtuu koska minulla on Vagrant version 2.7.3 minkä internetin mukaan pitäisi supporttaa VirtualBox 7.2 versiota. Mutta error messagen mukaan se ei olisi näin.

## Vagrant virtuaalikone

<img width="728" height="38" alt="image" src="https://github.com/user-attachments/assets/2ab1f3d6-9411-4ff9-8088-aaf51baff57d" />

- Ja sen takia tämä ei myös toimi. Jos en saa Virtuaalikonetta auki Vagrantilla niin en oikein voi päästä tästä eteenpäin. Tästä lähtien kerron mitä tekisin jos pääsisin tästä eteenpäin. Internet ja tekoäly ei antanut minulle mitään järkevää.

<img width="894" height="192" alt="image" src="https://github.com/user-attachments/assets/b82c6f5c-d3bb-4a73-870f-3a07e0d30542" />

## Herra-orja verkossa.

- Aloitan lataamalla micron.

<img width="793" height="135" alt="image" src="https://github.com/user-attachments/assets/8fd6ad0c-3e1f-4bda-96e2-3ffc14d0d578" />

- Jatkan tekemällä uuden directoryn micro filelle ja sen jälkeen $ micro Vagrantfile.

<img width="867" height="761" alt="image" src="https://github.com/user-attachments/assets/3e9934e2-4def-4412-a6b7-82b40911a638" />

- Tein micro Vagrantfilen mutta sama ongelma on edelleen.

<img width="743" height="572" alt="image" src="https://github.com/user-attachments/assets/6e4de9dc-73e6-4d1a-8338-a0c6930c062d" />


## Kokeile vähintään kahta tilaa verkon yli.

- Ei ole paljoa mitä voin tässä osuudessa tehdä, luin Tero Karvinen 2023: Salt-Vagrant ohjeet läpi ja testasin pari komentoa, niistä ei tietenkään tullut mitään vastausta koska virtualbox temppuilee.

<img width="772" height="516" alt="image" src="https://github.com/user-attachments/assets/68f30857-39cd-435c-971b-14e55d7f14d0" />

## Lopputiiviste ja pohdinta.

- Tämä oli ensimmäinen tehtävä mihin oikeasti jäin jumiin johonkin kohtaan useammaksi tunniksi. Menin varmuuden vuoksi testaamaan että olisiko ongelmana se että yritän väkisin pyörittää tätä Debian 13 Trixiellä, mutta latasin Debian 12 Bookwormin ja sama ongelma oli sielläkin että Vagrant ei osannut käyttää virtualboxia. Isänpäivänä loppui aika joten tuumailen mikä voisi olla ongelmana myöhemmin.
- Harmittaa koska olisin mieluiten tehnyt tehtävän loppuun, jos jollakin olisi ideoita mikä tässä mättää niin voi jättää kommentin.

## Lähteet:

- Linuxiac 2025. How to Install Virtualbox on Debian 13 Trixie: https://linuxiac.com/how-to-install-virtualbox-on-debian-13-trixie
- Karvinen 2021. Two Machine Virtual Network With Debian 11 Bullseye and Vagrant: https://terokarvinen.com/2021/two-machine-virtual-network-with-debian-11-bullseye-and-vagrant
- Karvinen 2018. Salt Quickstart – Salt Stack Master and Slave on Ubuntu Linux: https://terokarvinen.com/2018/salt-quickstart-salt-stack-master-and-slave-on-ubuntu-linux/?fromSearch=salt%20quickstart%20salt%20stack%20master%20and%20slave%20on%20ubuntu%20linux
- Karvinen 2023. Salt Vagrant - automatically provision one master and two slaves: https://terokarvinen.com/2023/salt-vagrant/#infra-as-code---your-wishes-as-a-text-file
