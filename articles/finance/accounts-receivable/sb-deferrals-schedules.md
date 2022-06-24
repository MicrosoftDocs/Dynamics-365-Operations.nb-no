---
title: Utsettelsesplaner i inntekts- og utgiftsutsettelser
description: Denne artikkelen beskriver utsettelsesplaner i inntekts- og utgiftsutsettelser.
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
ms.openlocfilehash: 093005f9b66d7ce741689b55612f006fa5123910
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903370"
---
# <a name="deferral-schedules"></a>Utsettelsesplaner

Utsettelsesplaner opprettes etter at en transaksjon er postert.

Du kan bruke siden **Alle utsettelsesplaner** eller **Aktive utsettelsesplaner** til å gå gjennom detaljene for en utsettelsesplan. Hvilken informasjon om vises, avhenger av typen utsettelsesplan (lineær eller hendelsesbasert) og transaksjonstypen. Den omfatter utsettelsesplanlinjene og totalbeløpene for utsettelsesplanen. Du kan bruke siden til å endre utsettelsesplanen.

## <a name="recognize-revenue"></a>Føre inntekt

> [!NOTE]
> - Start på trinn 1 for å føre inntekt for én utsettelsesplan.
> - Start på trinn 2 for å føre inntekt for flere utsettelsesplaner.

1. På siden **Alle utsettelsesplaner**, i rutenettet **Tidsplanlinjer**, velger du linjene du vil føre, og velger deretter **Før**.
2. På siden **Føringsbehandling** setter du feltet **Handling for føringskonto** til **Opprett føringsjournal**.
3. Velg fristdatoen i **Fristdato**-feltet. Behandlingen omfatter bare linjer der sluttdatoen er tidligere enn eller lik den valgte fristdatoen.
4. Velg **Filtrer**, og legg til datafiltre slik at listen bare viser de ønskede postene.
5. Velg **Vis forhåndsvisning** for å vise linjene.
6. Velg eventuelle linjer du ikke vil behandle, i listen over linjer, og velg deretter **Fjern**.
7. Velg om du vil summere føringsjournaloppføringen.
8. I delen **Transaksjonsdato** kan du overstyre transaksjonsdatoen med en bestemt dato for å behandle transaksjonen. Transaksjonsdatoen kan angis for lukkede perioder.
9. Hvis du vil foreta behandlingen som en del av et parti, velger du **Parti**. I dialogboksen **Satsvis behandling** angir du parameterne for partiet og velger deretter **OK** for å gå tilbake til siden **Føringsbehandling**. Inntektsføringen behandles senere, når partiet behandles.
10. Velg **Prosess**. Hvis du ikke la til transaksjonen i et parti, behandles alle linjene umiddelbart. Ellers behandles linjene når partiet behandles.

## <a name="modify-a-schedule"></a>Endre en tidsplan

Hvis du vil endre en utsettelsesplan, følger du trinnene nedenfor.

1. På siden **Alle utsettelsesplaner** velger du utsettelsesplanen og deretter velger du **Regnskap \> Endre tidsplan**.
2. På siden **Endre tidsplan** redigerer du alternativene du vil endre. Avhengig av utsettelsesplanen kan det hende at du ikke kan redigere alle alternativene.
3. Velg **Forhåndsvisning** for å se gjennom endringene i utsettelsesplanen.
4. Velg **OK**.

### <a name="straight-line-deferral-schedules"></a>Lineære utsettelsesplaner

Hvis utsettelsesplanen ikke har noen førte eller eksternt posterte linjer, kan du endre hele utsettelsesplanen, inkludert startdatoen.

Hvis utsatthetsplanen har førte eller eksternt posterte linjer, og du endrer utsettelsesplanen, vil den resulterende virkemåten til utsettelsesplanen være avhengig av omberegningsdatoen og den utsatte sluttdatoen for førte linjer. Som standard bestemmer den første perioden som ikke ble ført, den utsatte sluttdatoen.

Hvis du vil bruke føringsdatoen, velger du en av følgende verdier i feltet **Start på tidsplan**: 
- **Oppsamling** – Beløpet etter at alle førte linjer er omberegnet.
- **Tilbakeføring** – Alle linjer etter omberegningsdatoen tilbakeføres ved å bruke det angitte journalnavnet og posteringsdatoen. Beløpet etter omberegningsdatoen omberegnes deretter.

