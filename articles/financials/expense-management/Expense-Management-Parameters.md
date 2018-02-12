---
title: Parametere for reiseregning og utlegg
description: "Følgende parametere kontrollerer virkemåten i reiseregninger og utlegg."
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 8ca9e80d6d2b87fcdd10ebb9d32bd0a2b2d15614
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="expense-management-parameters"></a>Parametere for reiseregning og utlegg
-----------------------------

Parametrene kontrollerer den generelle virkemåten i reiseregninger og utlegg.

### <a name="general"></a>Generelt

| **Felt**                                                | **Beskrivelse**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **Standard kilometersats**                             | Angi refusjonssatsen for kilometergodtgjørelseutgifter. Satsen vil bli multiplisert med antall kilometer som angitt i utgiften for å beregne beløpet refundert for reiseutgifter.                       |
|**Personlige utgifter betalt av**                             | Velg hvem som er ansvarlig for å betale alle kredittkort transaksjonsbeløpene kategoriseres som personlig.                                                                                                     |
|**Vis hele utgiftsrapporten ved tilbakedrilling**               | Velg dette alternativet for å vise alle utgifter for en reiseregningsrapport når du viser detaljene for det opprinnelige dokumentet for et bestemt bilag som ble generert da reiseregningen ble postert.              |
|**Forhåndsautorisering av reise er obligatorisk**                 | Velg dette alternativet for å kreve at en reiserekvisisjon er sendt og godkjent før en ansatt kan sende en reiseregning.                                                                    |
|**Tillat redigering av distribusjoner før postering**            | Velg om distribusjonen av en reiseregning kan redigeres før postering.                                                                                                                 |
|**Evaluer policyer for reiseregning og utlegg**                     | Velg når utgifter evalueres til å bestemme om en utgiftspolicy brytes. Utgifter kan kontrolleres for brudd når utgiftsregistrering er registerert og lagret eller utgiften er sendt til godkjenning. Policyreglene for kvitteringer påkrevd kontrolleres når utgiftslinjen er lagret.                   |
|**Tillat konserninterne utgiftslinjer**                         | Velg om du vil tillate registrering av utgifter for andre juridiske enheter i en reiseregning.                                                                                                          |
|**Tillat redigering av valutakursen for kredittkortutgifter** | Velg dette alternativet for å tillate at brukeren redigerer valutakursen for importerte kredittkortet utgifter.                                                                        |
|**Hierarkifelt på flere nivåer som skal vises**                  | Velg hvilke godkjennerfelt som skal vises når rapporten arbeidsflyten tildelingen utgiftstypen er angitt som hierarkiet og valg av dimensjonssetthierarki er satt til å bruke godkjenningshierarkiet utgifter med flere nivåer. Når det brukes med flere nivåer godkjenningshierarkiet for arbeidsflyt, blir de valgte feltene vises og redigeres i reiseregningen. |
|**Angi kredittkortnummer for ansatt (oppdatering juli 2017)**     | Velg om et tall med 15 eller 16 tegn kan være angitt og lagret i feltet **Kort-ID** på siden **Kredittkort** for en ansatt.                                                                          |

### <a name="financial"></a>Økonomisk

| **Felt**                                                            | **Beskrivelse**     |
|----------------------------------------------------------------------|------------------------------------|
|**Daglig journalnavn i finans**                                         | Velg navnet på finansjournalen som godkjente reiseregninger posteres til.            |
|**Aktiver tilbakebetaling av avgifter fra utgifter**                                  | Velg dette alternativet for å aktivere avgiftsfradrag for utgifter kvalifisert. Dette alternativet kan ikke aktiveres hvis amerikansk merverdiavgift og use tax-regler er aktivert.      |
|**Poster forskudd direkte**                                     | Velg dette alternativet for å postere et godkjent forskudd når prosessen for betaling og overføring er fullført. Hvis det ikke er merket av for dette alternativet, genererer prosessen for betaling og overføring en ikke-postert økonomijournal. |
|**Riktig regnskapsdato under postering**                             | Velg dette alternativet for å oppdatere regnskapsdatoen under postering av utgifter hvis den gjeldende perioden er på vent eller lukket. Regnskapsdatoen settes til den neste åpne perioden.   |
|**Tillat gruppering av transaksjoner basert på en motkonto som er angitt i betalingsmetoden**      | Velg dette alternativet for å summere utgiftstransaksjoner for en reiseregningsrapport, basert på motkontoen som er angitt i betalingsmåten for utgiftene.   
|**Avgift inkludert**                                                   | Velg dette alternativet for å inkludere merverdiavgift i utgiftsbeløpet som standard.             |
|**Frigi disposisjoner i reiserekvisisjoner som lukkes**            | Velg dette alternativet for å frigi disponert midler når en godkjent reiserekvisisjon er lukket.                                                                                   |
|**Tillatt innsending av reiserekvisisjon ved budsjettoverskridelse av budsjettregister og prosjektbudsjett** | Velg dette alternativet for å tillate at ansatte sender reiserekvisisjoner for godkjenning som enten overskrider tillatt budsjettet som er angitt i budsjettjournalen eller tillatte budsjettet for et prosjekt.            |
|**Tillat innsending av reiseregning ved budsjettoverskridelse av budsjettregister og prosjektbudsjett**    | Velg dette alternativet for å tillate at ansatte sender reiseregninger for godkjenning som enten overskrider tillatt budsjettet som er angitt i budsjettjournalen eller tillatte budsjettet for et prosjekt.                |
|**Tillat godkjenning av reiseregning bare ved budsjettoverskridelse for budsjettregister**                | Velg dette alternativet for å tillate godkjennerne å godkjenne reiseregningsrapporter som overskrider det tillatte budsjettet som er angitt i budsjettjournalen.                                                                       |

