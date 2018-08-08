---
title: Fleksigrupper
description: Dette emnet beskriver hvordan fleksigrupper brukes i timeregistrering.
author: johanhoffmann
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgFlexGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: e21a2de2f46c619f27eddad4d7cced260a90bbb8
ms.openlocfilehash: 20f317ff57fac25b5b5b0d702fe64845eb849e87
ms.contentlocale: nb-no
ms.lasthandoff: 04/09/2018

---

# <a name="flex-groups"></a>Fleksigrupper

[!include[banner](../includes/banner.md)]

Fleksible arbeidstimer gjør at bedrifter kan redusere betalinger for overtid ved å tilby ekstra fritid i perioder når arbeidsmengden er lav. Denne funksjonen er relevant, for eksempel i segmenter som opplever sesongbetonte endringer i arbeidsmengden.

Du kan bruke fleksigrupper til å angi følgende regler og prinsipper for en arbeiders fleksible timer:

- Regler for fleksibestemmelser
- Prinsipp for beregning av arbeiderens fleksisaldo

## <a name="set-up-flexible-working-hours-in-flex-groups"></a>Angi fleksible arbeidstimer i fleksigrupper

- Velg **Timeregistrering** \> **Oppsett** \> **Grupper** \> **Fleksigrupper** for å definere fleksigrupper for fleksible timer.

## <a name="associate-workers-with-flex-groups"></a>Knytte ansatte til fleksigrupper

- Velg **Tidsregistrering** \> **Oppsett** \> **Tidsregistreringsarbeidere**.

## <a name="rules-for-flex-regulations"></a>Regler for fleksibestemmelser

Du kan bruke regler for fleksibestemmelser til å definere fleksigrenser, eller minste og største antall timer som tillates i arbeiderens flekskonto. Fleksigrensene er definert på fleksigruppen. Når fleksigrensene er overskredet, kan en arbeiders fleksisaldo og lønn justeres.

Hvis en arbeiders tillatte fleksiminimum er overskredet (det vil si hvis antallet timer i fleksikontoen er mindre enn angitt minimum), kan du bruke disse metodene til å justere arbeiderens fleksisald ved å velge en fleksibestemmelse:

- Arbeiderens fleksikonto kan justeres til angitt tillatte minimum, men uten å trekke fra arbeiderens lønn for antall timer som fleksikontoen er under tillatt minimum.
- Arbeiderens lønn kan trekkes for antall timer som fleksikontoen er under tillatt minimum. Dette fradraget dette gjøres ved å generere lønnsenheter for en bestemt lønnstype som har en negativ eller positiv lønnsenhet.

Hvis arbeiderens tillatte fleksimaksimum er overskredet, kan du bruke disse metodene til å justere arbeiderens fleksisaldo ved å velge en fleksibestemmelse:

- Arbeiderens fleksikonto kan justeres tilbake til angitt tillatte maksimum, men uten å kompensere arbeiderens lønn for antall timer som arbeideren arbeidet over tillatt maksimum.
- Antall timer arbeideren arbeidet over den tillatte maksimumslengden, kan konverteres til lønn. Denne konverteringen skjer ved generering av lønnsposter for en bestemt lønnstype.

Du kan også justere en fleksisaldo på følgende tidspunkt:

- Når en betalingsfil som er basert på lønnsdata, er eksportert ved hjelp av jobben **Overfør lønn**. Lønnsdata genereres når du overfører arbeiderens registrering fra **Godkjenn**-siden.
- Når jobben **Juster fleksisaldo** skal utføres.

> [!NOTE]
> Fleksibestemmelser oppstår ikke under daglig godkjenning og overføring av arbeiderregistreringer på **Godkjenn**-siden.

## <a name="principle-for-calculating-a-workers-flex-balance"></a>Prinsipp for beregning av en arbeiders fleksisaldo

Prinsippet for beregning av timene som arbeiderens fleksisaldo skal justeres etter, defineres på fleksigruppen. Velg **Timeregistrering** \> **Oppsett** \> **Grupper** \> **Fleksigrupper**. 

Følgende to prinsipper kan brukes:

- **Tid** – arbeiderens fleksible timer beregnes bare fra arbeiderens registrerte tid for dagen. Når arbeiderens daglige registreringer beregnes, beregnes antall Fleksi+ og Fleksi- timer for dagen fra Fleksi+ og Fleksi- soner som er definert i arbeiderens tidsprofil.
- **Lønnstyper** – arbeiderens fleksible timer beregnes basert på inntekter av lønnstypene for Fleksi+ og Fleksi- som er definert i arbeiderens lønnsavtale. Lønnsavtalen er knyttet til tidsregistreringsarbeideren. Du vil kanskje bruke lønnstyper til å administrere fleksikontoer hvis du for eksempel du vil øke fleksikontoen for en arbeider med en bestemt faktor i en eller flere fleksisoner.

