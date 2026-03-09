# Mitäs tarttis vielä pohtia:
- Joka sivulle oma banneri? Sain tehtyä värikorostuksen niin ei välttämättä tarvi
- Banneri meni rikki
- Saanko sivunimistä .html pois?
- Tarkista kuvakoot
- Siivoa CSS:stä turhat fonttikoot pois.
- Poista flex-item divit jos turhia, CSS:ssä ei ole niille mitään nyt
- Kirjallisuus sivulla kuva katoaa isolla näytöllä
- Kaikki kuvat ei pysy näkyvissä, oikealle vuotaa yli
- Jos haluat, että Prettier siivoaa koodin aina tallennettaessa: Settings → Format On Save → päälle
- Siivoa ja tarkista kommentit

- PALAUTA puhdas versio testauksesta.

Onko nämä molemmat koodit tarpeen? ei, poistettu .flex_item img
.flex_item img {
  width: 100%;
  height: auto;
  display: block;
  object-fit: cover;
}

.img {
  max-width: 100%;
  height: auto;
  display: block;
}

Käytänkö tätä:

.banneri-container {
  width: 100vw;
  margin-left: 50%;
  transform: translateX(-50%);
  overflow: hidden;
}

Poistettu: /* Piilottaa listan ensimmäisen bulletin, joka on usein epämiellyttävä kuvaan nähden */
.book-list > li:last-child {
  list-style-type: none;
}

Tämä ei muuttamu kuvien muutosta 
.kuva1, .kuva2 {
  width: 300px;
  height: auto;
  display: block;
  object-fit: cover;
}

Poistettu medioista:
  body {
    /* font-size: 20px; */
  }
    body {
    /* font-size: 24px; */
  }
    body {
    /* font-size: 24px; */
  }