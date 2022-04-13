---
title: Inntekts- og utgiftsutsettelser i Abonnementsfakturering
description: Dette emnet forklarer hvordan du definerer inntekts- og utgiftsutsettelser i Abonnementsfakturering.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 5ff8d2f4663c53bf6dece1ef9af6609d5f0c5b50
ms.sourcegitcommit: cf7d4af11bf85638ee831a28ea5ee1a1e041a675
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/04/2022
ms.locfileid: "8544510"
---
# <a name="revenue-and-expense-deferrals-in-subscription-billing"></a>Inntekts- og utgiftsutsettelser i Abonnementsfakturering

Dette emnet forklarer hvordan du definerer og bruker inntekts- og utgiftsutsettelser i Abonnementsfakturering. Utsettelsesplaner er alltid basert på og avhenger av et underliggende opprinnelsesdokument eller faktureringsplan. Fordi de er opprettet basert på standardverdier, kan de ikke angis eller opprettes separat.

Prosessen med å definere og bruke inntekts- og utgiftsutsettelser skjer på flere sider:

- På siden **Parametere for inntekts- og utgiftsutsettelse** kan du definere bedriftsinnstillingene.
- På siden **Standarder for utsettelse** kan du definere standardkontoene og -malene som skal brukes til utsettelsesplanene.
- På sidene **Utsettelsesmaler** og **Hendelsesbaserte utsettelsesmaler** kan du definere malene som skal brukes for utsettelsesplanene.
- På siden **Alle utsettelsesplaner** kan du vise og redigere en hvilken som helst utsettelsesplan.

Inntekts- og utgiftsutsettelser kan brukes sammen med regelmessig kontraktfakturering.

## <a name="revenue-and-expense-deferral-parameters"></a>Parametere for inntekts- og utgiftsutsettelse

Siden **Parametere for inntekts- og utgiftsutsettelse** inneholder følgende felter.

