# Full Stack -websovelluskehitys harjoitustyö 5, 7 tai 10 op

Harjoitustyössä toteutetaan vapaavalintainen sovellus Reactilla ja/tai Nodella. Myös React Nativella toteutettu mobiilisovellus on mahdollinen.

Sovelluksen backendia ei siis ole pakko toteuttaa Nodella. Backendia ei myöskään tarvitse toteuttaa itse, valmiit rajapinnat tai palvelut kuten Firebase kelpaavat. Frontend on mahdollista tehdä myös jollain muulla järkevällä tavalla kuin Reactilla, esim. Vue.js:llä. Tällöin olisi hyvä jos sovelluksella olisi Nodella tehty backend.

Opintopistemäärä määrittyy käytettyjen työtuntien mukaan, yksi opintopiste vastaa 17.5 tuntia. 5 opintopisteen suoritukseen tarvitaan vähintään 87.5 tunnin työskentely, 7 opintopisteen suoritukseen 122.5 tunnin työskentely ja 10 opintopisteen suoritus edellyttää vähintään 175 työtuntia. Jokaista opintopistettä kohti on laskettu myös tapahtuvan 9.5 tuntia omatoimista harjoitustyössä käytettävien tekniikoiden opiskelua.

Työ arvostellaan skaalalla hyväksytty/hylätty.

Työsi voidaan hylätä suoraan mikäli et ole itse tehnyt työtäsi tai jos tuntikirjanpito ja GitHub-repositorion commit-historia eivät vastaa kohtuullisesti toisiaan. Työtunteihin lasketaan kaikki sovelluksen tekemiseen käytetty aika, eli vaikka tekisit backendin jollain muulla tekniikalla kuin Nodella, lasketaan se silti työaikaan.

Työtunteihin _ei lasketa_ kurssin asioiden kertaamiseen käytettyä aikaa.

**Hyväksytty suoritus** edellyttää, että käytetyt tunnit näkyvät myös sovelluksesi toiminnallisuuksissa ja ominaisuuksissa.
Esimerkiksi 10 opintopisteen työhön edellytetään useampaa kuin yhtä tai kahta toiminnallisuutta. Hyvä lähtökohta on esim. se, että sovelluksesi toteuttaa monipuolisia tietokantatoimintoja, eli CRUD-toiminnot (_create, read, update_ ja _delete_). Vaihtoehtoisesti sovelluksesi toteuttaa osaa (mutta ei vain yhtä) näistä monipuolisesti. Testaus ja esimerkiksi deployauksen automatisointi ja muu huomattava konfigurointi luonnollisesti lasketaan laajuuteen.

Mikäli sovelluksesi sisältää hyvin rajallisesti toimintoja, voidaan etenkin 7 ja 10 opintopisteen suorituksiin sinua pyytää täydentämään sovellustasi.

**Huomaa:** Ei riitä, että tekemäsi toiminnallisuus toimii vain omalla koneella, vaan samat ominaisuudet tulisi olla testattavissa myös osoitteessa, jossa sovelluksesi on käynnissä.

Harjoitustyö on mahdollista tehdä myös pari- tai ryhmätyönä.

Full Stack -kurssin Discord-kanava https://study.cs.helsinki.fi/discord/join/fullstack toimii myös harjoitustyön kanavana.

## Ilmoittautuminen ja aiheen hyväksyminen

Jos käytät harjoitustyössä kurssilta tuttuja tekniikoita, ei aiheen hyväksymistä tarvita. Jos käytät jotain muita tekniikoita, varmista, että aihe sopii lähettämällä emailia osoitteeseen matti.luukkainen@helsinki.fi

## Ohjeet video-tutoriaalien käyttämiseen

Video-tutoriaalit voivat olla hyödyllinen tapa oppia uusia taitoja ja ymmärtää konsepteja, erityisesti kun aloitat uuden teknologian tai kehyksen käytön. Kuitenkin full stack -kurssin projektissa on tärkeää osoittaa oma ymmärryksesi ja kurssilla oppimasi taidot. Varmistaaksesi, että projektisi heijastaa henkilökohtaisia taitojasi ja ponnistelujasi, noudata näitä ohjeita käyttäessäsi video-oppaita referenssinä:

