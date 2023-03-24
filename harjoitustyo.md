# Full Stack -websovelluskehitys harjoitustyö 5, 7 tai 10 op

> Tätä harjoitustyötä *ei lasketa* aineopintojen harjoitustyöksi, joita vaaditaan tietojenkäsittelytieteen pääaineopiskelijoilta 2 kappaletta, eli et voi korvata Full Stack -harjoitustyöllä esim. tiralabraa.

Harjoitustyössä toteutetaan vapaavalintainen sovellus Reactilla ja/tai Nodella. Myös React Nativella toteutettu mobiilisovellus on mahdollinen.

Sovelluksen backendia ei siis ole pakko toteuttaa Nodella. Backendia ei myöskään tarvitse toteuttaa itse, valmiit rajapinnat tai palvelut kuten Firebase kelpaavat. Frontend on mahdollista tehdä myös jollain muulla järkevällä tavalla kuin Reactilla, esim. Vue.js:llä. Tällöin olisi hyvä jos sovelluksella olisi Nodella tehty backend.

Opintopistemäärä määrittyy käytettyjen työtuntien mukaan, yksi opintopiste vastaa 17.5 tuntia. 5 opintopisteen suoritukseen tarvitaan vähintään 87.5 tunnin työskentely, 7 opintopisteen suritukseen 122.5 tunnin työskentely ja 10 opintopisteen suoritus edellyttää vähintään 175 työtuntia. 

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

## Vaatimukset palautettavalle työlle

- Projektirepositoriosi README-tiedosta **tulee löytyä** seuraavat asiat:
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

Repositoriosi on käynttikorttisi, eritoten alan työnhaussa. Rekrytoijat eivät arvosta, mikäli joutuvat penkomaan sotkuista repoa saadakseen kuvan osaamisestasi ja luomuksestasi. (Eivät myöskään projektin tarkastajat.) Monet rekrytoijat eivät edes vaivaudu vaan siirtyvät eteenpäin. On suotavaa harjoittaa hyviä käytänteitä aina kun mahdollista.

## Työn valmistuminen ja arvostelu

Kun työsi on valmis arvosteltavaksi, **tee KAIKKI seuraavista askeleista**

(1) Ilmoittaudu avoimen yliopiston kautta oikean kokoiseen kurssiin:
- FS harjoitustyö (5 op): [https://www.avoin.helsinki.fi/palvelut/esittely.aspx?s=otm-cdc701c5-f817-41cc-8b47-ad2cb690c546](https://www.avoin.helsinki.fi/palvelut/esittely.aspx?s=otm-ba589ba3-603f-4e56-bc88-654494549567)
- FS harjoitustyö (7 op): [https://www.avoin.helsinki.fi/palvelut/esittely.aspx?s=otm-a1b99420-600c-42ea-81ab-7bdad3a8800d](https://www.avoin.helsinki.fi/palvelut/esittely.aspx?s=otm-d9404272-3391-4315-8036-ec48abb9192f)
- FS harjoitustyö (10 op): [https://www.avoin.helsinki.fi/palvelut/esittely.aspx?s=otm-67e986ac-78ad-4e2b-aef7-e01cc7f4ec3c](https://www.avoin.helsinki.fi/palvelut/esittely.aspx?s=otm-85bb770f-ef2f-4bde-984d-5c753bf6a442)

(2) Täytä tämä lomake https://docs.google.com/forms/d/e/1FAIpQLSfJxtLyWugefPSPHynZcZnrsNt4IGqhpr5M7dF5jgZZ6ASqsQ/viewform

(3) lähetä email osoitteeseen matti.luukkainen@helsinki.fi Kerro emailissa opiskelijanumerosi sekä GitHub-tunnuksesi

**HUOM: työtä ei arvostella jos KAIKKIA kolmea vaihetta ei ole tehty**

Jos repositorio on privaatti lisää käyttäjät mluukkai, outisa ja sinikala collaboraattoriksi.

Arvostelussa kestää noin 4 viikkoa. Saat arvosteluun liittyvän koodikatselmoinnin projektiisi GitHub-issuena