Hvis det brukes en mal, ignoreres periodene som hoppes over, og malen brukes bare til å beregne sluttdatoen.

### <a name="event-based-deferral-schedules"></a>Hendelsesbaserte utsettelsesplaner

For en hendelsesbasert utsettelsesplan kan du endre alle ikke-førte linjer.

Hvis utsettelsesplanen har førte eller eksternt posterte linjer, kan du ikke endre malen eller tildelingstypen for utsettelsesplanen. Når du endrer en eksisterende utsettelsesplan, kan du ikke endre verdien i feltet **Opprett separate hendelser per enhet**.

Hvis en linje er ført eller postert eksternt, er det merket av for **Ført**.

## <a name="modify-a-deferral-or-recognition-account"></a>Endre en utsettelses- eller føringskonto

Følg denne fremgangsmåten for å endre utsettelses- eller føringskontoen for en utsettelsesplan.

1. På siden **Alle utsettelsesplaner** velger du utsettelsesplanen og deretter velger du **Regnskap \> Endre konto**.
2. På siden **Endre konto** velger du kontoen du vil endre (utsettelse, kortsiktig eller føring).
3. Velg den nye kontoen i feltet **Ny konto**.
4. Velg om endringer i kontoen skal opprette justeringsjournaloppføringer.
5. Hvis du velger **Ja** i det forrige trinnet, velger du journalnavnet i **Journalnavn**-feltet og angir transaksjonsdatoen i **Transaksjonsdato**-feltet.
6. Velg **OK**.

## <a name="put-a-deferral-schedule-on-hold"></a>Sett en utsettelsesplan på vent

Hvis du vil sette en utsettelsesplan på vent, følger du trinnene nedenfor.

1. På siden **Alle utsettelsesplaner** velger du utsettelsesplanen og deretter velger du **Vent \> Sett på vent**.
2. På siden **Sett på vent** velger du om du vil overføre saldoen fra utsettelseskontoen eller ventekontoen.
3. Hvis du valgte å overføre saldoen, velger du journalnavnet i **Journalnavn**-feltet, velger ventekontoen i feltet **På vent-konto** og angir transaksjonsdatoen i feltet **Transaksjonsdato**.
4. Velg **OK**.

## <a name="remove-a-hold-from-a-deferral-schedule"></a>Fjern en venting fra en utsettelsesplan

Følg denne fremgangsmåten hvis du vil oppheve på vent-statusen for en utsettelsesplan.

1. I listen **Alle utsettelsesplaner** velger du utsettelsesplanen og deretter velger du **Vent \> Avslutt venting**.
2. Velg journalnavnet i **Journalnavn**-feltet.
3. Angi transaksjonsdatoen i **Transaksjonsdato**-feltet.
4. Velg **OK**.

## <a name="cancel-unrecognized-amounts"></a>Annuller ukjente beløp

> [!NOTE]
> Alle linjer som allerede er ført eller eksternt postert, utelates fra denne prosessen.

Hvis du vil annullere ikke-førte beløp i en utsettelsesplan, følger du trinnene nedenfor.

1. På siden **Alle utsettelsesplaner** velger du utsettelsesplanen og deretter velger du **Avbryt \> Ikke-førte beløp**.
2. På siden **Annuller ukjent beløp** velger du om du vil opprette annulleringsoppføringer.
3. Hvis du valgte å opprette annulleringsoppføringer, velger du journalnavnet i **Journalnavn**-feltet, velger annulleringskontoen i feltet **Annulleringskonto** og angir transaksjonsdatoen i feltet **Transaksjonsdato**.
4. Velg **OK**.

## <a name="cancel-a-completed-schedule"></a>Avbryt en fullført tidsplan

Bruk siden **Alle utsettelsesplaner** til å tilbakeføre alle førte eller eksternt posterte beløp, og avbryte utsettelsesplanen for å hindre videre føring.

Hvis du vil avbryte en hel utsettelsesplan, følger du trinnene nedenfor.

