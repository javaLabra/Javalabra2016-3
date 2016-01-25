# Deadline 2

### Aloita ohjelmointi

* Toteuta projektia pieninä paloina
* Aloita oleellisesta ohjelmalogiikasta, älä käyttöliittymästä tai ulkoasusta
* Lähde liikkeelle yksinkertaisesta toteutuksesta

### Clean Code

* Koodin tulisi alusta lähtien olla siistiä ja laajennettavaa
* Tutustu kurssin määrittelemiin [koodin laatuvaatimuksiin](Koodin-laatuvaatimukset.md)

### JUnit-yksikkötestit:

* Ohjelman testien tulisi alusta lähtien olla kattavia
  * Testaa mahdollisimman montaa luokkaa
  * Testaa mahdollisimman montaa metodia
  * Testaa mahdollisimman monelta kantilta
  * Huomioi [koodin laatuvaatimuksien](Koodin-laatuvaatimukset.md) alakohta *Testaus*
* **Ainakin 10 testiä valmiina**

### Dokumentaatio


### Generoi PIT-raportti
  * Katso täältä [ohjeet](Maven-ja-PIT.md#raportit) raportin generointiin
  * Laita generoitu raportti dokumentaatiokansion sisälle pit-kansioon.
  * Kannattaa myös generoida ja katsoa läpi cobertura-raportti, mutta sitä ei tarvitse lisätä dokumentaatioon.

#### README.md

* Sijaitsee projektin juuressa
* Lisää tiedostoon lyhyt tiivistelmä aihekuvausestasi
* Tee _Dokumentaatio_ -alaotsikko ja linkkaa sen alla projektisi aiheen kuvaus ja määritelmä sekä tuntikirjanpitosi
* Voit kirjoittaa linkin markdownilla esimerkiksi näin: ```[aiheen kuvaus](dokumentaatio/aiheenKuvausJaMääritelmä.md)```
* **Muista käyttää [markdownia](https://help.github.com/articles/markdown-basics/) tiedoston tyylittelyyn**
* Tulevien viikkojen dokumentaatiot, kuten rakennekuvaus ja testausdokumentaatio, tulee vastaavasti linkittää _README.md_:ssä tulevaisuudessa.

#### Luokkakaavio

* Piirrä käsin tai jollain ohjelmalla (mieluiten ohjelmalla)
  * Skannaa tai ota selkeä kuva käsinpiirretystä
* Palauta .png tai .jpg -tiedostomuodossa
* Hahmottele ensimmäinen versio ohjelmastasi
* Määrittelyvaiheen luokkakaavio
* Luokkakaavioon järjestelmän tärkeimmät luokat
* Luokkien nimet ja yhteydet riittää
* **Lisää luokkakaavio kuvana [seuraavien ohjeiden](https://daringfireball.net/projects/markdown/syntax#img) mukaisesti dokumentaatiosi aiheenKuvausJaRakenne.md tiedostoon.**

##### Piirtotyökaluja

Kurssiin soveltuvia piirtotyökaluja ovat:
* [http://yuml.me/](http://yuml.me/) luokka- ja käyttötapauskaavioihin
* [https://www.websequencediagrams.com/](https://www.websequencediagrams.com/) sekvenssikaavioihin