| Felt | Beskrivelse |
|---|---| 
| **Tidsplan**-fanen | |
| Lik per periode | <p>Angi om antall dager i en periode skal brukes når beløpet per periode beregnes for en utsettelsesplan:</p><ul><li>**Ja** – Beløpet for hver periode er det samme, uansett antall dager i perioden. Delvise perioder (for eksempel perioder ved begynnelsen eller slutten av en utsettelsesplan) blir fordelt.</li><li>**Nei** – Beløpet beregnes på grunnlag av antall dager i hver periode.</li></ul><p>Du kan overstyre denne innstillingen på transaksjonsnivå.</p> |
| Alternativ for salgsrabattutsettelse | <p>Angi om det skal opprettes separate utsettelsesplaner for rabatt- og salgsordrebeløpene:</p><ul><li>**Separat plan for rabatt** – Rabattbeløpet holdes separat fra inntektsbeløpet.<p>I dette tilfellet opprettes to utsettelsesplaner når en salgsordre opprettes og deretter posteres. Rabatt- og inntektsbeløpene posteres til ulike utsettelseskontoer.</p></li><li>**Slå sammen rabatt med inntekt** – Rabattbeløpet kombineres med inntektsbeløpet. Én utsettelsesplan opprettes, og både rabattbeløpet og inntektsbeløpet posteres til samme utsettelseskonto.<p>I dette tilfellet opprettes én utsettelsesplan når en salgsordre opprettes og deretter posteres. Både rabattbeløpet og inntektsbeløpet posteres til samme utsettelseskonto.</p></li></ul><p>**Merk:** Hvis du vil bruke rabatter på varer som bruker funksjonen for ufakturert inntekt, velger du alternativet **Separat plan for rabatt**. Rabatter kan deretter brukes på alle varer, uansett om funksjonen for ufakturert inntekt brukes eller ikke. Hvis alternativet **Slå sammen rabatt med inntekt** er valgt, kan ikke rabatter brukes på varer som bruker funksjonen for ufakturert inntekt.</p> |
| Alternativ for innkjøpsrabattutsettelse | <p>Velg om det skal opprettes separate utsettelsesplaner for rabatt- og bestillingsbeløpene:</p><ul><li>**Separat plan for rabatt** – Rabattbeløpet holdes separat fra utgiftsbeløpet.<p>I dette tilfellet opprettes to utsettelsesplaner når en bestilling opprettes og deretter posteres. Rabatt- og utgiftsbeløpene posteres til ulike utsettelseskontoer.</p></li><li>**Slå sammen rabatt med inntekt** – Rabattbeløpet kombineres med utgiftsbeløpet. Én utsettelsesplan opprettes, og både rabattbeløpet og utgiftsbeløpet posteres til samme utsettelseskonto.<p>I dette tilfellet opprettes én utsettelsesplan når en bestilling opprettes og deretter posteres. Både rabattbeløpet og utgiftsbeløpet posteres til samme utsettelseskonto.</p></li></ul> |
| Konsolider foregående perioder | <p>Angi om utsettelsesplanlinjer for tidligere perioder skal konsolideres:</p><ul><li>**Ja** – Hvis startdatoen for utsettelsen er i en periode før transaksjonsdatoen, kombineres alle beløp opp gjennom perioden til transaksjonsdatoen i én enkelt utsettelsesplanlinje.</li><li>**Nei** – Beløpene fra alle perioder beholdes i separate utsettelsesplanlinjer.<p>Hvis den startdatoen for utsettelsen er i den samme perioden som eller en senere periode enn transaksjonsdatoen, har ikke dette alternativet noen virkning.</p></li></ul><p>Denne innstillingen kan oppdateres på transaksjonsnivå.</p> |
| Standard startdato for utsettelse | <p>Velg regelen som skal brukes til å bestemme startdatoen for utsettelsesplanen:</p><ul><li>**Transaksjonsdato** – Bruk transaksjonsdatoen som startdato:</li><li>**Starten av gjeldende måned** – Bruk den første i gjeldende måned som startdato. Hvis transaksjonsdatoen er den første i måneden, er den første i gjeldende måned startdatoen.</li><li>**Starten av neste måned** – Bruk den første i neste måned som startdato. Hvis transaksjonsdatoen er den første, brukes transaksjonsdatoen. Ellers brukes den første i neste måned.</li><li>**Regel på 15** – Hvis transaksjonsdatoen er mellom den første og den femtende, bruker du den første i gjeldende måned som startdato. Hvis transaksjonsdatoen er den sekstende eller senere, brukes den første i neste måned som startdato.</li></ul><p>Du kan oppdatere denne innstillingen på transaksjonsnivå.</p> |
| Kortsiktig utsettelsesmetode | <p>Velg den kortsiktige utsettelsesmetoden **Ingen**, **Løpende perioder** eller **Fast år**.</p><p>|
| Posteringsmetode for utsettelse | <p>Velg metoden som skal brukes til å opprette utsettelsestransaksjoner:</p><ul><li>**Balanse** – Bruk balanseposteringsmetoden til å opprette utsettelsestransaksjoner.</li><li>**Resultat** – Bruk metoden for postering av resultat til å opprette utsettelsestransaksjoner. Når transaksjoner posteres, kan du gå gjennom fakturabilaget for å se tilleggsoppføringene som balanserer de innledende førings- og motføringsbeløpene.</li></ul> |
| Tilbakefør resultat på kreditt | <p>**Merk:** Dette feltet er bare tilgjengelig når feltet **Metode for utsettelsespostering** er satt til **Resultat**.</p><p>Angi om resultatbeløpene skal tilbakeføres når en tilbakeføring, avslutning eller refusjon er brukt for en faktureringsplan eller salgsordre:</p><ul><li>**Ja** – Tilbakefør resultatbeløpene og bruk et kredittjusteringsbeløp i utsettelsesplanen.<p>Hvis tilbakeføringen skjer halvveis i faktureringsperioden, blir beløpene fordelt.</p></li><li>**Nei** – Ingen tilbakeføringstransaksjon opprettes for resultatet når en tilbakeføring, avslutning eller refusjon er brukt for en faktureringsplan eller salgsordre.</li></ul> |
| Fanen **Inntektsføring** | |
| Poster økonomijournal automatisk | <p>Angi om journaloppføringer som er opprettet etter inntekts- og utgiftsutsettelser, skal posteres automatisk:</p><ul><li>**Ja** – Poster automatisk journaloppføringer som er opprettet etter inntekts- og utgiftsutsettelser.<p>**Tips:** Ved å velge **Ja** kan du forhindre inkonsekvenser i regnskapet som forårsakes av manuelle endringer i bilag.</p></li><li>**Nei** – Journaloppføringer som er opprettet etter inntekts- og utgiftsutsettelser, posteres ikke automatisk. Du må postere journalene manuelt.</li></ul> |
| Oppsummer føringsjournal | <p>Angi om inntektsføringsbilag skal konsolideres som standard:</p><ul><li>**Ja** – Opprett ett enkelt bilag for alle inntektsføringslinjer som har samme dato. Alle linjene i et bilag som har samme konto, blir konsolidert på én enkelt linje.</li><li>**Nei** – Opprett et bilag for hver inntektsføringslinje.</li></ul><p>Du kan oppdatere denne innstillingen på siden **Behandling av inntektsføring**.</p> |
| Standard journalnavn | Velg journalnavnet for journaler som er opprettet fra omsetnings- og utgiftsutsettelsesprosesser, for eksempel behandling av inntektsføring. |
| Beskrivelse for føringsjournallinje | <p>Velg beskrivelsen som vises i beskrivelsen av journalbilagslinjen:</p><ul><li>**Planlinjedatoer** – Vis planlinjedatoene i journallinjebeskrivelsen.</li><li>**Opprinnelige transaksjonsdetaljer** – Vis den opprinnelige transaksjonsinformasjonen i journallinjebeskrivelsen.<p>**Eksempel:** USMF-0001, CIV-00839, programvareinntekter</p></li></ul> |
| Fanen **Nummerserier** | Bruk denne fanen til å angi standardverdier for nummerserier for leie. Veiviseren for generering av nummerserier brukes til å generere og tilordne nummerserier automatisk. Du trenger ikke å endre nummerserien med mindre du vil gjøre manuelle endringer i de genererte nummerseriene. |
| Tidsplannummer | Nummeret som er en serie, som brukes til utsettelsesplaner. |

