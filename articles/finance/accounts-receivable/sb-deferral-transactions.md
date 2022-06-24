---
title: Utsettelsestransaksjoner i Abonnementsfakturering
description: Denne artikkelen beskriver de forskjellige transaksjonene som kan brukes i utsettelsestransaksjoner som en del av inntekts- og utgiftsutsettelser i Abonnementsfakturering.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: c3862f1a250bf8e56303975b5c6a3560cd84c1e7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872593"
---
# <a name="deferral-default-transactions"></a>Utsettelsesstandardtransaksjoner

Denne artikkelen beskriver transaksjonene som tillater inntekts- og utgiftsutsettelser. Utsettelsesplaner er alltid basert på og avhenger av et opprinnelsesdokument eller en faktureringsplan. Tidsplaner for utsettelser opprettes basert på standarder og kan ikke angis eller opprettes separat.

## <a name="sales-order-transaction-deferral"></a>Utsettelse av salgsordretransaksjon

Bruk siden **Utsettelser** eller **Opprett kreditnota** til å angi eller redigere utsettelsesparametere for en salgsordrelinje.

> [!NOTE]
> Når en salgsordre opprettes fra en faktureringsplan, er alle verdier på siden **Utsettelser** eller **Opprett kreditnota** skrivebeskyttet, og utsettelsesparameterne kan ikke redigeres. Hvis du vil redigere verdiene, bruker du siden **Endre tidsplan**.

### <a name="edit-deferral-options"></a>Rediger utsettelsesalternativer

Følg denne fremgangsmåten for å redigere utsettelsesalternativene for en linje.

1. Opprett en salgsordretransaksjon.
2. Velg linjen, og velg deretter **Utsettelser**.
3. På siden **Transaksjonsutsettelse** må alternativet **Utsatt** være angitt til **Ja**. Rediger de andre feltene etter behov.
4. Velg **Forhåndsvisning** for å forhåndsvise utsettelsesplanen.
5. Hvis du gjorde noen endringer i transaksjonsutsettelsen, velger du **OK** og går tilbake til transaksjonssiden.
6. Fullfør og poster transaksjonen.

Når transaksjonen er postert, åpner du siden **Alle utsettelsesplaner** for å vise utsettelsesplanen.

### <a name="create-a-credit-note"></a>Opprett en kreditnota

Hvis du vil opprette en kreditnota, gjør du følgende:

1. Opprett en salgsordretransaksjon.
2. Velg varen du vil opprette en kreditnota for, under **Salgsordrelinjer**.
3. Velg **Salgsordrelinje** \> **Ny**, og velg deretter **Kreditnota**.
4. Velg **Utsettelser**.
5. På siden **Utsettelse av salgsordretransaksjon** setter du alternativet **Juster eksisterende tidsplan** til **Ja** for varen.
6. I feltet **Justert tidsplan** velger du utsettelsesplanen du vil bruke kreditnotaen på.
7. Oppdater feltene **Beregn dato på nytt** og **Sluttdato** etter behov.
8. Velg **OK**.
9. Fullfør posteringen av salgsordretransaksjonen.

### <a name="purchase-orders-and-purchase-invoices"></a>Bestillinger og innkjøpsfakturaer

Hvis du vil bruke utsettelsesfunksjonaliteten for en bestilling, må du generere fakturaen først. Deretter kan du bruke siden **Ventende leverandørfakturaer** til å redigere eller legge til utsettelsesvarer. Du kan ikke redigere eller legge til utsettelser direkte på en bestilling.

1. Bruk siden **Ventende leverandørfakturaer** til å angi en leverandørfaktura.

    Når du angir en linje, angis utsettelsen automatisk for varen eller innkjøpskategorien du velger. Denne utsettelsen er basert på oppsettet av utsettelser på siden **Standarder for utsettelse**. Utsettelsene kan redigeres eller legges til på distribusjonsnivået.

3. På innkjøpslinjen velger du **Finans \> Fordel beløp**.
4. For hvet fordelingsbeløp velger du **Utsettelser**. Når fakturaen posteres, opprettes det en utsettelsesplan for hver fordeling som en utsettelse er definert for.

### <a name="tax"></a>Avgift

I noen tilfeller kan mva-beløpet være fullstendig eller delvis ikke-gjenopprettelig. Hvis avgiftsbeløpet på en utsettelseslinje inneholder et beløp som ikke kan gjenopprettes, inkluderes det ikke-gjenopprettbare avgiftsbeløpet i det utsettelsesbare tidsplanbeløpet når fakturaen posteres.

### <a name="variance"></a>Avvik

