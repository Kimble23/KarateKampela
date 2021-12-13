Miniprojektin ideana on (kuvitteelisesti) toimia luokkahuoneessa. Esimerkki tilanne, jonka tämä korjaisi...
Luokka tekee koneilla kokeen, mutta opettaja ei pysty valvomaan jokaisen oppilaan näyttöä koko kokeen ajan.
esim moodle tentissä on helppo googlettaa nopeasti yksinkertaisella hakusanalla.
Ratkaisuna olisi herra-orja arkkitehtuuri. Opettaja olisi herra (master) ja oppilaat (orjia). Opettaja sekä oppilaat käyttävät LINUXIA. Opettaja laittasi file.managed
-komennolla oppilaille kokeen eli jonkun tehtävänannon ja (vastauslomakkeen).

Ensimmäiseksi asensin käsin chocon ja kokeilin asentaa geogebran. Sehän toimi, joten loin infraa koodina (init.sls) tiedoston. 
![Screenshot](https://i.imgur.com/y5FHYpQ.png)

Suoritin komennon *sudo salt '*' state.apply win*
![Screenshot1](https://i.imgur.com/OJ0Szmy.png)