### 1. Käytä tutoriaaleja oppimiseen, Ei suoraan kopiointiin

- **Tarkoitus:** Video-tutoriaalit tulisi nähdä oppimateriaaleina, jotka auttavat ymmärtämään konsepteja, eikä suoraan kopioitavina malleina.
- **Odotus:** Opetusvideon katsomisen jälkeen sovella oppimaasi tietoa rakentaaksesi jotain ainutlaatuista tai laajentaaksesi videon esimerkkisovellusta omilla ominaisuuksillasi.

### 2. Tee merkittäviä muutoksia

- **Omaperäisyys:** Projektisi tulisi erota merkittävästi opetusvideosta. Tämä voi sisältää muutoksia käyttöliittymään, lisättyjä ominaisuuksia, erilaista toiminnallisuutta tai eri teknologiapinon käyttöä.
- **Muutosesimerkkejä:**
  - Uusien ominaisuuksien lisääminen, joita ei käsitellä videossa (esim. käyttäjäprofiilit, ilmoitukset, hakutoiminnallisuus).
  - Erilaisten tai kehittyneempien tekniikoiden toteuttaminen (esim. API-integraatio, eri tietokannan käyttö).
  - Sovelluksen tyylin muuttaminen tai vaihtoehtoisen frontend-kehyksen käyttö.

### 3. Lisää uniikkeja ominaisuuksia

- **Mukauttaminen:** Lisää ominaisuuksia, joita ei ollut mukana opetusvideossa, esitelläksesi taitojasi. Nämä voivat olla kurssin tavoitteisiin liittyviä ominaisuuksia tai sellaisia, jotka parantavat käyttäjäkokemusta.
- **Esimerkkejä ainutlaatuisista ominaisuuksista:**
  - Sosiaalisen median sovelluksessa: Ryhmien lisääminen, chat-toiminnallisuus tai kuvan latausominaisuus.
  - Verkkokauppa-sovelluksessa: Toivelista, arvostelut tai maksuyhdyskäytävä.

### 4. Selitä erot selkeästi

- **Dokumentointi:** Projektin palautuksen yhteydessä liitä mukaan lyhyt dokumentti, jossa selität, mitkä osat sovelluksestasi olivat inspiroituneet opetusvideosta ja mitä muutoksia tai parannuksia teit.
- **Perustelu:** Kerro, miksi valitsit tehdä nämä muutokset ja kuinka ne parantavat tai erottavat projektiasi alkuperäisestä.

### 5. Mene perusasioiden yli

- **Kehittyneet ominaisuudet:** Osoittaaksesi ymmärryksesi, harkitse kehittyneiden ominaisuuksien lisäämistä, joita ei käsitelty opetusvideossa, kuten:
  - **CI/CD pipelinet:** Jatkuvan integraation ja käyttöönoton määrittäminen sovellukselle.
  - **Testaus:** Yksikkötestien, integraatiotestien tai end-to-end -testien toteuttaminen.
  - **Validointi:** Käyttäjätunnistus, datan validointi ja herkän tiedon turvallinen käsittely.

### 6. Vältä plagiointia

- **Oma työ:** Koodin kopioiminen suoraan opetusvideosta ilman muutoksia katsotaan plagioinniksi. Projektin tulee heijastaa omia ponnistelujasi ja ymmärrystäsi.
- **Lähteen mainitseminen:** Jos käytät tiettyjä koodiesimerkkejä tai ideoita videosta, varmista, että annat asianmukaisen kunnianlauseen koodikommenteissa tai dokumentaatiossa.

Noudattamalla näitä ohjeita voit käyttää video-oppaita tehokkaasti oppimisvälineenä varmistaen samalla, että projektisi heijastaa omaa luovuuttasi ja taitojasi.

## Vaatimukset palautettavalle työlle

