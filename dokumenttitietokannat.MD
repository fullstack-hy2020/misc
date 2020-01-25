# Dokumenttitietokannat, esim. MongoDB

Dokumenttitietokantojen voi ajatella sijoittuvan jonnekin relaatiotietokantojen ja avain-arvotietokantojen puolen välin tienoille. Dokumenttikannat perustuvat avain-arvotietokantojen tapaan arvojen tallettamiseen avaimen perusteella. Arvot tai *dokumentit* kuten niitä dokumenttikantojen kontekstissa nimitetään voivat kuitenkin olla itsessään hyvin monimutkaisia oliota, jotka sisältävät kenttiä, joiden arvona voi olla joko normaaleja arvoja kuten lukuja ja merkkijonoja tai muita olioita. Toisin kuin avain-arvotietokannoissa, dokumenttikannat "näkevät" tietokantaan talletettujen dokumenttien sisään, ja mahdollistavat talletettujen dokumenttien sisällön suhteen tehdyt kyselyt.

Käytetään seuraavassa esimerkkinä ylivoimaisesti suosituimman dokumenttitietokannan <a href="https://www.mongodb.org/">MongoDB:n</a> merkintöjä.

<br/>

Dokumenttikannoissa käytetään tiedon loogisena esitysmuotona yleensä <a href="https://fi.wikipedia.org/wiki/JSON">JSON</a>:ia. Seuraavassa kurssia *Ohjelmoinnin perusteet* esittävä JSON-dokumentti:


```javascript
{
  "id": ObjectId("10"),
  "nimi": "Ohjelmistotekniikka",
  "laajuus": 5,
  "luennot": [ "Matti Luukkainen" ]
}
```

JSON-dokumentti koostuu avain-arvo-pareista. Avainta vastaava arvo merkitään kaksoispisteellä erotettuna avaimen yhteyteen.

Kurssi-dokumentissa on siis neljä avain-arvo-paria. Voidaankin ajatella että kurssilla on neljä kenttää. Näistä kentistä erikoisasemassa on MongoDB:n dokumentille automaattisesti generoima avainkenttä `id` jonka arvo on tyypiltään `ObjectId`. Poikkeavaa relaatiotietokantoihin nähden on se, että kentän arvona voi olla taulukko.

Seuraavassa on opiskelijaa kuvaava dokumentti:


```javascript
{
  "id" : ObjectId("59"),
  "nimi" : "Pekka Mikkola",
  "opiskelijanumero" : 14112345,
  "osoite" : {
                "katu" : "Tehtaankatu 10 B 1",
                "postinumero" : "00120",
                "postitoimipaikka" : "Helsinki"
             }
}
```

Nyt kentän osoite arvona on *olio*, jolla on itsellään omat kenttänsä.

Dokumenttitietokannassa dokumentit on lajiteltu *kokoelmiin* (engl. collection). Kokoelman merkitys on suunnilleen sama kuin taulun relaatiotietokannassa. Yhdessä kokoelmassa olevien dokumenttien ei kuitenkaan tarvitse olla kentiltään samanlaisia. Kenttiä voi olla vaihteleva määrä ja saman nimiset kentät voivat sisältää eri dokumenteilla eri tyyppisen arvon. Kokoelmille ei määritellä dokumenttikannoissa minkäänlaista skeemaa, eli on täysin sovellusten vastuulla, että kantaan talletetaan järkevää dataa, ja että kannasta luettava data tutkitaan oikein.

Kuten edellä opiskelijan kohdalla näimme, on dokumenttikannoissa mahdollista sisällyttää olioita toistensa sisään. Tilanne olisi myös voitu mallintaa "relaatiomallin tapaan" siten, että osoitteita varten olisi oma kokoelmansa, ja yksittäinen osoite mallinnettaisiin omana dokumenttina:


```javascript
{
  "id" : ObjectId("123"),
  "katu" : "Tehtaankatu 10 B 1",
  "postinumero" : "00120",
  "postitoimipaikka" : "Helsinki"
}
```

Opiskelijadokumentti sisältäisi nyt ainoastaan viitteen osoitedokumenttiin:


```javascript
{
  "id" : ObjectId("59"),
  "nimi" : "Pekka Mikkola",
  "opiskelijanumero" : 14112345,
  "osoite" : ObjectId("123")
}
```

Toisin kuin relaatiotietokantojen tapauksessa, dokumenttikannat *eivät tarjoa* tietokannan tasolla tapahtuvia *liitosoperaatiota*, ja edellisen esimerkin tapauksessa sovelluksen olisi itse huolehdittava siitä, että opiskelijaa haettaessa haetaan myös opiskelijan osoite tietokannasta.

Vaikka operaatio ei olekaan dokumenttikannan tasolla tuettu, on olemassa monia kirjastoja, jotka toteuttavat ohjelmallisen liitosoperaation siten, että sovellusohjelman ei tarvitse siitä huolehtia.

Relaatiotietokannoissa kannan skeeman muodostaminen on sikäli helppoa, että normalisoituun ratkaisuun pyrittäessä useimmissa tilanteissa on olemassa noin yksi "järkevä" ratkaisu, joka toimii lähes yhtä hyvin riippumatta siitä miten kantaa käytetään.

