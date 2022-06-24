---
title: Periodiske oppgaver i Regelmessig kontraktsfakturering
description: Denne artikkelen beskriver de periodiske oppgavene som er tilgjengelige i Regelmessig kontraktfakturering.
author: JodiChristiansen
ms.date: 04/29/2022
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
ms.openlocfilehash: d834d1d7aa34448b4ef21606974538eb294b5d7d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904795"
---
# <a name="periodic-tasks-in-recurring-contract-billing"></a>Periodiske oppgaver i Regelmessig kontraktsfakturering

Denne artikkelen beskriver de periodiske oppgavene som er tilgjengelige i Regelmessig kontraktfakturering.

## <a name="generate-invoice"></a>Generer faktura

Bruk siden **Generer faktura** til å opprette regelmessige månedlige massefakturaer fra informasjonen du definerer på sidene **Alle faktureringsplaner** og **Vis faktureringsdetaljer**. Når det opprettes en faktura, oppdateres varebeskrivelsen for behandlingslinjen for salgsordren med varebeskrivelsen og start- og sluttdatoene for planlinjen som faktureres.

## <a name="generate-invoice-batch-processing"></a>Satsvis behandling av generering av faktura

Bruk siden **Satsvis behandling av generering av faktura** til å opprette regelmessige fakturaer gjennom en gjentakende satsvis prosess. Parameterne som er tilgjengelige, er de samme som parameterne på siden **Generer faktura**, men de kan lagres i en satsvis prosess som kan kjøres flere ganger.

## <a name="price-update"></a>Prisoppdatering

Bruk prisoppdateringsverktøyet til å oppdatere prisene på flere varer på flere faktureringsplaner med en enkelt handling. Prisene kan oppdateres basert på enten en angitt prosent eller et angitt beløp. Listen over linjer viser bare de gjeldende enhetsprisene for varene. Prisene vises ikke etter prisoppdateringen.

Legg merke til følgende punkt om verktøyet for prisoppdatering:

- Hvis salgsordren for et bestemt år allerede er opprettet (det vil si hvis varene er fakturert), berøres ikke prisen på linjevarene.
- Prisoppdateringsverktøyet kan brukes for linjeelementer som har statusen **Aktiv** eller **På vent**. For varer som er satt på vent, må alternativet **Juster tidsplan** være satt til **Nei** da venting ble plassert.
- Prisoppdateringsverktøyet kan ikke brukes for linjeelementer som bruker varer, som bruker eskalering, milepælfakturering eller inntektsdeling.

### <a name="price-update-example"></a>Eksempel på prisoppdatering

Det opprettes en fakturaplan, og en fornyelsesvare blir lagt til. Enhetsprisen er USD 750. Det første året for varen betales 15. desember 2021. Faktureringsplanen opprettes for perioden fra 1. januar til 31. desember 2022.

På fornyelsestidspunktet opåpretter **Generer faktura**-prosessen salgsordren for året 2022. Når prisoppdateringsverktøyet er kjørt, oppdateres prisen fra USD 750 til USD 800.

Salgsordren og fakturaplanen for 2022 berøres ikke, og enhetsprisen forblir USD 750, fordi faktureringsplanen for 2022 allerede er fakturert. Fakturaplanlinjen og linjedetaljene for 2023 oppdateres til USD 800 fordi fakturaplanen for 2023 ikke er fakturert ennå.

### <a name="update-prices--flat-pricing-method"></a>Oppdater priser – Flat prissettingsmetode

Når du oppdaterer priser for varer som bruker flatprissettingsmetode, kan du angi en prosent eller et beløp for å øke prisen.

Følg denne fremgangsmåten for å kjøre prisoppdateringsverktøyet for varer som bruker flatprissettingsmetoden.

1. Velg **Flat**-prissettingsmetode på verktøysiden **Prisoppdatering**.
2. Velg økningsmetoden som brukes til å oppdatere prisen på varene, i feltet **Økningsmetode**.
3. Avhengig av økningsmetoden du har valgt, kan du angi prosentsatsen i **Prosent**-feltet eller beløpet i **Beløp**-feltet.
4. I hurtigkategorien **Poster som skal inkluderes** bruker du **Filter**-knappen til å legge til datafiltre.
5. Velg **Vis forhåndsvisning** for å vise postene.
6. Hvis du ikke vil behandle noen av linjene, merker du dem og velger **Fjern**.
7. Velg **OK**.

### <a name="update-prices--standard-pricing-method"></a>Oppdater priser – Standard prissettingsmetode

Hvis prisen på en vare er endret i vareposten, kan den oppdateres for alle fakturaplanlinjer hvis varen bruker standard prissettingsmetode.

