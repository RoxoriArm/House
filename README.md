# Paieška

Asmeninis įrankis namui susirasti. **Nekomercinis, be reklamos,
be registracijos, niekas neparduodama ir niekas nerenkama iš lankytojų.**

Puslapis sukurtas asmeniniam naudojimui, kuri ieško namo, ir kartu kaip mokymosi projektas — norėjosi
išsiaiškinti, kaip praktiškai surinkti ir sutvarkyti viešus duomenis.
Jokio verslo modelio už jo nėra ir nebus.

## Kaip elgiamasi su svetainėmis

Tai projekte svarbiausia dalis, todėl surašyta atvirai.

### robots.txt gerbiamas be išimčių

`robots.txt` yra svetainės atsakymas į klausimą „ar galima", ir čia jis
laikomas atsakymu, ne kliūtimi.

**Atskiri draudžiami keliai taip pat gerbiami**, net kai visa kita
svetainė leidžiama.

### Crawl-delay gerbiamas

Kai svetainė prašo laukti, laukiama tiek, kiek paprašė, net jei dėl to
paleidimas trunka dvidešimt minučių ilgiau:

### Apsauga nuo perteklinių užklausų

- Po nesėkmės kartojama **tik vieną kartą**, prieš tai palaukus dvigubai
  ilgiau (0,8 → 1,6 s).
- Jei tas pats serveris nepavyksta **tris kartus iš eilės**, likusios to
  serverio užklausos tą paleidimą praleidžiamos — nesidaužoma į sienas
  šimtus kartų.
- 404 ir Cloudflare patikros **nekartojamos** — kartoti nėra ko.
- Tas pats adresas per vieną paleidimą siurbiamas **tik kartą**.
- Užklausų iš viso per paleidimą: apie 300, iš jų didžioji dalis —
  sąrašų puslapiai, ne atskiri skelbimai.

### Kur einama ir kur neinama

- Imami **tik vieši skelbimų sąrašų puslapiai**, tokie, kuriuos mato
  bet kuris lankytojas be prisijungimo.
- **Neprisijungiama, neregistruojamasi, neužpildoma ir nesiunčiama nė
  viena forma.** Paskyrų, krepšelių, išsaugotų paieškų nė nebandoma.
- **Cloudflare ar kitos patikros neapeidinėjamos.** Jei gaunamas 403 —
  pasitraukiama ir įrašoma, kad šaltinis neatsakė. Niekas nebuvo apeita.

---

## Autorių teisės ir duomenys

**Rodomi faktai, ne turinys.** Kaina, plotas, sklypas, kambarių skaičius,
statybos metai, vietovė ir skelbimo antraštė. **Skelbimų aprašymai
nepublikuojami** — jie perskaitomi tik tam, kad būtų atpažinta apdaila
ir statybos baigtumas, ir į puslapį nepatenka.

**Puslapis paslėptas nuo paieškos sistemų:**

```html
<meta name="robots" content="noindex,nofollow">
```

Taip jis netampa konkuruojančiu katalogu ir neatima lankytojų iš
originalių svetainių.

**Apie lankytojus nerenkama jokia informacija.** Nėra analitikos, nėra
sekimo, nėra jokio serverio kodo — tai du statiniai failai
(`index.html` ir `duomenys.js`) GitHub Pages. Pažymėti namai ir filtrų
pasirinkimai saugomi tik pačioje naršyklėje (`localStorage`) ir niekur
nesiunčiami.

---

## Jei esate svetainės savininkas

Jei nenorite, kad jūsų svetainė būtų čia naudojama, **pakanka pasakyti** —
šaltinis bus išjungtas tą pačią dieną. Nereikia nei teisinių raštų, nei
paaiškinimų.

Projektas nėra skirtas naudoti kitiems, nėra palaikomas kaip produktas
ir nepriima pageidavimų. Jei jums pravertė kaip pavyzdys — puiku, bet
prieš siurbdami ką nors patys perskaitykite tos svetainės `robots.txt`.
