# Äänestyssovellus – Käyttötapauskuvaukset (hyvä sellainen ehkä.)

## 1. Selaa äänestystuloksia

| Kenttä | Kuvaus |

| **Käyttötapauksen nimi** | Selaa äänestystuloksia |
| **Käyttäjät** | Käyttäjä |
| **Laukaisija** | Käyttäjä haluaa nähdä äänestyksen tulokset |
| **Esiehto** | Järjestelmässä on vähintään yksi äänestys |
| **Jälkiehto** | Käyttäjä on nähnyt valitun äänestyksen tulokset |

**Käyttötapauksen kulku:**

1. Käyttäjä avaa sovelluksen etusivun.
2. Järjestelmä näyttää listan kaikista äänestyksistä.
3. Käyttäjä valitsee äänestyksen, jonka tuloksia haluaa tarkastella.
4. Järjestelmä näyttää äänestyksen tulokset: vaihtoehtojen nimet, äänimäärät ja prosenttiosuudet.

**Poikkeuksellinen toiminta:**

- **4a.** Jos äänestyksessä ei ole vielä yhtään ääntä, järjestelmä näyttää ilmoituksen "Ei vielä ääniä".

## 2. Äänestää äänestyksessä

| Kenttä | Kuvaus |

| **Käyttötapauksen nimi** | Äänestää äänestyksessä |
| **Käyttäjät** | Käyttäjä |
| **Laukaisija** | Käyttäjä haluaa antaa äänensä äänestyksessä |
| **Esiehto** | Järjestelmässä on vähintään yksi äänestys ja käyttäjä ei ole vielä äänestänyt kyseisessä äänestyksessä |
| **Jälkiehto** | Käyttäjän ääni on tallennettu ja äänestyksen tulokset ovat päivittyneet |

**Käyttötapauksen kulku:**

1. Käyttäjä avaa sovelluksen etusivun.
2. Järjestelmä näyttää listan kaikista äänestyksistä.
3. Käyttäjä valitsee äänestyksen, johon haluaa osallistua.
4. Järjestelmä näyttää äänestyksen vaihtoehdot.
5. Käyttäjä valitsee haluamansa vaihtoehdon.
6. Käyttäjä vahvistaa äänensä painamalla "Äänestä"-painiketta.
7. Järjestelmä tallentaa äänen ja näyttää päivitetyt tulokset.

**Poikkeuksellinen toiminta:**

- **5a.** Jos käyttäjä ei valitse vaihtoehtoa ennen vahvistamista, järjestelmä näyttää virheilmoituksen "Valitse vaihtoehto ennen äänestämistä".
- **6a.** Jos käyttäjä on jo äänestänyt kyseisessä äänestyksessä, järjestelmä näyttää ilmoituksen "Olet jo äänestänyt tässä äänestyksessä".

## 3. Luoda uusi äänestys

| Kenttä | Kuvaus |

| **Käyttötapauksen nimi** | Luoda uusi äänestys |
| **Käyttäjät** | Ylläpitäjä |
| **Laukaisija** | Ylläpitäjä haluaa luoda uuden äänestyksen |
| **Esiehto** | Ylläpitäjä on kirjautunut järjestelmään |
| **Jälkiehto** | Uusi äänestys on luotu ja se näkyy äänestyslistalla |

**Käyttötapauksen kulku:**

1. Ylläpitäjä siirtyy äänestyksen luontisivulle.
2. Järjestelmä näyttää lomakkeen uuden äänestyksen luomista varten.
3. Ylläpitäjä syöttää äänestyksen otsikon.
4. Ylläpitäjä lisää vähintään kaksi vastausvaihtoehtoa.
5. Ylläpitäjä painaa "Luo äänestys" -painiketta.
6. Järjestelmä tallentaa äänestyksen ja näyttää vahvistusilmoituksen.
7. Uusi äänestys näkyy äänestyslistalla.

**Poikkeuksellinen toiminta:**

- **3a.** Jos ylläpitäjä jättää otsikon tyhjäksi, järjestelmä näyttää virheilmoituksen "Syötä äänestyksen otsikko".
- **4a.** Jos ylläpitäjä yrittää luoda äänestyksen alle kahdella vaihtoehdolla, järjestelmä näyttää virheilmoituksen "Lisää vähintään kaksi vaihtoehtoa".

## 4. Poistaa äänestys

| Kenttä | Kuvaus |

| **Käyttötapauksen nimi** | Poistaa äänestys |
| **Käyttäjät** | Ylläpitäjä |
| **Laukaisija** | Ylläpitäjä haluaa poistaa äänestyksen järjestelmästä |
| **Esiehto** | Ylläpitäjä on kirjautunut järjestelmään ja järjestelmässä on vähintään yksi äänestys |
| **Jälkiehto** | Äänestys on poistettu eikä se enää näy äänestyslistalla |

**Käyttötapauksen kulku:**

1. Ylläpitäjä siirtyy äänestysten hallintanäkymään.
2. Järjestelmä näyttää listan kaikista äänestyksistä.
3. Ylläpitäjä painaa poistettavan äänestyksen kohdalla "Poista"-painiketta.
4. Järjestelmä näyttää vahvistusdialogin: "Haluatko varmasti poistaa tämän äänestyksen?"
5. Ylläpitäjä vahvistaa poistamisen.
6. Järjestelmä poistaa äänestyksen ja päivittää listan.

**Poikkeuksellinen toiminta:**

- **5a.** Jos ylläpitäjä peruuttaa poistamisen, järjestelmä palaa takaisin hallintanäkymään eikä äänestykseen tehdä muutoksia.