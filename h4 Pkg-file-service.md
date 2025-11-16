# h4 Pkg-file-service.

## Ympäristö:

- Windows 11
- CPU: AMD Ryzen 9 5700X 12-Core Processor
- RAM: 32GB
- GPU: Nvidia Geforce RTX 3070 8GB
- Disc size 2TB

## Tiivistelmä - Pkg-File-Service – Control Daemons with Salt – Change SSH Server Port.

- Voit luoda suuren määrän daemoneita käyttämällä configurement management systeemiä.
- Setuppaa master-slave ympäristö
- Luo SSH-tila
- Liitä tila orjiin
- Muista configuroida portti 8888.

## SSHouto. Lisää uusi portti, jossa SSHd kuuntelee.

- Aloitan tekemällä sshd.sls tiedoston /srv/salt/ kansioon.
<img width="984" height="317" alt="image" src="https://github.com/user-attachments/assets/af0e7067-aa7c-4a20-8ded-1f4f85fcb036" />

- Seuraavaksi luon /srv/salt/ kansioon sshd_config tiedoston.
<img width="726" height="576" alt="image" src="https://github.com/user-attachments/assets/1843de7c-e8b2-40ca-91a6-6a061a4cd0f9" />

- Ja apply komennolla lisään sshd
<img width="793" height="646" alt="image" src="https://github.com/user-attachments/assets/26ad2955-1ca5-401c-9c9c-de3a663d55d9" />

- Minulla meni service running pieleen jotenkin, yritän korjata asian.
- Ja virhe löytyi melkein heti, oli vain kirjoitusvirhe unohtui / ennen /etc/ssh/..
<img width="763" height="647" alt="image" src="https://github.com/user-attachments/assets/3f384bb4-f73c-4c62-92f4-33d8404cc489" />

- Seuraavaksi latasin netcatin jolla voin suorittaa nc komentoja.
<img width="1039" height="35" alt="image" src="https://github.com/user-attachments/assets/13192493-5ead-4d79-bddd-128bda667bea" />

- Ja kirjoitan komennon tarkistaakseni että asiat toimii.
<img width="872" height="43" alt="image" src="https://github.com/user-attachments/assets/52b56865-a954-4b4f-8bb7-990e3487398c" />

- Ja tuli taas ongelma, yritän selvittää mistä tämä ongelma johtuu.
<img width="532" height="58" alt="image" src="https://github.com/user-attachments/assets/691ccab8-5bca-4d0b-aad7-30bac854948d" />

- Katson jos olisi palomuurista kiinni.
<img width="873" height="97" alt="image" src="https://github.com/user-attachments/assets/a25bf3ac-3a61-4856-addf-7520a09d594a" />

- Ei vieläkään.
<img width="905" height="95" alt="image" src="https://github.com/user-attachments/assets/960f355e-2ec5-442f-aae3-a5262bc61a48" />
<img width="902" height="345" alt="image" src="https://github.com/user-attachments/assets/4beda463-0b39-4c5d-9fea-282c19a4d892" />

- Yritän restarttaa sshd:n jos se tunnistaisi 8888 portin 22 portin sijasta.
<img width="906" height="116" alt="image" src="https://github.com/user-attachments/assets/aa3182aa-03c5-4d38-9f6e-e0ea9141a99d" />

- Ja se oli näköjään vain restartista kiinni.

- Yritän nyt uudestaan katsoa kuunteleeko sshd.
<img width="715" height="39" alt="image" src="https://github.com/user-attachments/assets/cbe860c7-4770-4831-b09c-5cf1b486c5be" />

- Onnistui!

## Lopputiiviste ja pohdinta.

- Tällä kertaa sain kaiken toimimaan ja oli kiva tehtävä. Välillä tulee kirjoitusvirheitä koska tykkään kertauksen takia kirjoittaa itse että komennot ja konfiguraatiot jää mieleen. Olen vielä aloittelija Linuxin käytössä mutta pikkuhiljaa alan ymmärtämään kokonaisuuksia jo ja jotkut komennot osaan jo ulkoa.

## Lähteet.

- Karvinen 2018: Pkg-File-Service – Control Daemons with Salt – Change SSH Server Port: https://terokarvinen.com/2018/04/03/pkg-file-service-control-daemons-with-salt-change-ssh-server-port/?fromSearch=karvinen%20salt%20ssh






