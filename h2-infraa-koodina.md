# h2 Infraa koodina

-	Luin materiaalit: Karvinen 2014: Hello Salt Infra-as-Code, Salt contributors: Salt overview, ja Salt contributors: The top file.
-	Näissä tulee esille, miten käytetään Salt-ohjelmaa luodakseen koodia, miten YAML kieltä kirjoitetaan ja mikä top file on ja miten sitä käytetään.

-	Salt ohjelma käyttää sls tiedostoja suorittamalla koodia terminaalissa.
-	YAML perustuu "key: value" pareihin.
-	Top file ohjaa kaikkia muita sls-tiedostoja ja sen nimi on top koska se on hakemistossa ylimpänä.

## Hei infrakoodi

-	Aloitan tekemällä kansion /srv/salt/hello ”Tero Karvisen: Hello Salt Infra-as-code” mukaan,  ja siirryn cd komennon kautta hakemistossa kansion sisään.
-	Kansion sisälle luon esimerkkitiedoston komennolla ”$ sudoedit /srv/salt/hello/init.sls ja tarkistan että se toimii saltin kautta:
  
  <img width="1039" height="653" alt="image" src="https://github.com/user-attachments/assets/1de44e97-7752-4154-b39e-d6e7a0296e64" />
  
  <img width="1039" height="617" alt="image" src="https://github.com/user-attachments/assets/c48513d8-f5e2-4b59-9651-15003500f891" />
  
  <img width="936" height="67" alt="image" src="https://github.com/user-attachments/assets/1250ce79-baf4-4d36-8ac9-75caf7f92ec9" />
  
- Ja se toimii

## Top tiedosto

-	Teen seuraavaksi top.sls kansioon /srv/salt/ samalla tavalla, kun tein aiemman tiedoston Salt contributionsin mukaan (Salt contributions: The top file).
  
  <img width="1039" height="728" alt="image" src="https://github.com/user-attachments/assets/8f46d3cd-9f45-4bf1-8547-9f9d756a7834" />
  
  <img width="1039" height="593" alt="image" src="https://github.com/user-attachments/assets/83a3795b-a304-448f-a4ca-9e47a6b00d8c" />
  
-	Ja top.sls näyttää toimivan oikein.

## Viisikon tilafunktion ja .sls-tiedosto

-	Päätin tehdä tiedoston, joka suorittaa kaikki 5 tilaa samassa tiedostossa, joten tein /srv/salt/statefunction/init.sls tiedoston.
Käytin Rules of YAML (Saltproject.io) miten kirjoittaa komennot ja tekoälyä apuna ideoimisessa, miten voisi suorittaa kaikki viisi tilafunktiota samassa tiedostossa.

  <img width="983" height="667" alt="image" src="https://github.com/user-attachments/assets/ff9414b6-c878-4f23-9704-70d35e8b1d73" />
  <img width="958" height="334" alt="image" src="https://github.com/user-attachments/assets/2ee4bc2a-1cdd-40e4-9295-8030fa293ddb" />
  
-	Lisäsin top.sls tiedostoon vielä statefunctionin että voin suorittaa kaikki samaan aikaan.
-	Tämän jälkeen ajoin komennon sudo salt-call –local state.apply ja katson meneekö kaikki muut oikein paitsi viimeiset kaksi joiden tarkoitus on mennä pieleen testin mukaan.
  
  <img width="1039" height="715" alt="image" src="https://github.com/user-attachments/assets/92f75782-12b4-4250-a734-8e267a7894e3" />
  <img width="1039" height="640" alt="image" src="https://github.com/user-attachments/assets/59c76c26-057a-4cba-9070-3ded7f110f4a" />
  <img width="1039" height="483" alt="image" src="https://github.com/user-attachments/assets/36d202d9-b366-47fa-874e-f90f2c4cabdf" />

-	Testi onnistui odotetulla tavalla koska ensimmäiset neljä onnistui, ne minulla on virtuaalikoneellani määriteltynä ja tiedostot löytyy kansioistani ja viimeiset kaksi epäonnistui koska minulla ei ole apachea ladattuna virtuaalikoneella ja cmd.runilla ei ollut määritelty mitä sen tulisi tehdä, joten se epäonnistui. Jos haluaa että tuo kyseinen cmd komento onnistuisi niin se pitäisi määrittää minkä viestin se tulostaa, minne se tulostaa, onko tmp fileä ym.
-	Eli kaikki meni putkeen mitä pitikin.

## Lopputiivistelmä ja pohdinta

-	Tein tässä tehtävässä kaikki kohdat, yhdistin siis vain kohdan c ja d suorittamalla esimerkit yhdessä ja samassa tiedostossa.
Oppitunnin aikana sain tehtyä jo ensimmäisen /hello/init.sls tiedoston ja omalla ajalla suoritin loput tehtävät.
-	Minusta tällainen tapa koodata oli miellyttävä ja vaikeuksia ei ollut paljon. Kun tuli ongelmakohtia, jotka kaikki johtuivat kirjoitusvirheitä (ei ollut tarvetta dokumentoida kirjoitusvirheitä) tarkistin vain komentoni ja sls tiedostot uudestaan tai jos tulisi muita virheitä niin googlettaisin ja ctrl + f tai kysyn tekoälyltä mikä voisi olla pielessä koodini kanssa.
-	Päätin tehdä kaikki tilafunktiot samaan tiedostoon koska mielestäni se on nopeampaa ja editoiminen on helpompaa koska on vähemmän tiedostoja läpikäytävänä, jos tapahtuu virheitä mitä omassa testissäni ei tapahtunut.

Ja nyt sain tehtyä tehtävän myös Markdown tiedostossa :)

## Lähteet

- Karvinen 2014: Hello Salt Infra-as-Code: https://terokarvinen.com/2024/hello-salt-infra-as-code
- Salt contributors: Salt overview (Rules of YAML): https://docs.saltproject.io/salt/user-guide/en/latest/topics/overview.html#rules-of-yaml
- Salt contributors: The top file: https://docs.saltproject.io/en/latest/ref/states/top.html
- ChatGPT: https://chatgpt.com/
  <img width="857" height="488" alt="image" src="https://github.com/user-attachments/assets/dc079fc2-5061-4add-a474-65f8e3b32fea" />
  <img width="794" height="997" alt="image" src="https://github.com/user-attachments/assets/20b22a27-6b98-4840-8082-298355641e75" />





  

