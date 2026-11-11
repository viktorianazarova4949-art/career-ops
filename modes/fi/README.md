# career-ops — Suomalaiset modet (`modes/fi/`)

Tämä kansio sisältää suomenkieliset käännökset tärkeimmistä career-ops-modeista hakijoille, jotka etsivät töitä Suomen markkinalla tai työskentelevät suomenkielisten työpaikkailmoitusten kanssa.

## Milloin näitä modeja käytetään?

Käytä `modes/fi/`-kansiota, jos vähintään yksi seuraavista pätee:

- Haet pääosin **suomenkielisiä työpaikkailmoituksia** (Duunitori, Oikotie, Työmarkkinatori, LinkedIn FI, yritysten oma uraportaali)
- **CV:si on suomeksi** tai vaihdat FI- ja EN-kielen välillä ilmoituksesta riippuen
- Tarvitset vastaukset ja hakemuskirjeet **luontevalla tech-suomella**, ei konekäännöksenä
- Sinun on käsiteltävä **Suomen markkinan erityispiirteet**: koeaika, irtisanomisaika, vuosiloma ja lomaltapaluuraha, työehtosopimus (TES), TyEL-eläke, ammattiliitto, työttömyyskassa (esim. YTK), toistasopimus vs. toistaiseksi voimassa oleva sopimus

Jos useimmat ilmoituksesi ovat englanniksi, pysy oletusmodeissa `modes/`-kansiossa. Englanninkieliset modet toimivat, mutta eivät tunne Suomen markkinan erityispiirteitä yhtä yksityiskohtaisesti.

## Miten aktivoit ne?

career-ops:ssa ei ole kielivalintaa kooditasolla. Vaihtoehtoja on kaksi:

### Vaihtoehto 1 — istunnon aikana

Sano Agentille istunnon alussa:

> "Käytä tästä eteenpäin suomenkielisiä modeja kansiosta `modes/fi/`."

Agentti lukee tämän kansion tiedostot oletusmodien sijaan.

### Vaihtoehto 2 — pysyvästi, profiilin kautta

Lisää `config/profile.yml`-tiedostoon:

```yaml
language:
  output: fi
  modes_dir: modes/fi
```

Muistuta Agenttiä ensimmäisessä istunnossa ("Katso `profile.yml`, olen asettanut `language.modes_dir`"). Tämän jälkeen Agentti käyttää suomenkielisiä modeja automaattisesti.

## Mitä on käännetty?

Tämä ensimmäinen iteraatio kattaa neljä vaikuttavinta modea:

| Tiedosto | Käännetty lähteestä | Rooli |
|----------|----------------------|-------|
| `_shared.md` | `modes/_shared.md` (EN) | Jaettu konteksti, arketyypit, globaalit säännöt, Suomen markkinan erityispiirteet |
| `oferta.md` | `modes/oferta.md` (ES) | Yhden ilmoituksen täysi arviointi (lohkot A–H) |
| `apply.md` | `modes/apply.md` (EN) | Live-apuri hakemuslomakkeen täyttämiseen |
| `pipeline.md` | `modes/pipeline.md` (EN) | URL-saapuneet / Second Brain kerätyille ilmoituksille |

Muut modet (`scan`, `batch`, `pdf`, `tracker`, `auto-pipeline`, `deep`, `contacto`, `ofertas`, `project`, `training`) jäävät tarkoituksella kääntämättä. Niiden sisältö on lähinnä työkaluja, polkuja ja komentoja — kieliriippumatonta.

## Mikä pysyy englanniksi?

Tarkoituksella ei käännetty, koska kyse on vakiintuneesta teknissanastosta:

- `cv.md`, `pipeline`, `tracker`, `report`, `score`, `archetype`, `proof point`
- Työkalujen nimet (`Playwright`, `WebSearch`, `WebFetch`, `Read`, `Write`, `Edit`, `Bash`)
- Trackerin tila-arvot (`Evaluated`, `Applied`, `Interview`, `Offer`, `Rejected`)
- Koodinpätkät, polut, komennot

Modet käyttävät luontevaa tech-suomea, jolla puhutaan oikeissa engineering-tiimeissä Helsingissä, Espoossa tai Tampereella: suomenkielinen löpöteksti, englanninkieliset termit siellä, missä ne ovat normaali käytäntö.

## Sanastolistaus

Pidä sävy yhdenmukaisena, jos muokkaat tai laajennat modeja:

| Englanti | Suomi (tässä koodikannassa) |
|----------|------------------------------|
| Job posting | Työpaikkailmoitus |
| Application | Hakemus |
| Cover letter | Hakemuskirje / saatekirje |
| Resume / CV | CV / ansiolomake |
| Salary | Palkka |
| Compensation | Kokonaiskompensaatio / paketti |
| Skills | Osaamiset / taidot |
| Interview | Työhaastattelu |
| Hiring manager | Rekrytoiva esimies / hiring manager |
| Recruiter | Rekrytoija |
| Requirements | Vaatimukset |
| Career history | Työhistoria / urapolku |
| Notice period | Irtisanomisaika |
| Probation | Koeaika |
| Vacation | Vuosiloma |
| Holiday pay | Lomaltapaluuraha |
| Permanent employment | Toistaiseksi voimassa oleva työsopimus |
| Fixed-term contract | Määräaikainen työsopimus |
| Freelance | Freelance / itsenäinen ammatinharjoittaja |
| Collective agreement | Työehtosopimus (TES) |
| Trade union | Ammattiliitto |
| Unemployment fund | Työttömyyskassa (esim. YTK) |
| Pension | Eläke (TyEL) |

## Osallistuminen

Parantaaksesi käännöstä tai lisätäksesi moden:

1. Avaa Issue ehdotuksesi kanssa (ks. `CONTRIBUTING.md`)
2. Noudata yllä olevaa sanastoa sävyn yhdenmukaisuuden vuoksi
3. Käännä idiomattisesti — ei sana sanalta
4. Säilytä rakenteelliset elementit (lohkot A–H, taulukot, koodilohkot, työkaluohjeet) muuttumattomina
5. Testaa oikealla suomenkielisellä ilmoituksella (Duunitori, Oikotie, LinkedIn FI) ennen pull requestia
