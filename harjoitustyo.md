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

Repositoriosi on käyntikorttisi, eritoten alan työnhaussa. Rekrytoijat eivät arvosta, mikäli joutuvat penkomaan sotkuista repoa saadakseen kuvan osaamisestasi ja luomuksestasi. (Eivät myöskään projektin tarkastajat.) Monet rekrytoijat eivät edes vaivaudu vaan siirtyvät eteenpäin. On suotavaa harjoittaa hyviä käytänteitä aina kun mahdollista.

## Työn valmistuminen ja arvostelu

Kun työsi on valmis arvosteltavaksi, **tee KAIKKI seuraavista askeleista**

(1) Ilmoittaudu avoimen yliopiston kautta oikean kokoiseen kurssiin :
- FS harjoitustyö (5 op): https://www.avoin.helsinki.fi/palvelut/esittely.aspx?s=otm-213e3838-c757-4839-bdb9-69dc7e23571c
- FS harjoitustyö (7 op): https://www.avoin.helsinki.fi/palvelut/esittely.aspx?s=otm-b67feb5c-664a-4114-ad93-a7b982f938dc
- FS harjoitustyö (10 op): https://www.avoin.helsinki.fi/palvelut/esittely.aspx?s=otm-0b8aaeb0-d19b-43ab-9fc7-496f027776c4

(2) Täytä tämä lomake https://docs.google.com/forms/d/e/1FAIpQLSfJxtLyWugefPSPHynZcZnrsNt4IGqhpr5M7dF5jgZZ6ASqsQ/viewform

(3) lähetä email osoitteeseen matti.luukkainen@helsinki.fi Kerro emailissa opiskelijanumerosi sekä GitHub-tunnuksesi

**HUOM: työtä ei arvostella jos KAIKKIA kolmea vaihetta ei ole tehty**

Jos repositorio on privaatti lisää käyttäjät mluukkai ja hremonen collaboraattoriksi.

Arvostelussa kestää noin 4 viikkoa. Saat arvosteluun liittyvän koodikatselmoinnin projektiisi GitHub-issuena