## <a name="deferral-templates"></a>Maler for utsettelse

Bruk siden **Maler for utsettelse** til å definere lineære maler som brukes til utsettelsesplaner.

Her er noen av fordelene ved å bruke en mal:

* Lengden på utsettelsen beregnes automatisk.
* Du tillater utsettelsesplaner som har perioder der inntektsføringen hoppes over.
* Du kan automatisere utsettelser ved å tilordne malen til et produkt, en produktgruppe, en produktkategori, kunder eller en kundegruppe. Maltilordningen utføres fra siden **Standarder for utsettelse**.

Flere periodehyppigheter er tilgjengelige for maler: daglige, månedlige eller regnskapsperioder.

Mallinjene består av en type (**Inntektsført** eller **Hoppet over**) og periodelengden. Linjer som er hoppet over, har et beløp på 0 (null) på utsettelsesplanlinjene. Denne virkemåten kan være nyttig hvis du ikke vil inntektsføre inntekt i alle perioder.

### <a name="create-a-deferral-template"></a>Opprett en utsettelsesmal

Hvis du vil opprette en utsettelsesmal, følger du trinnene nedenfor.

1. Velg **Ny** på siden **Utsettelsesmaler**.
2. Skriv inn et navn i **Mal**-feltet.
3. Angi en beskrivelse i **Beskrivelse**-feltet.
4. Velg periodefrekvensen i **Periodefrekvens**-feltet.
5. Velg **Legg til** for å legge til en linje øverst i listen over linjer, eller velg **Tilføy** for å legge til en linje nederst i listen.
6. Velg periodetypen i **Type**-feltet.
7. Angi lengden på perioden i **Periodelengde**-feltet.
8. Gjenta trinn 5 til og med 7 for hver ekstra linje du trenger.
9. Velg **Lagre**.

## <a name="deferral-defaults"></a>Standarder for utsettelse

Bruk siden **Standarder for utsettelse** til å definere standard utsettelseskontoer for varer og til å tilordne standardmaler til varer som kan utsettes. Du kan også definere utsettelseskontoer for tillegg og tilordne maler til de tilleggene som kan utsettes.

**Utsettelse etter vare**