Hvis beløpet på leverandørfakturalinjen avviker fra beløpet på bestillingslinjen, opprettes det avviksfordelinger. Hvis linjen er utsatt, settes finanskontoen for disse fordelingene til utsettelseskontoen, og beløpene tas med i det utsettelsesbare planbeløpet når fakturaen posteres. Disse fordelingene kalles for **Prisavvik** og **Kostnadsavvik**.

### <a name="general-journals-and-invoice-journals"></a>Økonomijournaler og fakturajournaler

Bruk siden **Utsettelser** til å angi utsettelsesparameterne for en journalbilagslinje. Du kan også forhåndsvise utsettelsesplanen for lineære utsettelser. Når du angir en linje, angis utsettelsen automatisk basert på oppsettet for utsettelseskontoer på siden **Standarder for utsettelse**. Du kan manuelt endre utsettelsesalternativene for hver linje. Når journalbilaget posteres, opprettes utsettelsesplanen.

#### <a name="post-and-transfer"></a>Poster og overfør

Hvis du vil postere journalbilaget, bruker du kommandoen **Poster og overfør**. Utsettelsesalternativene følger linjen som bilaget gjelder for. Når det gjelder bilag som ikke inneholder feil, opprettes det en utsettelsesplan bilaget er utsatt. Når det gjelder et bilag som har en feil og overføres, overføres også eventuelle utsettelsesalternativer.

#### <a name="tax"></a>Avgift

I noen tilfeller kan mva-beløpet være fullstendig eller delvis ikke-gjenopprettelig. Hvis avgiftsbeløpet på en utsettelseslinje inneholder et beløp som ikke kan gjenopprettes, inkluderes det ikke-gjenopprettbare avgiftsbeløpet i det utsettelsesbare tidsplanbeløpet når fakturaen posteres.

## <a name="free-text-invoice-transaction-deferral"></a>Transaksjonsutsettelse på fritekstfaktura

Bruk siden **Utsettelser** til å angi utsettelsesparameterne for en linjefordeling på en fritektsfaktura. Når en fordeling er angitt, angis utsettelsen automatisk basert på utsettelsesinnstillingene på siden **Standarder for utsettelse**.

## <a name="fields"></a>Felt

Siden **Transaksjonsutsettelse** inneholder følgende felter.

