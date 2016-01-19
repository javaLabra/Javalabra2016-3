# Deadline 6 + lopullinen palautus

### JavaDoc
* Kaikki luokat, attribuutit ja julkiset metodit on dokumentoitu
* Javadocia **ei** tarvitse kirjoittaa...
  * Testeille
  * @Override -metodeille
  * Yksityisille (private) metodeille
  * Gettereille ja Settereille, jotka eivät tee mitään ylimääräistä
  * Aivan kaikille käyttöliittymäluokkien metodeille

### Kirjoita rakennekuvaus
* Kirjoita lyhyt, esimerkiksi muutaman tekstikappaleen kuvaus ohjelmasi rakenteesta
* Toisin sanoen: Avaa luokkakaaviotasi sanallisesti
* Tallenna kuvaus omaan tiedostoonsa tai aihemäärittelyn jatkoksi

### Clean-code
* Ohjelmasi tulisi noudattaa [koodin laatuvaatimuksia](Koodin-laatuvaatimukset.md) mahdollisimman hyvin

### Luo ajettava jar-tiedosto
* Shade-pluginin pitäisi paketoida mukaan ohjelmasi tarvitsemat riippuvuudet, jos sellaisia on.
* Lisää pom.xml-tiedostoosi uusi plugin:

```
<build>
    <plugins> 
        <!-- ... -->
        <plugin>
            <groupId>org.apache.maven.plugins</groupId>
            <artifactId>maven-shade-plugin</artifactId>
            <version>2.4.3</version>
            <executions>
                <execution>
                    <phase>package</phase>
                    <goals>
                        <goal>shade</goal>
                    </goals>
                    <configuration>
                        <transformers>
                            <transformer implementation="org.apache.maven.plugins.shade.resource.ManifestResourceTransformer">
                                <mainClass>PÄÄLUOKAN_SIJAINTI</mainClass><!-- Esimerkiksi muotoa "fi.omanimi.superprojekti" -->
                            </transformer>
                        </transformers>
                    </configuration>
                </execution>
            </executions>
        </plugin>
    </plugins>
</build>
```

* Korvaa javalabra.Main omalla pääluokallasi (siis haluamallasi `main`-metodin toteuttavalla luokalla).
* Valitse Netbeansista "Clean & Build". Komentoriviltä paketin saa luotua komennolla `mvn package`. Jar-tiedosto luodaan projektikansiosi `target`-kansion sisään.
* Kokeile .jar -tiedoston toimivuus. Komentoriviltä jar-tiedosto voidaan ajaa komennolla `java -jar paketti.jar`.
   * Jos ohjelma ei toimi, tarkista erityisesti ohjelmasi käyttämät tiedostopolut - ne ovat suhteellisia .jar-tiedoston sijaintiin
* Kokeile ajaa ohjelmaasi myös jollain muulla kuin omalla koneellasi. Esimerkiksi natiivikirjastojen kanssa paketointi saattaa vaatia ylimääräistä säätöä - näissä tapauksissa esimerkiksi kirjaston dokumentaatio saattaa kertoa sopivimman paketointitavan.

### Kirjoita käyttöohjeet
* Ajattele käyttäjää, joka ei ole käyttänyt ohjelmaasi
* Jos ohjelmasi on yksinkertainen käyttää, ei käyttöohjeidenkaan tarvitse olla pitkät

### Generoi Checkstyle-raportti uudestaan
* Generoi uusi Checkstyle raportti
* Lisää generoitu raportti dokumentaatiokansioon

### Generoi PIT-raportti uudestaan
* Generoi uudestaan PIT-raportti
* Lisää uusi generoitu raportti dokumentaatioon

# Lopulliseen palautukseen (Deadline 6 jälkeen)

### Tarkista ohjelmasi valmius
* Ohjelma toimii ja on valmis
* JUnit-testejä mahdollisimman kattavasti
* Kaaviot, Javadoc ja muu dokumentointi ajantasalla ja vastaa vaatimuksia

###  Kirjoita testausdokumentaatio
* **Vapaaehtoinen**
* Testausdokumentaatio korvaa yksikkötestauksen puutteita maksimissaan +2 pistettä
* Kirjoita esimerkiksi seuraavista
  * Mitä et testannut automaattisesti?
  * Miten näitä on testattu käsin?
  * Raportoi myös mahdolliset bugit

### Varmista kaikki vielä kerran
* Tarkista, että kaikki dokumentaatio on .md, .png tai .jpg -tiedostomuodoissa
* Puske kaikki vaadittava repositorioon ennen deadlinea, viimeisin ennen deadlinea tehty commit arvostellaan
* Tarkista selaimesta, että kaikki on varmasti Githubissa
* Tarkista, että ohjelma toimii varmasti laitoksen koneilla
* **Muistilistana toimii [arvosteluperusteet](Arvosteluperusteet.md)**