1. Velg **Standard**-prissettingsmetode på verktøysiden **Prisoppdatering**.
2. I hurtigkategorien **Poster som skal inkluderes** bruker du **Filter**-knappen til å legge til datafiltre.
3. Velg **Vis forhåndsvisning** for å vise postene.
4. Hvis du ikke vil behandle noen av linjene, merker du dem og velger **Fjern**.
5. Velg **OK**.

## <a name="mass-hold-processing"></a>Massesperrebehandling

Bruk siden **Massesperre** til å bruke holdalternativer på mange faktureringsplaner samtidig.

Hvis du bare vil sette én faktureringsplan eller én fakturaplanlinje på vent, åpner du siden **Alle faktureringsplaner** og velger **Sett på vent**. Hvis du vil fjerne en venting, bruker du siden **Fjern sperre**.

### <a name="put-billing-schedules-on-hold"></a>Sette faktureringsplaner på vent

Hvis du vil sette flere faktureringsplaner på vent, følger du trinnene nedenfor.

1. På siden **Massesperre** angir du **Prosessalternativ**-feltet til **Bruk sperre**.
2. Velg en årsakskode i feltet **Årsakskode**.
3. Angi alternativet **Juster planlegging**:

    - **Ja** – Hvis du velger **Ja**, angir du en ventingsdato i feltet **Sperredato**. Alle faktureringsplanlinjer etter at sperredatoen er fjernet.
    - **Nei** – Fakturaplanlinjene er ikke endret. Bare statusen er endret. Den oppdateres til **På vent**.

4. I hurtigkategorien **Poster som skal inkluderes** bruker du **Filter**-knappen til å legge til datafiltre.
5. Velg **Vis forhåndsvisning** for å vise postene.
6. Hvis du ikke vil behandle noen av linjene, merker du dem og velger **Fjern**.
7. Velg **OK**.

Når du går tilbake til listen over faktureringsplaner, bør du se at statusen for faktureringsplanene er endret til **På vent**.

### <a name="remove-a-hold-from-several-billing-schedules"></a>Fjerne en venting fra flere faktureringsplaner

1. På siden **Massesperre** angir du **Prosessalternativ**-feltet til **Fjern sperre**.
2. Angi en årsakskode i feltet **Årsakskode**.
3. I feltet **Fjern dato** velger du datoen da sperren skal fjernes.
4. Sett feltene **Fortsettelsesdato** og **Dato for utsettelse** etter behov. Fortsettelsesdatoen legges til alle linjer som kan utsettes.
5. I hurtigkategorien **Poster som skal inkluderes** bruker du **Filter**-knappen til å legge til datafiltre.
6. Velg **Vis forhåndsvisning** for å vise postene.
7. Hvis du ikke vil behandle noen av linjene, merker du dem og velger **Fjern**.
8. Velg **OK**.

> [!NOTE]
> Hvis du vil fjerne en sperre, må du angi verdien **Fjern overstyring av sperre for brukergruppe** på siden **Faktureringsparametere for regelmessig kontrakt**.

En fakturalinje har for eksempel startdatoen 1. februar 2022 og sluttdatoen 28. februar 2022. Faktureringsbeløpet er USD 200. **Sperredato**-feltet er satt til 10. februar 2022. Derfor justeres februarperioden for å utelate en hvilken som helst dato etter 10. februar. Den nye perioden er fra 1. februar til og med 9. februar, og beløpet USD 64.29 (gjennom daglig fordeling). Alle faktureringsplanlinjer på eller etter 10. februar fjernes.

Hvis **Fjern sperre**--prosessen er fullført, og feltet **Fjern dato** er satt til 10. februar 2022, vil det være to faktureringsperioder. Den første faktureringsperioden er fra 1. februar til og med 9. februar, og beløpet er USD 64.29. Den andre faktureringsperioden er fra 10. februar til og med 28. februar, og beløpet er USD 135.71.

## <a name="mass-termination-processing"></a>Masseavslutningsbehandling

Bruk siden **Masseavslutning** til å avslutte faktureringsplanlinjer som for øyeblikket vises, ved å angi en oppsigelsesdato.

Hvis du bruker omsetnings- og utgiftshenvisninger, kan du bruke faktureringsplaner der feltet **Avslutningsdato** er satt til **Juster tidsplan** på siden **Alle faktureringsplaner** er kvalifisert for refusjon.

Faktureringsplaner som bruker MEA-funksjonaliteten (multiple element allocation), vises ikke på siden **Masseavslutning**. Du kan likevel avslutte en enkelt faktureringsplan ved å bruke oppsigelsesfunksjonaliteten i faktureringsplanen.

> [!NOTE]
> Fakturaplanlinjer som for øyeblikket er inkludert i partiet **Generer faktura**, er ikke tilgjengelige for denne prosessen.