| Felt | Beskrivelse |
|-------|-------------|
| Utsatt | <p>Angi om linjen er en utsettelse:</p><ul><li>**Ja** – Linjen er en utsettelse.</li><li>**Nei** – Linjen er ikke en utsettelse.</li></ul><p>Hvis du setter alternativet til **Ja**, er ikke alternativet **Juster eksisterende tidsplan** tilgjengelig. For varer og tillegg som allerede er definert som utsatt, er dette alternativet satt til **Ja**. For varer og tillegg som ikke er definert som utsatt som standard, må du sette dette alternativet til **Ja**.</p> |
| Juster eksisterende tidsplan | <p>Angi om linjen er en justering av en eksisterende utsettelsesplan:</p><ul><li>**Ja** – Den nye salgslinjen er en justering av en eksisterende utsettelsesplan. I dette tilfellet kan du velge en utsettelsesplan i feltet **Justert tidsplan**.</li><li>**Nei** – Den nye salgslinjen er ikke en justering av en eksisterende utsettelsesplan.</li></ul><p>Hvis du setter alternativet til **Ja**, er ikke alternativet **Utsatt** tilgjengelig.</p> |
| Justert tidsplan | <p>Velg utsettelsesplanen som linjen justerer. Alle verdiene på siden oppdateres deretter med verdiene fra den opprinnelige utsettelsesplanen. Disse verdiene kan ikke redigeres.</p><p>Dette feltet er bare tilgjengelig når alternativet **Juster eksisterende tidsplan** er angitt til **Ja**.</p> |
| Omberegningsdato | <p>Angi startdatoen for perioden som du vil omberegne det gjenstående beløpet fra. Standarddatoen er datoen for den neste ikke-førte perioden.</p><p>Dette feltet er bare tilgjengelig når alternativet **Juster eksisterende tidsplan** er angitt til **Ja**.</p> |
| Sluttdato | <p>Avhengig av typen utsettelse kan sluttdatoen kanskje ikke oppdateres:</p><ul><li>Angi den nye sluttdatoen for planen for en lineær utsettelse. Den eksisterende sluttdatoen for utsettelsesplanen er standardverdien.</li><li>For en hendelsesbasert utsettelse angir du sluttdatoen for kreditthendelseslinjen. Denne datoen kan være tom.</li></ul><p>Dette feltet er bare tilgjengelig når alternativet **Juster eksisterende tidsplan** er angitt til **Ja**.</p> |
| Faktureringsplannummer | <p>Faktureringsplannummeret.</p><p>Dette feltet er bare tilgjengelig for gjentakende kontraktfaktureringsplaner.</p> |
| Justeringsmetode for utsettelse | <p>Justeringsmetoden for utsettelsen. Verdien samsvarer med verdien på siden **Masseavslutningsbehandling** for den gjentakende kontraktfaktureringsplanen.</p><p>Dette feltet er bare tilgjengelig for gjentakende kontraktfaktureringsplaner.</p> |
| **Kontoer – Inntekt** | |
| Utsettelseskonto | <p>Utsettelseskontoen, som er posteringskontoen som vises på **Salgsordre**-siden.</p><p>Hvis linjen ikke er utsatt, er dette feltet tomt. I dette tilfellet er posteringskontoen standard inntektskonto.</p> |
| Føringskonto | <p>Angi kontoen som skal brukes når en utsettelse føres. Denne kontoen må være forskjellig fra utsettelseskontoen.</p><p>Når **Utsatt**-alternativet i utgangspunktet er satt til **Ja**, kopieres dimensjonsverdiene som brukes i utsettelseskontoen, til inntektsføringskontoen. Hvis dimensjonen i utsettelseskontoen ikke eksisterer for føringskontoen, blir den ignorert.</p> |
| Opprinnelig føringskonto | <p>Velg kontoen for den opprinnelige inntektsføringen. Standardverdien hentes fra siden **Standarder for utsettelse**.</p><p>Dette feltet er bare tilgjengelig når feltet **Metode for utsettelsespostering** er satt til **Resultat** på siden **Parametere for inntekts- og utgiftsutsettelse**.</p> |
| Motkonto for føring | <p>Velg kontoen for motpostering av inntektsføringen. Standardverdien hentes fra siden **Standarder for utsettelse**.</p><p>Dette feltet er bare tilgjengelig når feltet **Metode for utsettelsespostering** er satt til **Resultat** på siden **Parametere for inntekts- og utgiftsutsettelse**.</p> |
| **Kontoer – Rabatt** | Denne delen vises bare for utsatte varer. Den er skjult for utsatte tillegg. |
| Utsettelseskonto | <p>Angi kontonummeret for rabattutsettelsen. Standardverdien hentes fra siden **Standarder for utsettelse**.</p><p>Dette feltet er bare tilgjengelig når feltet **Alternativ for rabattutsettelse** er satt til **Separat plan for rabatt** på siden **Parametere for inntekts- og utgiftsutsettelse**, og det brukes en rabatt på linjen.</p> |
| Føringskonto | <p>Angi kontonummeret for rabattføringen. Standardverdien hentes fra siden **Standarder for utsettelse**.</p><p>Dette feltet er bare tilgjengelig når feltet **Alternativ for rabattutsettelse** er satt til **Separat plan for rabatt** på siden **Parametere for inntekts- og utgiftsutsettelse**, og det brukes en rabatt på linjen.</p> |
| Opprinnelig føringskonto | <p>Velg kontoen for den opprinnelige rabattføringen. Standardverdien hentes fra siden **Standarder for utsettelse**.</p><p>Dette feltet er bare tilgjengelig når feltet **Posteringsmetode for utsettelse** er satt til **Resultat** på siden **Parametere for inntekts- og utgiftsutsettelse**, og det brukes en rabatt på linjen.</p> |
| Motkonto for føring | <p>Velg kontoen for motpostering av inntektsføringen. Standardverdien hentes fra siden **Standarder for utsettelse**.</p><p>Dette feltet er bare tilgjengelig når feltet **Posteringsmetode for utsettelse** er satt til **Resultat** på siden **Parametere for inntekts- og utgiftsutsettelse**, og det brukes en rabatt på linjen.</p> |
| **Kontoer – Forbruk** | Denne delen vises bare for utsatte varer. Den er skjult for utsatte tillegg. |
| Utsettelseskonto | <p>Angi kontonummeret for forbruksutsettelsen.</p><p>For standardprodukter opprettes det to utsettelsesplaner:</p><ul><li>**Standardsalg** – En inntektsplan som har en kreditsaldo. I dette tilfellet velger du forbruksutsettelseskontoen.</li><li>**Forbruk** – En utgiftsplan for forbruk (solgte varers kost \[vareforbruk\]) som har en debetsaldo. I dette tilfellet velger du forbruksføringskontoen.</li></ul><p>Når fakturaen er postert, posteres forbruksbeløpet til den angitte forbruksutsettelseskontoen. Disse feltene er ikke tilgjengelige for servicevarer.</p> |
| Føringskonto | Angi kontonummeret for forbruksføringen. |
| Opprinnelig føringskonto | <p>Angi kontoen for det opprinnelige forbruksføringsbeløpet. Standardverdien hentes fra siden **Standarder for utsettelse**.</p><p>Dette feltet er bare tilgjengelig når feltet **Metode for utsettelsespostering** er satt til **Resultat** på siden **Parametere for inntekts- og utgiftsutsettelse**.</p> |
| Motkonto for føring | <p>Angi kontoen for motregningsbeløpet for forbruksføringen. Standardverdien hentes fra siden **Standarder for utsettelse**.</p><p>Dette feltet er bare tilgjengelig når feltet **Metode for utsettelsespostering** er satt til **Resultat** på siden **Parametere for inntekts- og utgiftsutsettelse**.</p> |
| **Planlegg** | |
| Planleggingstype | <p>Velg typen utsettelsesplan: **Lineær** (standard) eller **Hendelsesbasert**.</p><p>Alternativene som vises på siden, er basert på typen utsettelsesplan du velger.</p><p>Hvis standardmalen er angitt på siden **Standarder for utsettelse** for transaksjonslinjen, er typen utsettelsesplan basert på typen mal som er valgt.</p> |
| **Tidsplan – Lineær** | |
| Konsolider foregående perioder | <p>Angi om du vil konsolidere utsettelsesplanlinjer for tidligere perioder:</p><ul><li>**Ja** – Konsolider utsettelsesplanlinjene for tidligere perioder.</li><li>**Nei** – Ikke konsolider utsettelsesplanlinjene for tidligere perioder.</li></ul><p>Standardverdien hentes fra siden **Parametere for inntekts- og utgiftsutsettelse**.</p> |
| Lik per periode | <p>Angi om antall dager i hver periode er likt eller varierer etter periode:</p><ul><li>**Ja** – Hver periode har samme antall dager.</li><li>**Nei** – Perioder har ikke samme antall dager.</li></ul><p>Når du setter alternativet til **Nei**, vurderes antall dager i en periode når beløpet i hver periode for en utsettelsesplan beregnes.</p><p>Standardverdien hentes fra siden **Parametere for inntekts- og utgiftsutsettelse**.</p> |
| Planlegg fra mal | <p>Angi om utsettelsesplanen skal opprettes basert på en mal eller en sluttdato:</p><ul><li>**Ja** – Utsettelsesplanen opprettes basert på en mal.</li><li>**Nei** – Utsettelsesplanen opprettes basert på en sluttdato.</li></ul> |
| Mal | Velg utsettelsesmalen. |
| Overstyr startdato | <p>Angi om du vil overstyre startdatoen:</p><ul><li>**Ja** – Overstyr startdatoen med datoen du angir i **Startdato**-feltet.</li><li>**Nei** – Startdatoen er regelen **Standard startdato for utsettelse** som brukes på fakturadatoen som er angitt på siden **Postering av faktura**. Denne regelen kan angis på siden **Parametere for inntekts- og utgiftsutsettelse**.</li></ul> |
| Startdato for utsettelse | Angi startdatoen for utsettelsen. Transaksjonsdatoen er standardverdien. |
| Sluttdato for utsettelse | <p>Sluttdatoen for utsettelsen.</p><p>Denne datoen beregnes automatisk basert på utsettelsesmalen. Hvis ingen mal er valgt, må du angi datoen manuelt.</p> |
| **Tidsplan – Hendelsesbasert** | |
| Mal | <p>Velg den hendelsesbaserte malen. Dette feltet er valgfritt.</p><p>Hvis du velger en mal, overskriver verdiene fra malen alle hendelsesbaserte data og hendelseslinjer.</p> |
| Tildelingstype | <p>Velg tilordningstypen for hendelseslinjene:</p><ul><li>**Variable beløp** – Et spesifikt tildelingsbeløp angis for hver linje.</li><li>**Like beløp** – Beløpet tildeles likt for hver linje.</li><li>**Prosent** – Et beløp tildeles basert på prosentverdien som angis for hver linje.</li><li>**Fullføringsprosent** – En akkumulert fullføringsverdi angis for hver linje.</li><p>**Variabelt antall** – Et spesifikt tildelingsantall angis for hver linje.</li></ul><p>**Merk:** Hvis du vil velge **Fullføringsprosent**, må datoene være i stigende rekkefølge.</p> |
| **Opprett separate hendelser per enhet** | |
| Beskrivelse | <p>Angi om du vil skille hendelser per enhet:</p><ul><li>**Ja** – Skill hendelseslinjene, slik at det er én linje per antall.<p>Eksempel: Du har tre hendelseslinjer, og fakturaen har et antall på fire. I dette tilfellet har den resulterende utsettelsesplanen 12 linjer.</p></li><li>**Nei** – Ikke skill hendelseslinjene.</li></ul> |
| Utløpskonto | <p>Velg kontoen som brukes for førte utløpte linjer. Du kan velge kontoen etter at utsettelsesplanen er opprettet.</p><p>Hvis en utløpsdato er angitt for en hendelse, går føringsbeløpet til utløpskontoen i stedet for føringskontoen under føringsprosessen.</p> |
| **Tidsplan – Hendelsesbaserte linjer** | |
| Beskrivelse | En beskrivelse av hendelsen. |
| Sluttdato for utsettelse | <p>Velg sluttdatoen for hendelsen.</p><p>**Merk:** Hvis du velger en sluttdato, tømmes **Utløpsdato**-feltet. Du kan ikke bruke både en sluttdato og en utløpsdato.</p> |
| Utløpsdato | <p>Velg utløpsdatoen for hendelsen.</p><p>**Merk:** Hvis du velger en sluttdato, tømmes **Utløpsdato**-feltet. Du kan ikke bruke både en sluttdato og en utløpsdato.</p> |
| Antall | <p>Angi tildelingsantallet. Standardverdien for alle linjer er **0** (null). Hvis du oppdaterer antallet, må det totale antallet for alle linjene være likt eller mindre enn antallet som er angitt for linjeelementet på salgsordren.</p><p>Dette feltet er bare tilgjengelig når feltet **Tildelingstype** er satt til **Variabelt antall**.</p><p>Hvis antallet for linjeelementet på salgsordren endres slik at det er mindre enn det opprinnelige antallet og fakturaen opprettes, opprettes færre hendelsesbaserte linjer. Det totale tildelte antallet overskrider ikke antallet som er angitt på den opprinnelige salgsordren eller faktureringsplanen.</p> |
| Fordelingsprosent | <p>Angi fordelingsprosenten. Hvis **Tildelingstype**-feltet er satt til **Prosent** eller **Fullføringsprosent**, kan du angi en prosent manuelt. Ellers beregnes det automatisk.</p><p>Hvis feltet **Tildelingstype** er satt til **Prosent**, må summen av prosentverdiene være lik 100.</p> |
| Beløp | <p>Angi tildelingsbeløpet. Hvis **Tildelingstype**-feltet er satt til **Variable beløp** eller **Fullføringsprosent**, kan du angi et beløp manuelt.</p><p>Hvis **Tildelingstype**-feltet er satt til **Fullføringsprosent**, og du angir et beløp her, blir verdien i **Fullføringsprosent**-feltet beregnet automatisk.</p><p>På grunn av avrunding kan det hende at det beregnede beløpet ikke samsvarer med det som er angitt manuelt. Hvis du krever et nøyaktig beløp, angir du **Tildelingstype**-feltet til **Variable beløp**.</p> |
| Fullføringsprosent | <p>Angi fullføringsprosenten. Verdien må være mellom 0 (null) og 100.</p><p>Dette feltet er bare tilgjengelig når feltet **Tildelingstype** er satt til **Fullføringsprosent**.</p> |
| Fullføringsbeløp | <p>Den beregnede totalen for alle linjene i utsettelsesplanen.</p><p>Hvis **Tildelingstype-feltet** er satt til **Fullføringsprosent**, kan du angi et beløp manuelt. I dette tilfellet beregnes verdien i **Fullføringsprosent**-feltet basert på beløpet du angir.</p><p>På grunn av avrunding kan det hende at det beregnede beløpet ikke samsvarer med det som er angitt manuelt.</p><p>Dette feltet er bare tilgjengelig når feltet **Tildelingstype** er satt til **Fullføringsprosent**.</p> |
| Føring ved postering | <p>Angi om linjen skal føres automatisk så snart transaksjonen er postert:</p><ul><li>**Valgt** – Linjen føres automatisk så snart transaksjonen er postert.</li><li>**Ikke valgt** – Linjen føres ikke så snart transaksjonen er postert.</li></ul> |
| Føringskonto | <p>Angi føringskontoen for hendelsen hvis kontoen er forskjellig fra kontoen som brukes for hele utsettelsesplanen.</p><p>Du kan bruke dette feltet sammen med alternativet **Føring ved postering**.</p> |
