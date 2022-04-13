---
title: Avslutt faktureringsplaner
description: Dette emnet beskriver hvordan du avslutter faktureringsplaner og faktureringsplanlinjer i Abonnementsfakturering.
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
ms.openlocfilehash: df81cc888e893c6a4a127e1a43426a0a0b56f0d1
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/23/2022
ms.locfileid: "8470458"
---
# <a name="terminate-billing-schedules"></a>Avslutt faktureringsplaner

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du avslutter faktureringsplaner og faktureringsplanlinjer i Abonnementsfakturering. Når du avslutter en faktureringsplan, må den ha statusen **Aktiv**. Den kan ikke ha statusen **På vent**. På samme måte, når du avslutter en faktureringsplanlinje, må den ha statusen **Aktiv**. Hodedelen i faktureringsplanen påvirkes ikke når du avslutter en faktureringsplanlinje.

Hvis du vil avslutte en faktureringsplan eller faktureringsplanlinje, kan du gå til et av følgende steder:

- Listesiden **Alle/Aktive faktureringsplaner**
- En bestemt faktureringsplan på siden **Alle faktureringsplaner**
- En bestemt faktureringsplanlinje på siden **Alle faktureringsplaner**

> [!NOTE]
> Hvis du vil avslutte flere faktureringsplaner samtidig, bruker du siden **Massebehandling av avslutning**.

## <a name="terminate-a-billing-schedule-or-line"></a>Avslutt en faktureringsplan eller -linje

Hvis du vil avslutte en faktureringsplan eller faktureringsplanlinje, følger du trinnene nedenfor.

1. Velg en faktureringsplan eller faktureringsplanlinje, og velg deretter **Avslutt**. 
2. Angi feltene **Avslutningsdato**, **Avslutningstype** og **Årsakskode**.
3. Sett feltet **Kredittalternativ** til **Utsted kreditt**.
4. Velg **Avslutt**.

Statusen til faktureringsplanen endres basert på avslutningstypen du valgte. Hvis du valgte **Fakturer gjenstående** som avslutningstype, er statusen til alle linjene i faktureringsplanen **Siste fakturering**. Statusen til faktureringsplanen forblir **Aktiv** til den siste fakturaen er behandlet. Etter at den siste fakturaen er behandlet, oppdateres statusen til **Avsluttet**. Hvis du valgte **Juster plan** som avslutningstype, blir statusen for faktureringsplanen umiddelbarft oppdatert til **Avsluttet**.

## <a name="terminate-a-billing-schedule-or-line-and-apply-a-refund"></a>Avslutt en faktureringsplan eller -linje og bruk en refundering

Hvis du vil avslutte en faktureringsplan eller faktureringsplanlinje og bruke en refundering, følger du trinnene nedenfor.

1. Velg en faktureringsplan eller faktureringsplanlinje, og velg deretter **Avslutt**.
2. Angi feltene **Avslutningsdato**, **Avslutningstype**, **Årsakskode** og **Kredittalternativ**.
3. Velg **Avslutt med refundering**. Siden **Massebehandling av avslutning** vises, og den er filtrert slik at den viser faktureringsplanen.
4. Velg **Vis forhåndsvisning** for å vise faktureringsplanlinjene, og velg deretter **Behandle**.

Når kreditten er behandlet, åpner du siden **Vis faktureringsdetaljer** for å se gjennom kreditten som ble brukt på faktureringsplanen. Hvis kredittbeløpet er mer enn 0 (null), blir alle fremtidige ufakturerte linjer slettet og erstattet med faktureringsdetaljlinjer som viser negative beløp for kreditten som ble brukt i faktureringsplanen.

### <a name="view-example"></a>Vis eksempel

En faktureringsplan har følgende informasjon:

- Startdatoen er 1. januar 2020.
- Sluttdatoen er 31. desember 2020.
- Faktureringsperiodebeløpet er 100,00 per måned.
- Fakturaer er opprettet for faktureringsperioder fra januar til juli.
- Avslutningsdatoen for kontrakten er 15. juni 2020.

Når kredittjusteringen er behandlet, fjernes alle fremtidige faktureringsperioder (august til desember) fra siden **Vis faktureringsdetaljer**. En kredittjusteringslinje blir lagt til etter faktureringsperioden for juli:

- 16. juni–31. juli med et kredittbeløp på 150,00

