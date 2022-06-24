---
title: Fraværsregistrering i timeregistrering
description: Denne artikkelen beskriver hvordan du håndterer fraværsregistreringer i Timeregistrering.
author: johanhoffmann
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JMGParameters, JmgAbsenceCalendar
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9a613edbe42d1bfb1d2ee43ee1cb2f1e0ab49a05
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890777"
---
# <a name="absence-registration-in-time-and-attendance"></a>Fraværsregistrering i timeregistrering

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver begreper for fravær, og forklarer hvordan du håndterer fravær i Timeregistrering.

## <a name="absence-that-is-based-on-regular-work-hours"></a>Fravær som er basert på vanlig arbeidtid

Arbeidere anses som fraværende i timer de ikke arbeider i den vanlige arbeidstiden. Vanlig arbeidstid defineres i profilen for standard arbeidstid for en arbeider.

En arbeider arbeider for eksempel på en dagprofil som har innstempling 07:00 og utstempling 15:00. Hvis arbeideren stempler inn 09:00, anses vedkommende som fraværende fra 07:00 til 09:00 denne dagen.

I slike tilfeller blir arbeidere bedt om å angi en årsak til fraværet. De kan angi en årsak ved å velge en fraværskode.

## <a name="absence-codes"></a>Fraværskoder

Fraværskoder definere ulike typer fravær. Fraværskoder defineres av firmaet.

Forskjellige regler kan brukes på fraværskoder. En fraværskode kan for eksempel konfigureres til å trekke fra eller gi lønn.

Et firma definerer for eksempel en **For sent**-fraværskode som arbeidere kan bruke hvis de kommer inn for sent og ikke har en god grunn. Firmaet definerer også en **Internt kurs**-fraværskode som arbeidere bruker for tid som brukes for deltakelse på interne kurs. Disse fraværskoder kan defineres slik at **For sent** trekker lønn fra en arbeider, men **Internt kurs** ikke trekke lønn fra en arbeider.

Du kan definere automatiske fraværskoder. Disse fraværskodene kan brukes til å beregne en arbeiders klokkeslett når ingen fravær er registrert. Arbeiderens tidsprofil bestemmer om fraværskoden for standardtid eller fleksetid brukes.

### <a name="set-up-standard-time-and-flex-time"></a>Definere standardtid og fleksitid

- Konfigurer parametere for standardtid og fleksitid ved hjelp av alternativene **Sett inn fravær automatisk** og **Sett inn fleksitid automatisk** på siden **Parametere for timeregistrering**.

## <a name="absence-groups"></a>Fraværsgrupper

Fraværskoder grupperes i fraværsgrupper. Du kan bruke fraværsgrupper til å gruppere fraværskoder som har felles egenskaper. Eksempler omfatter koder for gyldig fravær eller fravær på grunn av en legetime, meddommertjeneste eller sykt barn.

## <a name="planned-absence"></a>Planlagt fravær

Hvis du vet at en arbeider vil være fraværende en periode, for eksempel en kommende ferie, kan du bruke planlagt fravær. Du kan definere planlagt fravær ved å konfigurere fraværskoden slik at det anses som planlagt fravær. Når du definerer et planlagt fravær, blir du ikke bedt om en fraværskode i løpet av fraværsperioden når tidsregistrering for brukeren beregnes. Planlagt fravær kan defineres for én enkelt arbeider, eller du kan definere en satsvis jobb for å masseoppdatere planlagt fravær for arbeidere.

### <a name="set-up-planned-absence"></a>Definere planlagt fravær

1. Velg **Personale** &gt; **Arbeidere** &gt; **Ansatte**, og velg en ansatt.
2. Velg **Tid** &gt; **Tidstildelinger** &gt; **Fraværsregistrering**, og angi det planlagte fraværet.

## <a name="interrupted-planned-absence"></a>Avbrutt planlagt fravær