### <a name="per-diem"></a>Kostgodtgjørelse

| **Felt**                             | **Beskrivelse**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**Minste timeantall for kostgodtgjørelse**           | Angi standard minste antall timer som en arbeidstaker må jobbe i løpet en dag for å kunne reiserelaterte utgifter for ett døgn.  Denne verdien brukes kun som en standardverdi for feltet Minimum timer per døgn.                                                                                      |
|**Måltidsprosent**                          | Angi standardprosent for kostgodtgjørelse for måltider som brukes på de første og siste dag i den reiserelaterte utgiften når feltet **Beregn måltidsreduksjon etter** er satt til enten **Måltidstype per dag** eller **Antall måltider per dag**. Arbeidsdagen på første og siste dag kan være kortere enn en standard arbeidsdag. Kostgodtgjørelsen for disse dagene kan derfor være forskjellig fra standardbeløpet. Hvis prosenten er satt til 0, blir fradrag for første og siste dag 0,00. |
|**Hotellprosent**                        | Angi standardprosent for kostgodtgjørelse for hoteller som brukes på de første og siste dag i den reiserelaterte utgiften. Arbeidsdagen på første og siste dag kan være kortere enn en standard arbeidsdag. Kostgodtgjørelsen for disse dagene kan derfor være forskjellig fra standardbeløpet. Hvis prosenten er satt til 0, blir fradrag for første og siste dag 0,00.                                              |
|**Prosent, annet**                        | Angi standardprosent for kostgodtgjørelse for diverse utgifter som brukes på de første og siste dag i den reiserelaterte utgiften. Arbeidsdagen på første og siste dag kan være kortere enn en standard arbeidsdag. Kostgodtgjørelsen for disse dagene kan derfor være forskjellig fra standardbeløpet. Hvis prosenten er satt til 0, blir fradrag for første og siste dag 0,00.                                                                                                     |
|**Reduksjon i prosent for frokost** | Angi beløpet som er reduksjon i kostgodtgjørelse for frokost. Hvis den ansatte for eksempel får gratis frokost, kunne du velge å redusere beløpet for kostgodtgjørelsen med 10 prosent.                               |
|**Reduksjon i prosent for lunsj**    | Angi beløpet som er reduksjon i kostgodtgjørelse for lunsj. Hvis den ansatte for eksempel får gratis lunsj, kunne du velge å redusere beløpet for kostgodtgjørelsen med 15 prosent.                                       |
|**Reduksjon i prosent for middag**   | Angi beløpet som er reduksjon i kostgodtgjørelse for middag. Hvis den ansatte for eksempel får gratis middag, kunne du velge å redusere beløpet for kostgodtgjørelsen med 25 prosent.                                     |
|**Beregn måltidsreduksjon etter**         | Velg hvordan systemet skal beregne reduksjonen i kostgodtgjørelse for måltider ved å velge om reduksjonen er basert på typen måltider per tur eller per dag, eller hvis reduksjonen er basert på hvor mange måltider tillatt per dag.|
|**Satsavrunding**                  | Velg avrundingstypen som skal brukes for kostgodtgjørelse. Hvis du velger normal avrunding, avrundet eventuelle kostgodtgjørelse utgifter som har et beløp på 0,50 opp til 1,00 og eventuelle kostgodtgjørelse utgifter som har et beløp som er mindre enn 0,50 rundes ned til 0,00.                                                                                              |
|**Baser satsberegning på**         | Velg om et kostgodtgjørelsesbeløp er basert på en kalenderdag eller en 24-timers periode.       |

### <a name="fax-cover-pages"></a>Faksforsider

| **Felt**                      | **Beskrivelse**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **Instruksjoner**                   | Angi instruksjoner som ansatte må følge når de oppretter en forside for en faks som brukes til å sende kvitteringer som er knyttet til en reiseregningsrapport. Klikk knappen **Oversettelser** for å skrive inn språkspesifikk tekst som skal vises basert på språket. |
|**Bruker-ID (strekkodeinformasjon)** | Velg dette alternativet for å lagre en ansatts unike ID i strekkoden som er brukt på forsiden av telefaksen.                 |
|**Strekkode**                      | Velg strekkoden som skal brukes på forsiden av telefaksen. Strekkodene 39 og 128 støttes med reiseregninger.               |

### <a name="anti-corruption"></a>Antikorrupsjon

| **Felt**                             | **Beskrivelse**      |
|---------------------------------------|------------------------------------------------------------------------|
|**Vis antikorrupsjonsattestering**   | Velg dette alternativet for å vise antikorrupsjonsteksten når du oppretter en ny reiseregningsrapport. Bestemt utgiftskategorier kan aktiveres som krever at antikorrupsjonsattestation velges i reiseregningen. For eksempel kan en gavekategori knyttet til en offentlig offisielle utgift kreve at den ansatte bekrefter at utgiften oppfyller firmapolicy som er knyttet til offentlige myndighetspersoner. |
|**Antikorrupsjonsmelding for innsender** | Skriv inn teksten som skal vises for den ansatte når du oppretter en ny reiseregningsrapport. Klikk knappen **Oversettelser** for å skrive inn språkspesifikk tekst som skal vises basert på språket.         |
|**Antikorrupsjonsmelding for godkjenner**  | Skriv inn teksten som skal vises for godkjenneren når du oppretter en ny reiseregningsrapport. Klikk knappen **Oversettelser** for å skrive inn språkspesifikk tekst som skal vises basert på språket.        |