For transaksjoner som har en vare (for eksempel salgsordrer), kan du tilordne kontoer og maler til bestemte varer og kunder. Disse innstillingene brukes som standardverdier når en transaksjon utsettes. Hvis du vil at transaksjonen skal kunne utsettes som standard, må du definere varene på siden **Varer som kan utsettes**.

**Utsettelse etter konto**

For transaksjoner som ikke har varer (for eksempel økonomijournaler), kan du angi utsettelseskontoene. Når disse kontoene brukes på en transaksjonslinje, merkes transaksjonen automatisk som utsatt. Den tilsvarende malen og inntektsføringskontoen blir tilordnet transaksjonslinjen.

**Alle transaksjonstyper (for eksempel på fanene Salgsordre, Innkjøp og Økonomijournal)**

Kontoene på siden er hovedkontoene som ikke har finansdimensjoner. Finansdimensjonene i inntektsføringskontoen kommer fra kunden eller varen basert på organisasjonen.

Hver mallinje må ha enten en lineær mal eller en hendelsesbasert mal. Den kan ikke ha begge deler.

### <a name="for-sales-orders"></a>For salgsordrer

Følg denne fremgangsmåten for å angi standardverdiene for utsettelse for salgsordrer.

1. Velg utsettelsestypen på **Salgsordre**-fanen.
2. Velg **Legg til** for å legge til en linje.
3. I feltet **Varekode** velger du varekoden. Varekoden bestemmer hvordan standardverdiene for utsettelse skal brukes.
4. Angi hvordan varekoden skal brukes:

    * Hvis feltet **Varekode** er angitt til **Tabell** eller **Gruppe**, velger du varerelasjonen i feltet **Varerelasjon**.
    * Hvis **Varekode**-feltet er angitt til **Kategori**, velger du kategorirelasjonen i **Kategorirelasjon**.
    * Hvis **Varekode**-feltet er angitt til **Alle**, gjelder standardverdiene for alle aktuelle poster.

5. Angi hvordan kontokoden skal brukes:

    * Hvis feltet **Kontokode** er angitt til **Tabell** eller **Gruppe**, velger du kontorelasjonen i feltet **Kontorelasjon**.
    * Hvis **Kontokode**-feltet er angitt til **Alle**, gjelder kontoen for alle poster.

6. Velg hovedkontoen for utsettelsen i **Hovedkonto**-feltet.
7. Hvis feltet **Metode for utsettelsespostering** er angitt til **Resultat**, velger du den opprinnelige inntektskontoen i feltet **Opprinnelig inntektskonto** og motkontoen for inntekt i feltet **Motkonto for inntekt**.
8. Hvis feltet **Kortsiktig utsettelsesmetode** er angitt til **Løpende perioder** eller **Fast år**, velger du kontoen for kortsiktig utsettselse i feltet **Konto for kortsiktig utsettelse**.
9. For en mal kan du velge **Legg til** for å legge til en linje.
10. I feltet **Varekode** velger du varekoden.
11. Angi hvordan varekoden skal brukes:

    * Hvis feltet **Varekode** er angitt til **Tabell** eller **Gruppe**, velger du varerelasjonen i feltet **Varerelasjon**.
    * Hvis **Varekode**-feltet er angitt til **Kategori**, velger du kategorirelasjonen i feltet **Kategorirelasjon**.
    * Hvis **Varekode**-feltet er angitt til **Alle**, gjelder standardverdiene for alle aktuelle poster.

12. Angi hvordan kontokoden skal brukes:

    * Hvis feltet **Kontokode** er angitt til **Tabell** eller **Gruppe**, velger du kontorelasjonen i feltet **Kontorelasjon**.
    * Hvis **Kontokode**-feltet er angitt til **Alle**, gjelder kontoen for alle aktuelle poster.
    * Velg den lineære malen i feltet **Lineær mal** eller den hendelsesbaserte malen i feltet **Hendelsesbasert mal**.

13. Velg **Lagre**.

### <a name="for-purchase-orders"></a>For bestillinger

Følg denne fremgangsmåten for å angi standardverdiene for utsettelse for bestillinger.

