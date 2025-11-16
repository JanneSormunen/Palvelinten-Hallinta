# h4 Pkg-file-service.

## Ympäristö:

- Windows 11
- CPU: AMD Ryzen 9 5700X 12-Core Processor
- RAM: 32GB
- GPU: Nvidia Geforce RTX 3070 8GB
- Disc size 2TB

## Tiivistelmä - Pkg-File-Service – Control Daemons with Salt – Change SSH Server Port

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

- Seuraavaksi latasin netcatin
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