### <a name="scenario-1-adjusting-a-workers-pay-and-flex-account-because-the-allowed-flex-minimum-is-exceeded"></a>Scenario 1: Justering av en arbeiders lønn og fleksikonto fordi tillatt fleksi-minimum er overskredet

En arbeider som kan jobbe fleksitid, har en negativ fleksikonto.

- **Fleksikonto:** -4

Arbeideren er knyttet til en fleksigruppe som har følgende konfigurasjon:

- **Fleksiminimum:** -0,5
- **Minimumslønnstype:** 1302
- **Lønnstypefaktor:** -1,00

Som differansen mellom arbeiderens fleksikonto og hans tillatte fleksiminimum angir, har arbeideren overskredet sin tillatte fleksiminimum med 3,5 timer.

Når lønnsadministratoren overfører arbeiderens lønnsdata ved å kjøre jobben **Overfør til lønn** eller **Fleksijustering**, gjøres følgende justeringer:

- Arbeiderens fleksikonto justeres med 3,5 timer. Derfor blir fleksisaldoen -4,0 timer justert til arbeiderens tillatte fleksiminimum på -0,5 timer.
- Det opprettes en lønnsenhet for lønnstypen 1302. Denne lønnsposten har en lønnsenhet på -3,5 timer som blir trukket fra arbeiderens lønn. I dette tilfellet er lønnsenheten et negativt tall fordi den positive justeringen av 3,5 timer multipliseres med den negative lønnsfaktortypen -1,0 som er definert i fleksigruppen. Denne lønnsposten blir en del av lønnsfilen som genereres av jobben **Overfør til lønn**.

### <a name="scenario-2-adjusting-a-workers-pay-and-flex-account-because-the-allowed-flex-maximum-is-exceeded"></a>Scenario 2: Justering av en arbeiders lønn og fleksikonto fordi tillatt fleksi-maksimum er overskredet

En arbeider som kan jobbe fleksitid, har en positiv fleksikonto.

- **Fleksikonto:** 6

Arbeideren er knyttet til en fleksigruppe som har følgende konfigurasjon:

- **Fleksi maksimum:** 2,0
- **Minimumslønnstype:** 1302
- **Lønnstypefaktor:** -1,0

Som differansen mellom arbeiderens fleksikonto og hennes tillatte fleksi-maksim angir, har arbeideren overskredet sin tillatte fleks-maksimum med 4,0 timer.

Når lønnsadministratoren overfører arbeiderens lønnsdata ved å kjøre jobben **Overfør til lønn** eller **Fleksijustering**, gjøres følgende justeringer:

- Arbeiderens fleksikonto justeres med -4,0 timer. Derfor blir fleksisaldoen 6,0 timer justert til arbeiderens tillatte fleksi-maksimum på 2,0 timer.
- Det opprettes en lønnsenhet for lønnstypen 1302. Denne lønnsposten har en lønnsenhet på 4,0 timer som legges til arbeiderens lønn. I dette tilfellet er lønnsenheten et positivt tall fordi den negative justeringen av 4,0 timer multipliseres med den negative lønnsfaktortypen -1,0 som er definert i fleksigruppen. Denne lønnsposten blir en del av lønnsfilen som genereres av jobben **Overfør til lønn**.

### <a name="scenario-3-managing-a-workers-flex-balance-based-on-pay-types"></a>Scenario 3: Administrasjon av en arbeiders fleksisaldo basert på lønnstyper

Som forklart tidligere kan fleksikontoer administreres basert på tiden som er registrert i Fleksi+ og Fleksi- soner som er definert arbeiderens tidsprofil, eller på lønnstypene som er definert i arbeiderens lønnsavtaler. Hvis lønnstyper brukes, justeres en arbeiders fleksikonto med lønnspostene som genereres når du overfører arbeiderens registrering fra **Godkjenn**-siden. Du vil kanskje bruke lønnstyper til å administrere fleksikontoer hvis du for eksempel du vil øke fleksikontoen for en arbeider med en bestemt faktor i en eller flere fleksisoner.

Dette scenariet bruker følgende fleksiprofil som representerer en arbeidsdag.