1. Velg utsettelsestypen på **Innkjøp**-fanen.
2. Velg **Legg til** for å legge til en linje.
3. I feltet **Varekode** velger du varekoden.
4. Angi hvordan varekoden skal brukes:

    * Hvis feltet **Varekode** er angitt til **Tabell** eller **Gruppe**, velger du varerelasjonen i feltet **Varerelasjon**.
    * Hvis **Varekode**-feltet er angitt til **Kategori**, velger du kategorirelasjonen i feltet **Kategorirelasjon**.
    * Hvis **Varekode**-feltet er angitt til **Alle**, gjelder standardverdiene for alle aktuelle poster.

5. Angi hvordan kontokoden skal brukes:

    * Hvis feltet **Kontokode** er angitt til **Tabell** eller **Gruppe**, velger du kontorelasjonen i feltet **Kontorelasjon**.
    * Hvis **Kontokode**-feltet er angitt til **Alle**, gjelder kontoen for alle aktuelle poster.

6. Velg hovedkontoen for utsettelsen i **Hovedkonto**-feltet.
7. Hvis feltet **Metode for utsettelsespostering** er angitt til **Resultat**, velger du den opprinnelige inntektskontoen i feltet **Opprinnelig inntektskonto** og motkontoen for inntekt i feltet **Motkonto for inntekt**.
8. Hvis feltet **Kortsiktig utsettelsesmetode** er angitt til **Løpende perioder** eller **Fast år**, velger du kontoen for kortsiktig utsettselse i feltet **Konto for kortsiktig utsettelse**.
9. For en mal velger du **Legg til** for å legge til en linje. 
10. I feltet **Varekode** velger du varekoden.
11. Angi hvordan varekoden skal brukes:

    * Hvis feltet **Varekode** er angitt til **Tabell** eller **Gruppe**, velger du varerelasjonen i feltet **Varerelasjon**.
    * Hvis **Varekode**-feltet er angitt til **Kategori**, velger du kategorirelasjonen i feltet **Kategorirelasjon**.
    * Hvis **Varekode**-feltet er angitt til **Alle**, gjelder standardverdiene for alle aktuelle poster.

12. Angi hvordan kontokoden skal brukes:

    * Hvis feltet **Kontokode** er angitt til **Tabell** eller **Gruppe**, velger du kontorelasjonen i feltet **Kontorelasjon**.
    * Hvis **Kontokode**-feltet er angitt til **Alle**, gjelder kontoen for alle aktuelle poster.
    * Velg den lineære malen i feltet **Lineær mal** eller den hendelsesbaserte malen i feltet **Hendelsesbasert mal**.

13. Velg **Lagre**.

### <a name="for-general-journals"></a>For økonomijournaler

Følg denne fremgangsmåten for å angi standardverdiene for oppføringer i økonomijournalen.

1. Velg fanen **Økonomijournal**.
2. For en utsettelse velger du **Legg til** for å legge til en linje.
3. Hvis feltet **Kortsiktig utsettelsesmetode** er angitt til **Løpende perioder** eller **Fast år**, velger du kontoen for kortsiktig utsettselse i feltet **Konto for kortsiktig utsettelse**.
4. Velg utsettelseskontoen i **Utsettelseskonto**-feltet.
5. Velg inntektsføringskontoen i **Inntektsføringskonto**-feltet.
6. Hvis feltet **Metode for utsettelsespostering** er angitt til **Resultat**, velger du den opprinnelige inntektskontoen i feltet **Opprinnelig inntektskonto** og motkontoen for inntekt i feltet **Motkonto for inntekt**.
7. Velg den lineære malen i feltet **Lineær mal** eller den hendelsesbaserte malen i feltet **Hendelsesbasert mal**.
8. Velg **Lagre**.

### <a name="for-free-text-invoices"></a>For fritekstfakturaer

Følg denne fremgangsmåten for å angi standardverdiene for fritekstfakturaer.

1. Velg fanen **Fritekstfaktura**.
2. For en utsettelse velger du **Legg til** for å legge til en linje.
3. Angi hvordan kontokoden skal brukes:

    * Hvis feltet **Kontokode** er angitt til **Tabell** eller **Gruppe**, velger du kontorelasjonen i feltet **Kontorelasjon**.
    * Hvis **Kontokode**-feltet er angitt til **Alle**, gjelder kontokoden for alle aktuelle poster.