- Projektirepositoriosi **README-tiedostosta tulee löytyä** seuraavat asiat:

  - Linkki osoitteeseen, jossa sovelluksesi on käynnissä. Expolla toteutetun React Native mobiilisovelluksen kohdalla repositoriossa tulee olla [julkinen linkki](https://docs.expo.io/versions/latest/workflow/publishing/#how-to-publish), jonka kautta sovelluksen voi käynnistää Expon mobiilisovelluksessa. Muissa tapauksissa sovitaan sovelluksen demoamisesta tapauskohtaisesti
  - Lyhyt kuvaus sovelluksestasi (mitä se tekee?) sekä jonkinlaiset käyttöohjeet (tai linkki niihin)
  - Linkki tuntikirjanpitoon. Kirjanpito oltava "heti nähtävässä" -muodossa, eli ei erikseen ladattavana excelinä. Käytä esim. markdownia (.md)
    - Riittävä kirjanpidon tarkkuus on suunnilleen [tämä](https://github.com/mluukkai/OtmTodoApp/blob/master/dokumentaatio/tuntikirjanpito.md)
    - Työaikakirjanpidosta **on myös selvittävä työtuntien yhteenlaskettu määrä**
    - Työaikakirjanpidon ja repositorion commit-historian tulee vastata toisiaan kohtuullisessa määrin. Tee siis välicommiteja!
    - Pari- tai ryhmätöissä jokaisen on pidettävä omaa työaikakirjanpitoa
  - Jos työsi on useassa repositoriossa, linkit muihin repositorioihin

- Repositoriosi ja koodikantasi on oltava edustuskelpoisessa tilassa. Ei poiskommentoitua tai muuten käyttämätöntä koodia.

Jos ylläolevat edellytykset eivät täyty pyytäessäsi kurssisuoritusta, sinua tullaan joka tapauksessa pyytämään täydentämään ne ennen tarkastuksen etenemistä.

Miksi?

Repositoriosi on käyntikorttisi, eritoten alan työnhaussa. Rekrytoijat eivät arvosta, mikäli joutuvat penkomaan sotkuista repoa saadakseen kuvan osaamisestasi ja luomuksestasi. (Eivät myöskään projektin tarkastajat.) Monet rekrytoijat eivät edes vaivaudu vaan siirtyvät eteenpäin. On suotavaa harjoittaa hyviä käytänteitä aina kun mahdollista.

## Työn valmistuminen ja arvostelu

Kun työsi on valmis arvosteltavaksi, **tee KAIKKI seuraavista askeleista**

(1) Ilmoittaudu avoimen yliopiston kautta oikean kokoiseen kurssiin :

- FS harjoitustyö (5 op): [https://www.avoin.helsinki.fi/palvelut/esittely.aspx?s=otm-213e3838-c757-4839-bdb9-69dc7e23571c](https://www.avoin.helsinki.fi/palvelut/esittely.aspx?s=otm-7b7d5cc3-2bb5-435d-8c33-752a51238f00)
- FS harjoitustyö (7 op): https://www.avoin.helsinki.fi/palvelut/esittely.aspx?s=otm-5b229b06-d94e-483d-becf-e50c0f30ac47
- FS harjoitustyö (10 op): [https://www.avoin.helsinki.fi/palvelut/esittely.aspx?s=otm-0b8aaeb0-d19b-43ab-9fc7-496f027776c4](https://www.avoin.helsinki.fi/palvelut/esittely.aspx?s=otm-37990742-5372-41ee-9bc9-a7f3795184b3)

(2) Täytä tämä lomake https://docs.google.com/forms/d/e/1FAIpQLSfJxtLyWugefPSPHynZcZnrsNt4IGqhpr5M7dF5jgZZ6ASqsQ/viewform

(3) lähetä email osoitteeseen matti.luukkainen@helsinki.fi Kerro emailissa opiskelijanumerosi sekä GitHub-tunnuksesi

**HUOM: työtä ei arvostella jos KAIKKIA kolmea vaihetta ei ole tehty**

Jos repositorio on privaatti, lisää käyttäjät mluukkai, outisa ja vejol collaboraattoriksi.

Arvostelussa kestää noin 4 viikkoa. Saat arvosteluun liittyvän koodikatselmoinnin projektiisi GitHub-issuena.