1. På siden **Alle utsettelsesplaner** velger du utsettelsesplanen og deretter velger du **Avbryt \> Fullfør tidsplan**.
2. På siden **Annuller hele tidsplanen** velger du om du vil opprette annulleringsoppføringer.
3. Hvis du valgte å opprette annulleringsoppføringer, velger du journalnavnet i **Journalnavn**-feltet, velger kontoen i feltet **Annulleringskonto** og angir transaksjonsdatoen i feltet **Transaksjonsdato**.
4. Velg **OK**.

## <a name="reverse-transactions"></a>Tilbakefør transaksjoner

> [!NOTE]
> - Start på trinn 1 for å tilbakeføre inntektsføring for én utsettelsesplan.
> - Start på trinn 2 for å tilbakeføre inntektsføring for flere planer.

1. På siden **Alle utsettelsesplaner**, i rutenettet **Tidsplanlinjer**, velger du linjene du vil oppheve føringen av, og velger deretter **Tilbakefør**.
2. På siden **Føringsbehandling** setter du feltet **Handling for føringskonto** til **Snudd føringsjournal**.
3. Velg fristdatoen i **Fristdato**-feltet. Behandlingen omfatter bare linjer der sluttdatoen er tidligere enn eller lik den angitte fristdatoen.
4. Velg **Filtrer**, og legg til datafiltre slik at listen bare viser de ønskede postene.
5. Velg **Vis forhåndsvisning** for å vise linjene.
6. Velg eventuelle linjer du ikke vil behandle, i listen over linjer, og velg deretter **Fjern**.
7. Feltene **Navn** og **Beskrivelse** oppdateres automatisk med standard journalnavn og -beskrivelse. Du kan endre verdiene etter behov. Du kan også velge om du vil summere føringsjournaloppføringen.
8. I delen **Transaksjonsdato** kan du overstyre transaksjonsdatoen med en bestemt dato for å behandle transaksjonen. Transaksjonsdatoen kan angis for lukkede perioder.
9. Hvis du vil foreta behandlingen som en del av et parti, velger du **Parti**. I dialogboksen **Satsvis behandling** angir du parameterne for partiet og velger deretter **OK** for å gå tilbake til siden **Føringsbehandling**. Den snudde inntektsføringen behandles senere, når partiet behandles.
10. Velg **OK**. Hvis du ikke la til transaksjonen i et parti, behandles alle linjene umiddelbart. Ellers behandles linjene når partiet behandles.

## <a name="apply-or-unapply-a-credit-note"></a>Bruk eller fjern en kreditnota

Hvis du vil bruke en kreditnota, gjør du følgende:

> [!NOTE]
> Når du oppretter en kreditnota fra siden **Utsettelse av salgsordretransaksjon** og setter alternativet **Juster eksisterende tidsplan** til **Ja**, brukes kreditnotaen automatisk på tidsplanen når kreditnotaen posteres.

1. Velg utsettelsesplanen på siden **Alle utsettelsesplaner**.
2. Velg en linje i **Kredittjusteringer**-listen, og velg deretter **Bruk**.
3. På siden **Bruk kreditnota (utsettelser)** angir du omberegningsdatoen i feltet **Omberegningsdato** og sluttdatoen i feltet **Sluttdato**.
4. I **Hode**-listen velger du **salgsordren** som har kreditnotaer.
5. Velg linjen i **Linjer**-listen.
6. Velg **OK**.
7. Velg **Ja**.

> [!NOTE]
> Hvis du vil bruke en kreditnota på flere enkeltvarer fra ulike fakturaer, må du gjenta disse trinnene.

Hvis du vil oppheve en kreditnota, gjør du følgende:

1. Velg utsettelsesplanen på siden **Alle utsettelsesplaner**.
2. Velg fakturaen i **Kredittjusteringer**-listen, og velg deretter **Ikke bruk**.
3. Velg **Ja**.

## <a name="fields"></a>Felt

Siden **Alle utsettelsesplaner** inneholder følgende felter.

