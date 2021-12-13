Kuvitteellinen tila jossa opettaja masterina asentaisi geogebran opiskelijoille(minioneille) ja jotenkin rajoittaisi heidän internettiin pääsyä tai tekisi lunttaamisesta vaikeampaa. Kaikki toimisi salt-stack:llä.


Huomasin että jos käyttää vain komentoa *sudo apt-get install geogebra* se asentaa geogebra6 ja siinä oli jotain ongelmia conf tiedostojen kanssa. Ne olivat jossakin srv muodossa, en ymmärtänyt miten olisi pitänyt toimia. Siksi valitsin 5-version. Siinä config file sijaitsi /etc/geogebra/geogebra.conf, toisin kuin geogebra6:ssa.
Ihan ensimmäiseksi lisäsin kokeilen asentaa asiat käsin.
![Screenshot](https://i.imgur.com/UEBh4Ch.png)

Olin luonut ekana repon geogebralle ja kun yritin lisätä avainta se ei toiminut. Mietinnän jälkeen tajusin iha itse mennä poistamaan repon. Lisäsin avaimen jonka jälkeen loin repon. Sitten pystyin asentamaan geogebra5.

![Screenshot1](https://i.imgur.com/7MWqnJT.png) Tässä on toimiva geogebra5 käsin asennettuna.

Tältä näyttää init.sls file
![Screenshot7](https://i.imgur.com/BHS5Y2v.png) 

![Screenshot2](https://i.imgur.com/oKE7lIf.png)
![Screenshot3](https://i.imgur.com/DmpjGFt.png)
![Screenshot4](https://i.imgur.com/kNRjGFc.png)

geogebran conf tiedostoon tein muutoksia kuten anti-aliasing pois päältä vaikka ei sitä edes näe tästä vm-koneelta ja otin pois käytöstä geogebran käynnistys logon. Conf tiedosto toimii kun kokeilin, ei näkynyt käynnistyksen yhteydessä logoa.

![Screenshot5](https://i.imgur.com/twzLHPp.png)

service.running ei toiminut jostakin syystä. Kokeilin terminaalin kautta katsoa sen statuksen,käynnistää sekä lopettaa käyttäen *sudo systemctl...*. Mutta sama error.
En saanut selville mikä oli ongelmana.

![Screenshot6](https://i.imgur.com/YQfvhEi.png)
pkg.removed poistaa oletuksena tulevan firefoxin. Ei estä lunttaamista mutta vaikeuttaa tosi tosi vähän...