4. Velg utsettelseskontoen i **Utsettelseskonto**-feltet.
5. Hvis feltet **Kortsiktig utsettelsesmetode** er angitt til **Løpende perioder** eller **Fast år**, velger du kontoen for kortsiktig utsettselse i feltet **Konto for kortsiktig utsettelse**.
6. Velg inntektsføringskontoen i **Inntektsføringskonto**-feltet.
7. Hvis feltet **Metode for utsettelsespostering** er angitt til **Resultat**, velger du den opprinnelige inntektskontoen i feltet **Opprinnelig inntektskonto** og motkontoen for inntekt i feltet **Motkonto for inntekt**.
8. Velg den lineære malen i feltet **Lineær mal** eller den hendelsesbaserte malen i feltet **Hendelsesbasert mal**.
9. Velg **Lagre**.

### <a name="for-invoice-journals"></a>For fakturajournaler

Følg denne fremgangsmåten for å angi standardverdiene for oppføringer i fakturajournalen.

1. Velg fanen **Fakturajournal**.
2. For en utsettelse velger du **Legg til** for å legge til en linje.
3. Angi hvordan kontokoden skal brukes:

    * Hvis feltet **Kontokode** er angitt til **Tabell** eller **Gruppe**, velger du kontorelasjonen i feltet **Kontorelasjon**.
    * Hvis **Kontokode**-feltet er angitt til **Alle**, gjelder kontokoden for alle aktuelle poster.

4. Velg utsettelseskontoen i **Utsettelseskonto**-feltet.
5. Hvis feltet **Kortsiktig utsettelsesmetode** er angitt til **Løpende perioder** eller **Fast år**, velger du kontoen for kortsiktig utsettselse i feltet **Konto for kortsiktig utsettelse**.
6. Velg inntektsføringskontoen i **Inntektsføringskonto**-feltet.
7. Hvis feltet **Metode for utsettelsespostering** er angitt til **Resultat**, velger du den opprinnelige inntektskontoen i feltet **Opprinnelig inntektskonto** og motkontoen for inntekt i feltet **Motkonto for inntekt**.
8. Velg den lineære malen i feltet **Lineær mal** eller den hendelsesbaserte malen i feltet **Hendelsesbasert mal**.
9. Velg **Lagre**.

### <a name="items-that-are-deferred-by-default"></a>Varer som er utsatt som standard

Bruk siden **Varer utsatt som standard** til å definere hvilke varer som skal være utsatt som standard. Du kan definere transaksjonstypene som varene skal utsettes for. Du kan angi om en enkelt vare skal utsettes, eller hele varegruppen eller -kategorien.

Når du definerer varer som utsatt, velger du standardkontoene og -malene på siden **Standarder for utsettelse**. Hvis kontoene og malene ikke er valgt, blir ikke transaksjonslinjer utsatt der disse varene er angitt.

For varer som er utsatt basert på salgs- eller innkjøpskategorien de er tilknyttet, er de innstillingene for utsettelse basert på kategorien. Hvis kategorien ikke er valgt i feltet **Kategorirelasjon**, brukes imidlertid innstillingene for utsettelse for kategorien som er høyere i rang. Du kan for eksempel legge til en **Hjemmevideo**-salgskategori, men ikke en **TV**-salgskategori. Når du legger til en utsettelsesvare som er tilknyttet **TV**-kategorien, brukes innstillingene for utsettelse i **Hjemmevideo**-kategorien for varen.

### <a name="set-up-deferred-items"></a>Definer utsatte varer

Følg denne fremgangsmåten for å definere varer som er utsatt som standard.

1. På siden **Varer utsatt som standard** velger du fanen du vil bruke: **Salgsordre** eller **Innkjøp**.
2. Velg **Legg til** for å legge til en linje.
3. I feltet **Varekode** velger du varekoden.
4. Angi hvordan varekoden skal brukes:

    * Hvis feltet **Varekode** er angitt til **Gruppe** eller **Tabell**, velger du varerelasjonen i feltet **Varerelasjon**.
    * Hvis **Varekode**-feltet er angitt til **Kategori**, velger du kategorirelasjonen i feltet **Kategorirelasjon**.

5. Gjenta trinn 2 til og med 4 for hver ekstra linje du trenger.
6. Velg **Lagre**.