| Profiltype  | Start    | Slutt      |
|---------------|----------|----------|
| Fleksi+         | 12:00 AM | 08:00 AM |
| Stemple inn      | 08:00 AM | 08:00 AM |
| Fleksi-         | 08:00 AM | 09:00 AM |
| Normaltid | 09:00 AM | 11:30 AM |
| Betalt pause    | 11:30 AM | 12:00 PM |
| Fleksi-         | 12:00 PM | 04:00 PM |
| Utstempling     | 04:00 PM | 04:00 PM |
| Fleksi+         | 04:00 PM | 12:00 AM |

I dette tilfellet vil du kunne administrere arbeiderens fleksisaldo basert på lønnstyper. Derfor må du angi alternativet **Basert på lønnstyper** til **Ja** i arbeiderens fleksigruppe.

For å ta høyde for de fleksible timene, må du også definere en ny lønnstype. I dette scenariet kalles lønnstypen **FlexCnt**.

| Lønnstype | beskrivelse  |
|----------|--------------|
| FlexCnt  | Fleksibel teller |

Deretter følger du denne fremgangsmåten for å definere en lønnstype og legge til linjer med den nye typen til en lønnsprofil.

1. Velg **Timeregistrering** \> **Oppsett** \> **Grupper** \> **Fleksigrupper**, og velg deretter **Ny**.
2. I både feltet **Fleksi+** og feltet **Fleksi-** angir du den nye lønnstypen, **FlexCnt**.
3. Velg **Timeregistrering** \> **Oppsett** \> **Lønnsavtaler**, og velg deretter **Avtalelinjer**.
4. For **mandag**, for profiltypen **Fleksi+**, legger du til følgende tre linjer.

    | Lønnstype | beskrivelse  | Fra kl. | Til kl.  | Minimum | Maksimum | Omregningsfaktor |
    |----------|--------------|-----------|----------|---------|---------|--------|
    | FlexCnt  | Fleksibel teller | 12:00 AM  | 06:00 PM | 00.00   | 00.00   | 1,00   |
    | FlexCnt  | Fleksibel teller | 06:00 PM  | 12:00 AM | 00.00   | 02.00   | 1.50   |
    | FlexCnt  | Fleksibel teller | 06:00 PM  | 12:00 AM | 02.00   | 06.00   | 2.00   |

    > [!NOTE]
    > Hver linje brukes for et annet tidsintervall og har en annen faktor. De fleksible timene som arbeideren jobber i et tidsintervall, multipliseres med faktoren for denne linjen. Timer som er arbeidet fra 06:00 PM til 08:00 PM, multipliseres med 1,50. Faktoren er angitt i **Faktor**-feltet i **Generelt**-kategorien på siden **Linjer for lønnsavtale**.

Arbeideren angir følgende registreringer for dagen.

| Journalregistreringstype | Start    | Slutt      |
|---------------------------|----------|----------|
| Stemple inn                  | 07:00 AM | 07:00 AM |
| Produksjonsjobb            | 07:00 AM | 09:00 PM |
| Utstempling                 | 09:00 PM | 09:00 PM |

Beløpet som skal betales, beregnes på **Godkjenn**-siden, basert på arbeiderens registrering. Når registreringen er beregnet, kan du vise resultatet i **Tider**-kategorien. Du er interessert i følgende felt i dette scenariet.

| Fleksi + | Fleksi - | Tidspunkt  | Lønnstid |
|--------|--------|-------|----------|
| 6,00   | 0.00   | 13.50 | 08.00    |

Mengden Fleksi+ tid er seks timer, og beregningen er basert på fleksisonene i tidsprofilen. Denne mengden består av én time for Fleksi+ tid fra 07:00 AM til 08:00 AM og fem timer med Fleksi+ tid fra 04:00 PM til 09:00 PM.

Når du overfører registreringene, ser du at mengden Fleksi+ tid er endret fra 6,0 timer til 8,0 timer.

| Fleksi + | Fleksi - | Tidspunkt  | Lønnstid |
|--------|--------|-------|----------|
| 8,00   | 0.00   | 13.50 | 08.00    |

Denne endringen skjer etter overføringen fordi de fleksible timene er beregnet basert på lønnstyper i stedet for klokkeslett. Følgende tabell viser hvordan de åtte timene beregnes:

| Fra     | Til       | Tidspunkt | Omregningsfaktor    | Fleksikonto |
|----------|----------|------|-----------|--------------|
| 07:00 AM | 08:00 AM | 1    | 1         | 1            |
| 04:00 PM | 06:00 PM | 2    | 1         | 2            |
| 06:00 PM | 08:00 PM | 2    | 1.5       | 3            |
| 08:00 PM | 09:00 PM | 1    | 2         | 2            |
|          |          |      | **Totalt** | **8**        |