Hvis du vil ha mer informasjon om hvert felt og prosessen, kan du se [Avslutte faktureringsplaner](terminate-billing-schedule.md).

## <a name="mass-archive-process"></a>Massearkiveringsprosess

Bruk siden **Massearkivering** til å arkivere flere faktureringsplaner. Bare avsluttede faktureringsplaner kan arkiveres.

Når en faktureringsplan er arkivert, skjer følgende hendelser:

- Statusen endres til **Arkivert**.
- Faktureringsplanene er permanent låst.
- Fakturaplanlinjene er ikke lenger tilgjengelige på forespørselssider.

> [!NOTE]
> Arkivering av en fakturaplan er en permanent handling og kan ikke tilbakeføres.

Følg disse trinnene for å arkivere faktureringsplaner.

1. Angi en sluttdato for fakturering på siden **Massearkivering** i feltet **Sluttdato for fakturering**. Hvis du vil vise alle avsluttede faktureringsplaner, lar du dette feltet stå tomt.
2. Hvis du vil begrense postene som vises, bruker du **Filter**-knappen i hurtigfanen **Poster som skal inkluderes**.
3. Velg **Vis forhåndsvisning**.
4. Hvis du ikke vil arkivere noen av postene, merker du dem og velger **Fjern**.
5. Velg **OK** for å arkivere postene på siden.

## <a name="mass-stubbing-process"></a>Masseavbrytelsesprosess

Bruk siden **Masseavbrytelse** til å merke alle valgte fakturaplanlinjer som fakturert (avbrytelse) eller ikke fakturert (tilbakeført avbrytelse). Avbrytelse eller tilbakeført avbrytelse utføres som oftest på importerte fakturaplanlinjer som tidligere er fakturert i et annet system. Tidsplanlinjer for avbrutt fakturering vises som avbrutt, og det vil ikke bli opprettet en faktura for kunden.

### <a name="stub-records"></a>Poster for avbrytelse

1. På siden **Masseavbrytelse**, i feltet **Behandlingsalternativer**, velger du **Avbrytelse**.
2. I **Fristdato** angir du en frist for å angi linjene du vil bruke prosessen på. Bare poster der startdatoen for fakturering er på eller før den angitte fristen, vises.
3. Velg **Vis forhåndsvisning** for å vise linjene du vil avbryte.
4. Hvis du vil utelate en linje fra prosessen, merker du den og velger **Fjern**.
5. Velg **Prosess** for å avbryte linjene.

### <a name="reverse-stub-records"></a>Tilbakeføre avbrutte poster

1. På siden **Masseavbrytelse**, i feltet **Behandlingsalternativer**, velger du **Tilbakefør avbrytelse**.
2. I **Fristdato** angir du en frist for å angi linjene du vil bruke prosessen på. Bare poster der startdatoen for fakturering er på eller før den angitte fristen, vises.
3. Velg **Vis forhåndsvisning** for å vise linjene du vil tilbakeføre avbrudd.
4. Hvis du vil utelate en linje fra prosessen, merker du den og velger **Fjern**.
5. Velg **Prosess** for å tilbakeføre avbrytelse av linjene.

## <a name="update-completion-date-process"></a>Oppdater fullføringsdatoprosess

Bruk siden **Oppdater fullføringsdato** til å oppdatere fullføringsdatoen for bestemte milepælvarer for flere faktureringsplaner eller brukere. Du kan også oppdatere fullføringsprosenten for varer på milepælmaler som bruker metoden **Prosent fullført**.

1. På siden **Oppdater fullføringsdato** kan du gå til **Milepælbehandling** og velge **Oppdater fullføringsprosent**.
2. I **Prosentbeløp**-feltet angir du den totale prosenten som er fullført.
3. Velg varenummeret som er relatert til milepælmalen.
4. I hurtigkategorien **Poster som skal inkluderes** velger du **Filter** for å velge en spesifikk verdi for **Sluttbrukerkonto**, **Faktureringsplannummer**, **Varenumre** som et filterkriterium.
5. Velg **OK** for behandle endringen. Når behandlingen er fullført, blir det lagt til en ny linje i milepæltildelingen. Denne linjen representerer prosenten som er fullført for milepælmalen.

## <a name="unbilled-revenue-mass-processing"></a>Massebehandling av ufakturert inntekt

Bruk siden **Massebehandling av ufakturert inntekt** for å opprette journaloppføringen for ufakturert regning eller avbryt journaloppføringen for én eller flere valgte faktureringsplaner eller faktureringsdetaljlinjer.

