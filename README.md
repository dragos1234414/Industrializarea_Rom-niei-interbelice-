# Industrializarea României interbelice (1920–1938)

Infografic interactiv despre industria, petrolul și transporturile României Întregite. Proiect interdisciplinar Istorie – Informatică, clasa a X-a, Echipa 5.

**Pagina publicată:** `https://NUMELE-TAU-DE-UTILIZATOR.github.io/industrializare-romania-interbelica/`
(înlocuiește `NUMELE-TAU-DE-UTILIZATOR` cu numele contului GitHub după ce activezi GitHub Pages)

## Ce conține

| Secțiune | Ce arată | Tehnologie |
|---|---|---|
| Ziarul interbelic | Patru articole scurte scrise pe baza datelor | HTML, CSS |
| A. Boom-ul industrial | Serii de date 1920–1938, cu alegerea anului și a indicatorului | Chart.js |
| B. Aurul negru și transporturile | Fluxul petrolului de la sonde la rafinării, conducte și port | HTML5 Canvas |
| C. Harta industriilor | Centrele industriale (București, Reșița, Brașov, Arad, Ploiești, Constanța), cu ferestre de detalii | SVG |
| D. Simulatorul „Fii Ministrul Industriei în 1936!” | Un joc cu trei decizii economice | JavaScript |
| Export | Datele ca fișier CSV pentru Excel și versiune de tipărit | JavaScript |

## Fișiere

- `index.html` – structura paginii
- `style.css` – designul Art Deco
- `app.js` – logica aplicației; citește totul din `date.json`
- `date.json` – toate cifrele, cu gradul de încredere și sursa fiecărei cifre

## Cum rulezi local

Pornește un server local în folderul proiectului:

```
python -m http.server 8000
```

Apoi deschide `http://localhost:8000`. Dacă deschizi `index.html` direct din folder (dublu-click), pagina cere să alegi manual fișierul `date.json`.

Pagina are nevoie de internet pentru biblioteca Chart.js și pentru fonturi.

## Despre date

Fiecare cifră din `date.json` are un grad de încredere:

- **verificat** – cifra a fost regăsită într-o sursă din bibliografie (sursă secundară sau monografie accesată direct);
- **derivat** – calculată din altă cifră a sursei;
- **estimat** – valoare nesigură sau interpolată liniar între două puncte reale (apare ca punct gol în grafic).

Limite cunoscute:

- Anuarul Statistic al României 1939/40 și lucrările lui Victor Axenciuc nu au fost consultate; cifrele din sursele secundare trebuie confirmate în ele.
- Seriile `cale_ferata_km` și `chimie_productie` sunt goale, pentru că nu am găsit cifre cu an și sursă.
- La oțel, drumuri și marea industrie (1936–1937) unele puncte sunt interpolate și marcate „estimat”.

Lista completă a surselor este în `date.json` (câmpul `bibliografie`) și în secțiunea „Surse și date” a paginii.

## Tehnologii

Chart.js 4.4.7 (CDN), HTML5 Canvas, SVG inline, Web Audio API, fonturile Playfair Display și Source Sans 3 (Google Fonts).