Dokumenttikantojen suhteen tilanne on toinen. Tarkastellaan esimerkiksi Kursseja ja Opiskelijoiden kurssisuorituksia. Relaatiotietokannassa tilanne olisi suoraviivainen, *Suoritus* olisi *Kurssin* ja *Opiskelijan* liitostaulu.

Eräs mahdollisuus olisi tehdä täsmälleen sama ratkaisu dokumenttikannassa.

Kokoelma Opiskelija:

```javascript
[
  {
    "id": ObjectId("10"),
    "nimi" : "Lea Kutvonen",
    "opiskelijanumero" : 13457678
  },
  {
    "id": ObjectId("11"),
    "nimi" : "Pekka Mikkola",
    "opiskelijanumero" : 14012345
  }
]
```

Kokoelma kurssi:

```javascript
[
  {
    "id": ObjectId("34"),
    "nimi" : "Ohjelmoinnin perusteet",
    "laajuus" : 5
  },
  {
    "id": ObjectId("35"),
    "nimi" : "Tietokone työvälineenä",
    "laajuus" : 1
  }
]
```

Suoritus olisi nyt "liitostaulumainen" kokoelma:


```javascript
[
  {
    "id": 55
    "kurssi_id" : ObjectId("34"),
    "opiskelija_id" : ObjectId("10"),
    "arvosana" : 4
  },
  {
    "id": 56
    "kurssi_id" : ObjectId("35"),
    "opiskelija_id" : ObjectId("10"),
    "arvosana" : 5
  },
  {
    "id": 57
    "kurssi_id" : ObjectId("35"),
    "opiskelija_id" : ObjectId("11"),
    "arvosana" : 2
  }
]
```

Vaihtoehtoja on kuitenkin myös muita. Käyttötapauksista riippuen saattaisi olla edullista tallettaa tieto suorituksista ("liitosdokumentin" id) myös kurssin ja opiskelijan yhteyteen:

Kokoelma Opiskelija:

```javascript
[
  {
    "id": ObjectId("10")
    "nimi" : "Lea Kutvonen",
    "opiskelijanumero" : 13457678,
    "suoritukset" : [ ObjectId("55"), ObjectId("56") ]
  },
  {
    "id": ObjectId("11")
    "nimi" : "Pekka Mikkola",
    "opiskelijanumero" : 14012345,
    "suoritukset" : [ ObjectId("57") ]
  }
]
```

Kokoelma kurssi:

```javascript
[
  {
    "id": ObjectId("34")
    "nimi" : "Ohjelmoinnin perusteet",
    "laajuus" : 5,
    "suorittajat" : [ObjectId("10")]
  },
  {
    "id": ObjectId("35")
    "nimi" : "Tietokone työvälineenä",
    "laajuus" : 1,
    "suorittajat" : [ObjectId("10"), ObjectId("11")]
  }
]
```

Jossain tapauksessa paras ratkaisu olisi luopua liitoksena toimivista dokumenteista eli kokoelmasta suoritukset ja tallettaa suoritukset kokonaisuudessaan opiskelija-dokumentteihin:

```javascript
[
  {
    "id": ObjectId("10")
    "nimi" : "Lea Kutvonen",
    "opiskelijanumero" : 13457678,
    "suoritukset" : [
      {
        "id": 55
        "kurssi_id" : ObjectId("34"),
        "arvosana" : 4
      },
      {
        "id": 56
        "kurssi_id" : ObjectId("35"),
        "arvosana" : 5
      }
    ]
  },
  {
    "id": ObjectId("11")
    "nimi" : "Pekka Mikkola",
    "opiskelijanumero" : 14012345,
    "suoritukset" : [
      {
        "id": 57
        "kurssi_id" : ObjectId("35"),
        "arvosana" : 2
      }
    ]
  }
]
```

Tämä ratkaisu vaikeuttaisi kurssin suorittajien selvittämistä, joten joissain käyttötapauksissa saattaisi olla edullista sisällyttää suoritukset *molempiin* opiskelijoihin ja kurssiin.

Yhtä "oikeaa" vastausta miten sovelluksen data kannattaa mallintaa dokumenttikannan kokoelmiksi ja dokumenteiksi ei ole olemassa. Parhaaseen tapaan vaikuttaa suuresti se minkälainen käyttöprofiili rakennettavalla sovelluksella on: datamalli kannattaa valita siten, että se tekee yleisimpien operaatioiden suorituksen nopeaksi ja helpoksi.

Kuten jo totesimme, dokumenttikannat eivät tue liitosoperaatioita, ja kyselyt kohdistuvat aina vain yhteen kokoelmaan. Dokumenttikannoilla ei ole mitään standardoitua kyselykieltä, jokaisen kannan kyselykieli on täysin omanlaisensa. Esim. MongoDB:n kyselykieli ei muistuta kovinkaan läheisesti SQLää.

Dokumenttikannat eivät myöskään tue useamman kokoelman yhtäaikaista muuttamista transaktionaalisesti. Kaikki yhteen kokoelmaan suoritettavat tapahtumat tehdään kuitenkin aina transaktionaalisesti.