## <a name="deferred-charges"></a>Utsatte tillegg

Bruk siden **Utsettelsestillegg** til å definere hvilke tillegg som skal utsettes som standard.

> [!NOTE]
> * For øyeblikket er utsatte tillegg bare tilgjengelige for salgsordrer.
> * Tillegg kan kun utsettes på linjenivå. Hvis du vil utsette et tillegg på salgsordrehodenivå, kan du definere tillegget som en utsatt vare på en egen linje i salgsordren.
> * Hvis du vil utsette et tillegg for en fritekstfaktura, må du angi tillegget som en separat utsatt fakturalinje.
> * Denne funksjonaliteten er ikke tilgjengelig for støttetillegg og funksjonaliteten for inntektsdeling.

### <a name="set-up-deferred-charges"></a>Definer utsatte tillegg

Følg disse trinnene for å definere utsatte tillegg.

1. På siden **Utsettelsestillegg** velger du **Legg til** for å legge til en linje.
2. Velg tilleggskoden i **Tilleggskode**-feltet.
3. Velg tilleggsrelasjonen i **Tilleggsrelasjon**-feltet.
4. Gjenta trinn 1 til og med 3 for hver ekstra linje du trenger.
5. Velg **Lagre**.

## <a name="event-based-deferral-templates"></a>Hendelsesbaserte maler for utsettelse

Bruk siden **Hendelsesbaserte utsettelsesmaler** til å definere hendelsesbaserte utsettelsesmaler som du kan bruke i utsettelsestransaksjoner og tilordne på siden **Standarder for utsettelse**.

### <a name="create-an-event-based-template"></a>Opprett en hendelsesbasert mal

Hvis du vil opprette en hendelsesbasert mal, følger du trinnene nedenfor.

1. Velg **Ny** på siden **Hendelsesbaserte utsettelsesmaler**.
2. I **Mal**-feltet angir du et unikt navn på malen.
3. Angi en beskrivelse i **Beskrivelse**-feltet.
4. Velg tildelingstypen i feltet **Tildelingstype**.

    * **Variabelt beløp** – Tildel et bestemt beløp for hver linje som angis.
    * **Likt beløp** – Tildel det samme beløpet for hver linje som angis. 
    * **Prosent** – Tildel et beløp som er basert på prosentverdien som angis for hver linje.
    * **Fullføringsprosent** – Tildel en akkumulert fullføringsverdi for hver linje som angis.
    * **Variabelt antall** – Tildel et bestemt antall for hver linje som angis.

5. Angi alternativet **Opprett separate hendelser per enhet** til **Ja** hvis du vil at hver hendelseslinje skal fordeles likt etter antallet enheter i fakturatransaksjonen. Angi det til **Nei** hvis du ikke vil dele hendelseslinjene.
6. Velg utløpskontoen i **Utløpskonto**-feltet.
7. Velg **Legg til** for å legge til en linje øverst i listen over linjer, eller velg **Tilføy** for å legge til en linje nederst i listen.
8. I **Beskrivelse**-feltet skriver du inn en beskrivelse av hendelsen.
9. Hvis **Tildelingstype**-feltet er satt til **Prosent**, angir du tildelingsprosenten i **Tildelingsprosent**-feltet. Prosenten må være mellom 0 (null) og 100. Hvis du lar feltet **Tildelingsprosent** stå tomt, regnes prosenten som 0. Summen av alle prosentverdiene vises i feltet **Total prosent** feltet nederst på siden og må være lik 100.
10. Angi hvor mange måneder hendelsen er gyldig, i feltet **Måneder til utløp**. Utløpsdatoen i transaksjonsutsettelsen angis automatisk basert på denne verdien.
11. Merk av for **Inntektsføring når postert** for å inntektsføre inntekt automatisk når transaksjonen posteres. Hvis du ikke merker av i boksen, må inntekten føres manuelt.
12. I feltet **Inntektsføringskonto** velger du inntektsføringskontoen for hendelsen hvis hendelsen bruker en annen konto enn hele utsettelsesplanen. Dette feltet brukes sammen med avmerkingsboksen **Inntektsføring når postert**.
13. Gjenta trinn 7 til og med 12 for hver ekstra linje du trenger.
14. Velg **Lagre**.
