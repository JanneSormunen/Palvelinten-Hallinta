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
