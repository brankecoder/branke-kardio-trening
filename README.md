# 🚴 Kardio Trening

**Jednostavna web aplikacija za intervalnivodio trening na sobnom biciklu.**  
Nastala u veljači 2026. tijekom kardio rehabilitacije.

---

## ✨ O aplikaciji

Kardio Trening je besplatna, single-file HTML aplikacija koja ne zahtijeva instalaciju ni internetsku vezu. Dovoljno je preuzeti jednu `.html` datoteku i otvoriti je u pregledniku. Namijenjena je za praćenje intervalnog kardio treninga na sobnom biciklu s vizualnim i zvučnim feedbackom.

---

## 🚀 Pokretanje

1. Preuzmi najnoviju verziju: [`Kardio_by_Branke_v3_37.html`](Kardio_by_Branke_v3_37.html)
2. Otvori je u pregledniku (Chrome, Firefox, Safari, Edge)
3. Nema instalacije, nema registracije — radi potpuno offline

> 📱 Radi i na mobitelu — responzivan dizajn prilagođen svim veličinama ekrana.

---

## 🎯 Kako koristiti

### 1. Odaberi broj etapa

Na početnom ekranu odaberi broj etapa — od **3 do 12**.

- Preporučuje se početi s **4 etape** i postupno povećavati
- Svaka etapa traje 3 minute: `2× vježbanje + 1× odmor`
- Zadnja etapa nema odmor — slijedi 3 minute opuštanja

### 2. Pokreni trening

Pritisni **START**. Slijedi kratko odbrojavanje:

| Vrijeme | Prikaz | GLAS mod |
|---------|--------|----------|
| +1s | 🔴 **PRIPREMA!** | *"Priprema!"* |
| +2s | 🟠 **POZOR!** | *"Pozor!"* |
| +3s | 🟢 **VJEŽBAJ!** | *"Vježbaj!"* |

### 3. Prati napredak

- 🟢 **VJEŽBAJ!** — faza vježbanja
- 🔴 **ODMARAJ!** — faza odmora
- 🔵 **OPUŠTANJE!** — završna faza (3 min)

### 4. Zaustavi ili prekini

- **ZAUSTAVI** → pauza, zatim **NASTAVI** ili **PREKID**

---

## ⚙️ Funkcionalnosti

### 🔵 Vizualni prikaz — tri kruga

| Krug | Boja | Faza |
|------|------|------|
| 1 | 🟢 zeleni | 1. minuta vježbanja |
| 2 | 🟢 zeleni | 2. minuta vježbanja |
| 3 | 🔴 crveni | minuta odmora *(skriven u zadnjoj etapi)* |

Za fazu opuštanja sva tri kruga postaju 🔵 plava.

#### Načini animacije (klik na "Način punjenja")

| Način | Opis |
|-------|------|
| **SAT** | Sektor napreduje poput kazaljke sata |
| **VODA** | Punjenje odozdo prema gore |

Animacija je fluidna (~60 fps). Može se mijenjati i **u tijeku treninga**.

### 🔊 Zvučni signali (klik na "Zvuk minute")

| Način | Opis |
|-------|------|
| **GLAS** | Sinteza govora na hrvatskom — izgovara "Priprema!", "Pozor!", "Vježbaj!", najave etapa i završetka |
| **BEEP** | Zvučni signali: dugi beep / 4 kratka pulsa |
| **ISKLJ.** | Bez zvuka |

### 📊 Traka napretka etapa

Pravokutnici ispod krugova prate napredak:  
🟩 završena · 🟨 pretposljednja · 🟥 zadnja

### ⏱️ Mjerenje vremena

- **Sat treniranja** — broji samo aktivno vježbanje (bez odmora i opuštanja)
- **Preostalo** — ukupno preostalo do kraja

### 📱 Wake Lock

Sprječava gašenje zaslona na mobitelu dok trening teče.

### 📷 QR kod

Klik na žuti tekst **"QR kod"** generira QR za dijeljenje aplikacije.

---

## 🏗️ Struktura treninga

```
Etapa 1..N-1:   [ VJEŽBAJ 1min ] → [ VJEŽBAJ 1min ] → [ ODMORI 1min ]
Zadnja etapa:   [ VJEŽBAJ 1min ] → [ VJEŽBAJ 1min ] → [ OPUŠTANJE 3min ]
```

### Trajanje po broju etapa

| Etape | Vježbanje | Ukupno (s opuštanjem) |
|-------|-----------|------------------------|
| 3  | 5 min  | 8 min  |
| 4  | 7 min  | 10 min |
| 6  | 11 min | 14 min |
| 8  | 15 min | 18 min |
| 10 | 19 min | 22 min |
| 12 | 23 min | 26 min |

---

## 📋 Dnevni program

Preporučena struktura dnevnog kardio treninga:

1. 🤸 **Jutarnja tjelovježba** — 30 min ([YouTube](https://youtu.be/EkyuoWBDIo0?t=85))
2. 🚴 **Prijepodnevna vožnja** — ovaj program
3. 🚴 **Popodnevna vožnja** — ovaj program

---

## 📝 Napomene

- ⚠️ Prije početka savjetujte se s liječnikom.
- 🔰 Počnite lagano i postupno povećavajte intenzitet.
- 🚴 Preporučeno opterećenje: srednje, ~60 okr/min (≈15 km/h).
- 💻 Aplikacija ne prikuplja nikakve podatke i radi potpuno lokalno.

---

## 📦 Verzije

| Verzija | Opis |
|---------|------|
| **v3.37** | GLAS mod: glasovne najave "Priprema!", "Pozor!", "Vježbaj!" u odbrojavanju i na početku svake etape; stišani beep (−50%); gumb "POVRATAK" |
| v3.36 | ČEKAM! poruka; 3s odbrojavanje (PRIPREMA!/POZOR!) prije starta |
| v3.35 | GLAS kao default; redoslijed: GLAS→BEEP→ISKLJ. |
| v3.33 | Tri stanja zvuka: BEEP/ISKLJ./GLAS; sinteza govora (hr) |
| v3.32 | Pulsirajući beep (4 pulsa); auto-skaliranje; pinch-zoom onemogućen |
| v3.31 | Favicon ugrađen kao Base64 |
| v3.30 | Sat treniranja broji samo aktivno vježbanje |
| v3.27–29 | SAT/VODA animacija, WhatsApp grupa, popravci |

---

## 💝 Autor

Napravio **Branke** uz malo pomoći AI alata.

- 💬 [WhatsApp grupa](https://chat.whatsapp.com/DK3BTdtSjNCEuNgB5NdfAH?mode=hq1tcla)
- ☕ [Revolut donacija](https://revolut.me/brankebananke) — ako ti je aplikacija korisna, svaka podrška je dobrodošla!

---

## 📄 Licenca

Aplikacija je potpuno **besplatna** za osobnu upotrebu.  
Zabranjena bilo kakva komercijalna upotreba.
Slobodno dijeli, ali molim te ostavi za čaj s rumom autoru. 🙏
