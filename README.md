# 🚴 Kardio Trening v3.28

**Web aplikacija za vođenje kardio treninga na sobnom biciklu**, nastala tijekom kardio rehabilitacije (veljača 2026).

> *"Tko se sa mnom druži, život mu je duži!"*

Autor: **Branke** · [WhatsApp kontakt](https://chat.whatsapp.com/DK3BTdtSjNCEuNgB5NdfAH?mode=hq1tcla) · [Revolut donacija](https://revolut.me/brankebananke)

---

## O aplikaciji

Kardio Trening je jednostavna, besplatna aplikacija u obliku jedne HTML datoteke. Ne zahtijeva instalaciju ni internet vezu — dovoljno je otvoriti datoteku u pregledniku. Namijenjena je za praćenje intervalnog kardio treninga na sobnom biciklu uz vizualni i zvučni feedback.

---

## Pokretanje

1. Preuzmi datoteku `Kardio_by_Branke_v3_28.html`
2. Otvori je u bilo kojem modernom pregledniku (Chrome, Firefox, Safari, Edge)
3. Nema instalacije, nema registracije, radi offline

> 📱 Radi i na mobitelu — responzivan dizajn prilagođen ekranima svih veličina.

---

## Kako koristiti

### 1. Odabir broja etapa

Na početnom ekranu odaberi broj etapa vožnje sobnog bicikla — dostupno od **3 do 12 etapa**.

- Preporučuje se početi s **4 etape** i postupno povećavati do maksimalnih 12
- Svaka etapa traje 3 minute (2× vježbanje + 1× odmor)
- Zadnja etapa nema odmor — trening završava nakon druge faze vježbanja

### 2. Postavljanje opcija (prije ili tijekom treninga)

Prije pokretanja ili u tijeku treninga možeš podesiti:

- **Način punjenja** — odabir vizualnog prikaza napretka (vidi dolje)
- **Zvuk kraja minute** — uključivanje/isključivanje zvučnog signala

### 3. Pokretanje treninga

Pritisni zeleni gumb **START** da pokreneš trening.

Tijekom treninga:
- Zeleni natpis **VJEŽBAJ!** označava fazu vježbanja
- Crveni natpis **ODMARAJ!** označava fazu odmora
- Plavi natpis **OPUŠTANJE** označava završnu fazu opuštanja

### 4. Pauza i nastavak

Pritisni **ZAUSTAVI** za pauziranje. Zatim:
- **NASTAVI** — nastavlja trening od mjesta zaustavljanja
- **PREKID** — vraća na početni ekran za odabir etapa

### 5. Završetak

Po završetku svih etapa i faze opuštanja pojavljuje se poruka **"Bravo trening završen!"** i gumb **PONOVI VJEŽBANJE** za novi krug.

---

## Funkcionalnosti

### 🔵 Vizualni prikaz napretka — tri kruga

Tri kruga prikazuju napredak svake od tri faze unutar etape:
- **Krug 1 (zeleni)** — prva minuta vježbanja
- **Krug 2 (zeleni)** — druga minuta vježbanja
- **Krug 3 (crveni)** — minuta odmora (skriven u zadnjoj etapi)

Za faze opuštanja sva tri kruga postaju **plava**.

#### Načini punjenja (klik na "Način punjenja")

| Način | Boja teksta | Opis |
|-------|-------------|------|
| **SAT** | 🟢 zelena | Tamni sektor napreduje poput kazaljke sata (pie animacija) |
| **VODA** | 🟠 narančasta | Tamna sjena se puni odozdo prema gore |

Animacija je fluidna u oba načina (~60 fps). Promjena načina moguća je i **u tijeku treninga** — već napunjeni krugovi ostaju napunjeni.

### 🔊 Zvučni signali

Na kraju svake faze oglašava se zvučni signal:
- **Dugi beep** — kraj faze vježbanja ili opuštanja
- **4 kratka pulsa** — kraj faze odmora

Zvuk se može isključiti klikom na tekst **"Zvuk kraja minute"** (postaje narančast kad je isključen).

### 📊 Traka napretka etapa

Ispod krugova prikazuje se redak pravokutnika koji vizualno prate napredak kroz etape:
- **Zelena** — završena etapa
- **Žuta** — pretposljednja etapa (upozorenje)
- **Crvena** — zadnja etapa

### ⏱️ Mjerenje vremena

- **Vrijeme treniranja** — ukupno proteklo vrijeme od starta
- **Preostalo vrijeme** — koliko vremena ostaje do kraja (uključujući opuštanje)

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
[ VJEŽBAJ 1 min ] → [ VJEŽBAJ 1 min ] → [ OPUŠTANJE 3 min ]
```

### Trajanje treninga po broju etapa

| Etape | Trajanje (bez opuštanja) | Ukupno (s opuštanjem) |
|-------|--------------------------|------------------------|
| 3 | 5 min | 8 min |
| 4 | 7 min | 10 min |
| 6 | 11 min | 14 min |
| 8 | 15 min | 18 min |
| 10 | 19 min | 22 min |
| 12 | 23 min | 26 min |

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
| v3.28 | WhatsApp link zamijenjen grupom (Kardio Trening Grupa@Whatsapp), verzija povećana na v3.28 |
| v3.27 | SAT način punjenja (pie animacija), fluidna animacija za oba načina (RAF), popravak zvuka |
| v3.26 | Način punjenja krugova (SAT/VODA), toggle između načina |
| v3.25 | Prethodna stabilna verzija |

---

## Licenca

Aplikacija je potpuno **besplatna** za osobnu upotrebu.
Ako ti je korisna, možeš pokazati zahvalnost donacijom na [Revolut](https://revolut.me/brankebananke). 🙏