Hvis du bruker alternativet **Avbryt** når du definerer et planlagt fravær, blir det planlagte fraværet avbrutt hvis arbeideren stempler inn i løpet av perioden for planlagt fravær. Det planlagte fraværet vil bli merket som **Avbrutt** og vil ikke ha noen innvirkning på fremtidige beregninger.

### <a name="set-up-a-planned-absence-for-interruption"></a>Definere planlagt fravær for avbrudd

1. Åpne siden **Fraværsregistrering** som beskrevet i fremgangsmåten for å definere planlagt fravær.
2. Velg **Avbryt**.

Alternativet **Avbryt** brukes når tiden registreres gjennom shop floor-terminalen eller -enheten. Alternativet gjelder ikke hvis registreringer er angitt på sidene for beregning og godkjenningsstatus eller på siden **Elektronisk tidskort**.

## <a name="examples-of-the-use-of-absence-in-a-flex-profile"></a>Eksempler på bruk av fravær i en fleksiprofil

De tre eksemplene nedenfor viser hvordan fravær beregnes i en profil som har fleksiperioder.

Eksemplene bruker profilen nedenfor.

| Innstempling | Normaltid    | Bryt             | Normaltid | Fleksi-        | Utstempling | Fleksi+        |
|----------|------------------|-------------------|---------------|--------------|-----------|--------------|
| 08:00     | 09:00 til 11:30 | 11:30 til 12:00 | 12:00 til 15:00 | 12:00 til 15:00 | 16:00      | 16:00 til 18:00 |

### <a name="example-1-signing-out-during-a-flex--period"></a>Eksempel 1: Utstempling i perioden Fleksi-

Arbeideren stempler inn 8:00 og stempler ut 15:30. Siden arbeideren i dette tilfellet stempler ut i perioden Fleksi-, beregnes ikke fravær, og en halv time trekkes fra fleksisaldoen for arbeideren.

### <a name="example-2-signing-out-in-during-standard-time-period"></a>Eksempel 2: Utstempling i løpet av perioden for standardtid

Arbeideren stempler inn i 8:00 og stempler ut 14:30. Siden arbeideren i dette tilfellet stempler ut i perioden for standardtid, beregnes fravær fra 14:30 til 16: 00, og det registreres en fraværsperioden på 1,5 timer. Det kreves en fraværskode i dette tidsrommet.

### <a name="example-3-signing-out-during-a-flex-period"></a>Eksempel 3: Utstempling i perioden Fleksi+

Arbeideren stempler inn 8:00 og stempler ut 15:30. Siden arbeideren i dette tilfellet stempler ut i perioden Fleksi+, beregnes ikke fravær, og en halv time legges til fleksisaldoen for arbeideren.

## <a name="absence-in-the-calculation-and-approval-process"></a>Fravær i beregnings- og godkjenningsåprosessen

Tidsregistreringer for arbeider må beregnes og godkjennes før de kan overføres til lønningssystemet som lønnsposter.

En godkjenner kan endre tidsregistreringer for en arbeider. Godkjenneren kan også endre alle fravær som arbeideren har registrert. Hvis godkjenneren manuelt angir en tidsperiode som har en fraværskode, overstyres ikke fraværskoden for denne perioden av standard fraværskode fra Parametere for timeregistrering.

En arbeider stempler for eksempel inn 10:00 og velger en fraværskode som indikerer at vedkommende kommer for sent. Senere informerer arbeideren sin overordnede om en legeavtale fra 08:00 til 10:00. Legeavtalen skal ikke føre til trekk i lønn for arbeideren. I dette tilfellet kan derfor overordnede justere de to timene med fravær fra 08:00 til 10:00 ved å manuelt angi en fraværskode som angir sykdom for disse to timene.

### <a name="calculate-and-approve-absence"></a>Beregne og godkjenne fravær

- Velg **Timeregistrering** &gt; **Gjennomgå og godkjenn** &gt; **Godkjenn eller beregn**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]