Hvis funksjonen for ufakturert inntekt brukes, oppdateres siden **Revisjon av journaloppføring som ikke er fakturert** med avslutningsoppføringen.

## <a name="terminate-a-billing-schedule-or-line-without-applying-a-credit"></a>Avslutt en faktureringsplan eller -linje uten å bruke en kreditt

Hvis du vil avslutte en faktureringsplan eller faktureringsplanlinje uten å bruke en kreditt, følger du trinnene nedenfor.

1. Velg en faktureringsplan eller faktureringsplanlinje, og velg deretter **Avslutt**.
2. Angi **Avslutningsdato**-feltet.
3. Sett feltet **Avslutningstype** til **Ingen justering**. Feltet **Kredittalternativ** settes automatisk til **Ingen kreditt**.
3. Angi **Årsakskode**-feltet.
4. Angi eventuelle merknader i feltet **Avslutningsmerknader**.
5. Velg **Avslutt**. 

Når avslutningen er behandlet, fjernes alle faktureringsdetaljlinjene etter at avslutningsdatoen er fjernet. (Disse linjene omfatter linjen som inneholder avslutningsdatoen.) Det kan ikke opprettes fakturaer for de avsluttede linjene. Hvis avslutningen fjernes, blir alle avsluttede linjer lagt til på siden **Vis faktureringsdetaljer**, og de blir tilgjengelige for fakturering.

## <a name="fields"></a>Felt

Siden **Vis faktureringsdetaljer** inneholder følgende felter.

| Felt | Beskrivelse |
|-------|-------------| 
| Avslutningsdato | Velg datoen når du ønsker å avslutte en faktureringsplan eller faktureringsplanlinje. |
| Avslutningstype | <p>Velg avslutningstypen:</p><ul><li>**Juster plan** – Stopp faktureringsperiodene for linjen på avslutningsdatoen, og endre statusen for linjen til **Siste fakturering**. Hvis det finnes en utsettelsesplan for linjevaren, justeres den ved å tilbakeføre beløpet som ikke lenger må inntektsføres. Hvis startdatoen for fakturering er etter avslutningsdatoen, fjernes de gjenværende faktureringsperiodene.</li><li>**Fakturer gjenstående** – Legg til et eventuelt restbeløp for faktureringsperioden i avslutningsperioden, og endre statusen for linjen til **Siste fakturering**. Hvis det finnes en utsettelsesplan for linjevaren, oppdateres sluttdatoen for utsettelsen. Hvis startdatoen for fakturering er etter avslutningsdatoen, blir totalbeløpet for alle gjenværende faktureringsperioder lagt til i faktureringsperioden, og de gjenværende faktureringsperiodene blir fjernet.</li><li>**Ingen justering** – Avslutt faktureringsperiodene for linjen på den angitte avslutningsdatoen. Ingen justeringer blir foretatt. Når denne avslutningstypen er valgt, blir feltet **Kredittalternativ** angitt til **Ingen kreditt** og feltet **Fordel daglig** angitt til **Nei**. Begge disse feltene blir skrivebeskyttet, og de kan ikke endres.</li></ul> |
| Kredittalternativ | <p>Velg hvordan kreditten skal brukes når du avslutter en faktureringsplanlinje:</p><ul><li>**Kredittjustering** – Opprett en kredittjustering for en faktureringsplan når en linje avsluttes. Kredittjusteringen vises i en fremtidig faktureringsperiode for faktureringsplanen. Justeringen justerer også automatisk fakturabeløpet for den neste faktureringsperioden til kreditten er ferdig brukt på faktureringsplanen.</li><li>**Utsted kreditt** – Opprett en kreditnota når en faktureringsplan eller faktureringsplanlinje avsluttes.</li><li>**Ingen kreditt** – Ikke opprett en kreditnota når en faktureringsplan eller faktureringsplanlinje avsluttes. Dette alternativet er bare tilgjengelig når du bruker en avslutning av typen **Ingen justering** for å avslutte en faktureringsplan.</li></ul><p>Standardalternativet er fra siden **Parametere for gjentakende kontraktfakturering**.</p> |
| Årsakskode | Velg årsakskoden til avslutningen. |
| Årsaksbeskrivelse | Beskrivelsen av årsakskoden. |
| Avslutningsmerknader | Angi merknader om avslutningen. |

<!--## Additional information-->