| Felt | Beskrivelse |
|--------|-------------|
| **Hode** | |
| **Planlegg** | |
| Tildelingstype | Tildelingstypen for hendelsesbaserte utsettelser: **Prosent** eller **Beløp**. |
| Omklassifiseringsdato | <p>Den siste datoen da den kortsiktige omklassifiseringen for en utsettelsesplan ble behandlet. Denne datoen oppdateres hver gang **Kortsiktig omklassifisering av hendelse** brukes for utsettelsesplanen.</p>Dette feltet er bare tilgjengelig når de løpende periodene eller metoden for kortsiktig utsettelse for fast år brukes. |
| **Konto** | |
| Utsettelseskonto | Kontoen som brukes for utsettelsesbeløpet. |
| Føringskonto | Kontoen som brukes for føringsbeløpet. |
| Føringstype | Føringstypen. |
| Distribusjonstype | Distribusjonstypen. |
| **Transaksjon** | |
| Opprettingskilde | Kilden som transaksjonen ble opprettet fra. |
| Transaksjonstype | Transaksjonstypen. |
| Salgsordre | Salgsordrenummeret. |
| Faktura | Fakturanummeret. |
| Vare | Varenummeret. |
| **Faktureringsplan** | |
| Faktureringsplannummer | Nummeret til den tilsvarende faktureringsplanen. |
| Status for faktureringslinje | Statusen for linjevaren i den tilsvarende faktureringsplanen. |
| Eksterne referanser | Informasjon om eksterne referanser fra faktureringsplanen: **Ekstern** og **Linjenummer**. |
| Totaler | <p>Totalbeløp for utsettelsesplanen:</p><ul><li>**Langsiktig** – Summen av langsiktige utsettelsesbeløp. Denne verdien er bare tilgjengelig når feltet **Kortsiktig utsettelsesmetode** er satt til **Ingen** på siden **Parametere for inntekts- og utgiftsutsettelse**, eller når det kortsiktige beløpet er mer enn 0 (null).</li><li>**Kortsiktig** – Summen av kortsiktige utsettelsesbeløp. Denne verdien er bare tilgjengelig når feltet **Kortsiktig utsettelsesmetode** er satt til **Ingen** på siden **Parametere for inntekts- og utgiftsutsettelse**, eller når det kortsiktige beløpet er mer enn 0 (null).</li><li>**Ikke ført** – Summen av ikke-førte beløp for alle linjer.</li><li>**Avbrutt** – Summen av eksternt posterte beløp for alle linjer.</li><li>**Ført** – Summen av førte beløp for alle linjer.</li><li>**Eksternt postert og ført** – Summen av eksternt posterte og førte beløp for alle linjer.</li><li>**Totalbeløp** – Summen av beløpene for alle linjer.</li></ul> |
| **Tidsplanlinjer** | |
| Linje | Linjesekvensnummeret. |
| Startdato for utsettelse | Startdatoen for utsettelsesplanen. |
| Sluttdato for utsettelse | Sluttdatoen for utsettelsesplanen. |
| Beløp | Utsettelsesbeløpet. |
| Eksternt postert | En verdi som angir om linjen har blitt eksternt postert. |
| Ført | En verdi som angir om linjen har blitt ført. |
| Journalpartinummer | Partinummeret som beløpet ble ført i. |
| Hendelsesbeskrivelse | En beskrivelse av hendelsen. Dette feltet er bare tilgjengelig for hendelsesbaserte utsettelsesplaner. |
| **Kredittjusteringer** | |
| Faktura | <p>Fakturanummeret.</p><p>Verdien angir fakturaen for kreditnotajusteringen som allerede er brukt i utsettelsesplanen.</p> |
| Brukt beløp | Kredittjusteringsbeløpet som allerede er brukt i utsettelsesplanen. |
| Brukt dato | Datoen da kredittjusteringen ble brukt. |
| **Justering** | Justeringsverdiene vises bare hvis en kreditnota ble behandlet for utsettelsesplanen. Hvis ingen kreditnota ble behandlet, er disse verdiene skjult. |
| Justeringsbeløp | Det totale justeringsbeløpet, beregnet som *opprinnelig beløp* – *tidsplanbeløp*. |
| Opprinnelig sluttdato | Den opprinnelige sluttdatoen for utsettelsesplanen. |
| Opprinnelig tidsplanbeløp | Totalsummen i den opprinnelige utsettelsesplanen. |
