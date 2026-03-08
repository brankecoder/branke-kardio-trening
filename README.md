# 🚴 Kardio Trening v3.46

**Web aplikacija za vođenje kardio treninga na sobnom biciklu**, nastala tijekom kardio rehabilitacije (veljača 2026).

> *"Tko se sa mnom druži, život mu je duži!"*

Autor: **Branke** · [WhatsApp kontakt](https://chat.whatsapp.com/DK3BTdtSjNCEuNgB5NdfAH?mode=hq1tcla) · [Revolut donacija](https://revolut.me/brankebananke)

---

## O aplikaciji

Kardio Trening je jednostavna, besplatna aplikacija u obliku jedne HTML datoteke. Ne zahtijeva instalaciju ni internet vezu — dovoljno je otvoriti datoteku u pregledniku. Namijenjena je za praćenje intervalnog kardio treninga na sobnom biciklu uz vizualni i zvučni feedback.

---

## Pokretanje

1. Preuzmi datoteku `Kardio_by_Branke_vX_YZ.html`
2. Otvori je u bilo kojem modernom pregledniku (Chrome, Firefox, Safari, Edge)
3. Nema instalacije, nema registracije, radi offline

> 📱 Radi i na mobitelu — responzivan dizajn prilagođen ekranima svih veličina.

---

## Kako koristiti

### 1. Odabir broja etapa

Na početnom ekranu odaberi broj etapa vožnje sobnog bicikla — dostupno od **3 do 12 etapa**.

- Preporučuje se početi s **4 etape** i postupno povećavati do maksimalnih 12
- Svaka etapa traje 3 minute (2× vježbanje + 1× odmor)
- Zadnja etapa nema odmor — trening završava s 3 minute opuštanja

### 2. Postavljanje opcija (prije ili tijekom treninga)

Prije pokretanja ili u tijeku treninga možeš podesiti:

- **Način punjenja** — odabir vizualnog prikaza napretka (vidi dolje)
- **Zvuk minute** — odabir načina zvučnih signala: GLAS → BEEP → ISKLJ.

### 3. Pokretanje treninga

Nakon odabira etapa prikazuje se poruka **ČEKAM!** i zeleni gumb **START**.

Pritisni **START** da pokreneš trening. Gumbi START i PREKID nestaju i slijedi kratko odbrojavanje:
- nakon 1s prikazuje se crveni natpis **PRIPREMA!** *(u GLAS modu izgovara se "Priprema!")*
- nakon 2s prikazuje se narančasti natpis **POZOR!** *(u GLAS modu izgovara se "Pozor!")*
- nakon 3s trening kreće, pojavljuje se gumb **ZAUSTAVI** i zeleni natpis **VJEŽBAJ!** *(u GLAS modu izgovara se "Vježbaj!")*

Tijekom treninga:
- Zeleni natpis **VJEŽBAJ!** označava fazu vježbanja
- Crveni natpis **ODMARAJ!** označava fazu odmora
- Plavi natpis **OPUŠTANJE!** označava završnu fazu opuštanja

### 4. Pauza i nastavak

Pritisni **ZAUSTAVI** za pauziranje. Zatim:
- **NASTAVI** — nastavlja trening od mjesta zaustavljanja
- **PREKID** — vraća na početni ekran za odabir etapa

### 5. Završetak

Po završetku svih etapa i faze opuštanja pojavljuje se poruka **"Bravo trening je završen!"** i gumb **PONOVI VJEŽBANJE** za novi krug.

---

## Funkcionalnosti

### 🔵 Vizualni prikaz napretka — tri kruga

Tri kruga prikazuju napredak svake od tri faze unutar etape:
- **Krug 1 (zeleni)** — prva minuta vježbanja
- **Krug 2 (zeleni)** — druga minuta vježbanja
- **Krug 3 (crveni)** — minuta odmora (skriven u zadnjoj etapi)

Za fazu opuštanja sva tri kruga postaju **plava**.

#### Načini punjenja (klik na "Način punjenja")

| Način | Boja teksta | Opis |
|-------|-------------|------|
| **SAT** | 🟢 zelena | Tamni sektor napreduje poput kazaljke sata (pie animacija) |
| **VODA** | 🟠 narančasta | Tamna sjena se puni odozdo prema gore |

Animacija je fluidna u oba načina (~60 fps). Promjena načina moguća je i **u tijeku treninga** — već napunjeni krugovi ostaju napunjeni.

### 🔊 Zvučni signali — tri načina (klik na "Zvuk minute")

| Način | Opis |
|-------|------|
| **GLAS** | Sinteza govora na hrvatskom: izgovara "Priprema!", "Pozor!", "Vježbaj!" i najave kraja etapa |
| **BEEP** | Zvučni signali: dugi beep na kraju 1. min/odmora, 4 kratka pulsa na kraju 2. min |
| **ISKLJ.** | Bez zvuka |

U načinu **GLAS**:
- Odbrojavanje govori: *"Priprema!"* → *"Pozor!"* → *"Vježbaj!"*
- Na početku prve minute svake etape izgovara se *"Vježbaj!"*
- Na kraju druge minute svake etape izgovara se broj etape i najava (npr. *"Treća etapa završena, odmori!"*)
- Na kraju zadnje etape: *"Odlično! Sve etape završene!"*
- Bez beep signala (samo govor)

### 📊 Traka napretka etapa

Ispod krugova prikazuje se redak pravokutnika koji vizualno prate napredak kroz etape:
- **Zelena** — završena etapa
- **Žuta** — pretposljednja etapa (upozorenje)
- **Crvena** — zadnja etapa

### ⏱️ Mjerenje vremena

- **Vrijeme treniranja** — ukupno proteklo aktivno vrijeme vježbanja (bez odmora i opuštanja)
- **Preostalo vrijeme** — koliko vremena ostaje do kraja (uključujući odmore i završno opuštanje)

### 📱 Wake Lock

Aplikacija automatski sprječava gašenje zaslona mobilnog uređaja tijekom treninga.

### 📱 QR kod

Klikom na **"QR kod"** (žuti tekst) generira se QR kod za dijeljenje aplikacije.

---

## Struktura treninga

Svaki dnevni kardio trening preporučuje se sastavljati od:

1. **Jutarnja tjelovježba** ([YouTube link](https://youtu.be/EkyuoWBDIo0?t=85)) — 30 minuta
2. **Prijepodnevna vožnja** sobnog bicikla — ovaj program
3. **Popodnevna vožnja** sobnog bicikla — ovaj program

### Interval po etapi

```
[ VJEŽBAJ 1 min ] → [ VJEŽBAJ 1 min ] → [ ODMORI 1 min ] → sljedeća etapa
```

Zadnja etapa:
```
[ VJEŽBAJ 1 min ] → [ VJEŽBAJ 1 min ] → [ OPUŠTANJE! 3 min ]
```

### Trajanje treninga po broju etapa

| Etape | Trening | Ukupno |
|-------|---------|--------|
| 3 | 6 min | 11 min |
| 4 | 8 min | 14 min |
| 6 | 12 min | 20 min |
| 8 | 16 min | 26 min |
| 10 | 20 min | 32 min |
| 12 | 24 min | 38 min |

---

## Napomene

- ⚠️ Prije početka vježbanja savjetujte se s liječnikom.
- 🔰 Vježbe započnite lagano i postupno pojačavajte.
- 🚴 Sobni bicikl: preporučuje se srednje opterećenje i tempo oko **60 okretaja/min (≈15 km/h)**.
- 💻 Aplikacija ne prikuplja podatke, ne treba internet i radi lokalno u pregledniku.

---

## Verzije

| Verzija | Opis |
|---------|------|
| v3.46 | Upute i napomene poravnate s lijevim rubom gumba za odabir broja etapa |
| v3.45 | README: sortirane verzije silazno; ispravljen opis "Preostalo vrijeme"; ispravljena tablica trajanja treninga |
| v3.44 | README modal: dodan scroll na iOS uređajima (max-height + overflow-y + -webkit-overflow-scrolling) |
| v3.43 | Prečica na radnoj površini: uklonjen PWA install prompt, prikazuju se jasne upute za Android, iOS, Chrome, Edge i Firefox |
| v3.42 | Globalni brojač završenih vožnji: narančasti tekst ispod brojača pokretanja, +1 pri startu opuštanja (CountAPI) |
| v3.41 | Brojač pokretanja promijenjen s localStorage na globalni CountAPI (countapi.mileshilliard.com) |
| v3.40 | Dodan inline PWA manifest — prečica na radnoj površini dobiva naziv "Kardio Trening" |
| v3.39 | Brojač pokretanja premješten na Info/QR ekran (iznad QR koda) |
| v3.38 | Gumb "QR kod" preimenovan u "Info"; prečica na radnoj površini; brojač pokretanja APP (localStorage, početak od 150) |
| v3.37 | GLAS mod: glasovne najave "Priprema!", "Pozor!", "Vježbaj!" u odbrojavanju i na početku svake etape |
| v3.36 | ČEKAM! poruka po odabiru etapa; 3s odbrojavanje (PRIPREMA!/POZOR!) prije pokretanja vježbanja |
| v3.35 | Glasovni signal (GLAS) kao default; redoslijed: GLAS→BEEP→ISKLJ.; u GLAS modu bez beep-a na kraju faze |
| v3.33 | Tri stanja zvuka: BEEP/ISKLJ./GLAS; GLAS = sinteza govora (hr) izgovara završetak faze i "Sve etape završene!" |
| v3.32 | Pulsirajući beep (4 pulsa) na kraju 2. min; auto-skaliranje; onemogućen pinch-zoom |
| v3.31 | Favicon (kardio bicikl) ugrađen kao Base64 |
| v3.30 | Sat treniranja broji samo aktivno vježbanje; manje ispravke teksta |
| v3.27–29 | SAT/VODA animacija, WhatsApp grupa, popravci |

---

## Licenca

Aplikacija je potpuno **besplatna** za osobnu upotrebu.
Ako ti je korisna, možeš pokazati zahvalnost donacijom na [Revolut](https://revolut.me/brankebananke). 🙏
