---
title: Vanlige spørsmål om tilbakestilling av data mart
description: Dette emnet gir svar på noen vanlige spørsmål om tilbakestilling av data mart.
author: jinniew
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 90abe1fc3e84e0a9777f3eabd790a4b7e9b509c5
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638273"
---
# <a name="data-mart-resets-faq"></a>Vanlige spørsmål om tilbakestilling av data mart

Dette emnet gir svar på noen vanlige spørsmål om tilbakestilling av data mart. En tilbakestilling av data mart kan være en tidkrevende prosess og, avhengig av omstendighetene, kan det hende at det ikke er den løsningen som kreves. Derfor inneholder dette emnet informasjon om forhold der en tilbakestilling av data mart kan hjelpe, og også forhold der det sannsynligvis ikke vil hjelpe.

## <a name="what-is-a-data-mart-reset"></a>Hva er en tilbakestilling av data mart?

En datatilbakestilling av data mart vil deaktivere integreringsoppgavene, slette alle data mart-data og deretter aktivere integreringen på nytt.

For å sikre at de gamle dataene ikke settes inn, kan en datatilbakestilling startes bare etter at eksisterende oppgaver er fullført. Hvis du prøver å tilbakestille data mart før alle oppgavene er fullført, kan du for eksempel få meldingen: "Tilbakestilling av data mart vil ikke kunne behandles på grunn av en aktiv oppgave. Prøv på nytt senere."

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a>Når må jeg tilbakestille et data mart?

Hvis én eller flere av de følgende erklæringene gjelder for din situasjon, kan organisasjonen dra nytte av en tilbakestilling av data mart:

- Applikasjonsdatabasen ble gjenopprettet.
- Du har åpnet en støtteforespørsel, og en kundestøttetekniker har bedt deg om å tilbakestille data mart som en del av et feilsøkingstrinn.
 
> [!NOTE]
> Prosessen med å tilbakestille et datatorg påvirkes av antallet økonomi- og budsjettransaksjoner i databasen. Avhengig av antall transaksjoner i systemet, kan en tilbakestilling av datatorg fullføres på bare 15 minutter, eller det kan ta opptil fire timer. Hvis tilbakestillingen tar mer enn fire timer, anbefaler vi at du kontakter kundestøtte.
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a>Når blir et data mart tilbakestilt på feil måte?

Her er noen omstendigheter der vi anbefaler at du ikke tilbakestiller et data mart:

- Du har ytelsesproblemer som er knyttet til datasynkronisering.
- Du har et gjentakende tilbakestillingsmønster av en av følgende årsaker:

    - **Manglende data** – Hvis du ser at det mangler data, åpner du en støtteforespørsel hos Microsoft for å gå gjennom rapportformatet og mulige problemer med datasynkronisering.
    - **Fastlåst integreringstilstand**
    - **Foreldede poster** – Foreldede poster alene gir ikke nødvendigvis en god grunn til å tilbakestille data mart. Hvis du har et stort datasett, tar det litt tid å kjøre tilbakestillingsprosessen, men den fører sannsynligvis ikke til forbedringer.

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Hvis jeg tilbakestiller data mart, vil jeg miste rapporter som jeg allerede har utformet?

Nei. Rapportene dine lagres i SQL-tabeller som ikke påvirkes av en tilbakestilling av data mart. Hvis du er opptatt av å miste rapporter du har utformet, kan du sikkerhetskopiere utformingene du ikke vil miste. Hvis du vil sikkerhetskopiere utforminger, åpner du Rapportutforming og går til **Firma \> Firmaer \> Byggesteiner \> Eksporter**.
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a>Må alle brukerne avslutte systemet før jeg kan tilbakestille data mart?

Nei. Brukere kan fortsette å arbeide i systemet under tilbakestillingen av data mart. De vil imidlertid ikke få tilgang til rapporter som ble opprettet med Financial Reporter før tilbakestillingen er fullført.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