- **Opprett journaloppføring** – Opprett journaloppføringer for ufakturert regning for flere faktureringsplanlinjer. Bruk knappen **Filter** i hurtigkategorien **Poster som skal inkluderes** for å velge området med poster som skal vises i listen. Listen viser bare fakturaplanlinjer som journaloppføringer for ufakturerte inntekt ikke er opprettet for. De innledende journaloppføringene blir opprettet. Når det gjelder utsettelsesvarer, opprettes også utsettelsesplaner.
- **Stubjournaloppføring** – Merk fakturaplanlinjene som de journaloppføringene for ufakturerte allerede er opprettet for. Dette alternativet brukes hvis journaloppføringen for ufakturerte allerede er postert i et annet system. Den merker journalen for ufakturerte som avbrutt og posterer ikke en transaksjon til økonomimodulen.
- **Tilbakefør stubjournaloppføring** – Tilbakefør stubjournaloppføringer som er behandlet. Hvis det ble gjort en feil under behandlingen for **Stubjournaloppføring**, fjerner dette alternativet avmerkingsboksen **Avbrutt** for faktureringsplanlinjen.
- **Linjenummer for faktureringsdetalj for stub** – Bruk denne prosessen når ufakturert inntekt ble behandlet i et eksternt system, og noen av faktureringsdetaljlinjene er allerede fakturert. Denne prosessen sikrer at riktig beløp vises i kontoene for ufakturerte inntekter.
- **Linjenummer for faktureringsdetalj for snudd stub** – Tilbakefør alle handlinger for **Linjenummer for faktureringsdetalj for stub**.

Feltet **Journalnavn** brukes til å postere **Opprett journaloppføringer** til økonomimodulen.

> [!NOTE]
> Stubprosessen posterer ikke beløp til økonomimodulen. Feltet **Journalnavn** er ikke tilgjengelig for alle stub- og reserver stub-prosesser.

### <a name="unbilled-revenue-stub-example"></a>Eksempel på avbrutt ufakturert inntekt

En fakturaplan er definert for ett år, fra oktober 2021 til september 2022. Den ufakturerte inntekten ble allerede behandlet i et eksternt system. Ni måneder av fakturaplanen er allerede fakturert. Beløpet for hver faktureringsperiode er USD 250. I begynnelsen av året blir det totale beløpet som er postert til ufakturert inntekt, USD 3000. Etter ni måneder er USD 2250 allerede fakturert, og ufakturert inntekt på USD 750 gjenstår.

Følg denne fremgangsmåten for å konfigurere faktureringsplanen der det gjenstår bare tre måneder med ufakturert inntekt gjenstår.

1. På siden **Vis faktureringsdetaljer** oppretter du en faktureringsplan for perioden fra oktober 2021 til september 2022, varenummer S0001, og et beløp USD 250 per måned.
2. Velg **Opprett journaloppføring** for faktureringsplanen. Beløpet på USD 3000 posteres til ufakturert inntekt.
3. Velg **Linjenummer for faktureringsdetalj for stub**, og angi en transaksjonsdato for juni 2022 (ni måneder). Fakturaplanlinjene vises ikke i forhåndsvisningen. Linjene som påvirkes, er basert på transaksjonsdatoen.
4. Velg **OK**.

De første ni månedene som er fakturert, avbrytes.

[![Vis avbrytelse av fakturadetaljlinjer.](./media/01_View-billing-detail-stub.png)](./media/01_View-billing-detail-stub.png)

USD 3000 tilbakeføres fra ufakturert inntekt, og USD 750 i ufakturert inntekt som gjenstår, posteres. Hvis du vil vise posteringer av ufakturert inntekt, velger du **Revisjon av journaloppføring som ikke er fakturert** i kategorien **Fornyinger** for linjedetaljsiden.

[![Revisjon av journaloppføring som ikke er fakturert.](./media/02_Unbilled-rev-journal-audit.png)](./media/02_Unbilled-rev-journal-audit.png)

> [!NOTE]
> Ufakturert inntekstjournaloppføring kan opprettes for en hvilken som helst fornyelsesperiode, forutsatt at alle faktureringsdetaljlinjene fra den forrige perioden er fakturert. En fakturaplanlinje har for eksempel en månedlig faktureringsfrekvens for en 12-måneders periode, fra januar til desember 2021. Linjen har tre termer: første termin, andre termin (januar til desember 2022) og en tredje termin (januar til desember 2023). Når fakturaen er opprettet for alle fakturadetaljlinjene fra de innledende 12 månedene i 2021, kan journaloppføringen for ufakturert inntekt opprettes for den andre perioden.
>
> For utsatte varer som bruker funksjonen for ufakturert inntekt, behandles faktureringslinjen og rabattlinjene. For disse varene opprettes den ufakturerte journaloppføringen, og den utsatte planen for fakturalinjen og rabattlinjen opprettes.
>
> Journaloppføringene som er opprettet for varer som ikke kan utsettes, og varer som kan utsettes, posterer en kreditt til ulike inntektskontoer.
