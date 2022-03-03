---
title: Vanlige spørsmål om tilbakestilling av datatorg
description: Dette emnet gir svar på noen vanlige spørsmål om tilbakestilling av datatorg.
author: jinniew
ms.date: 02/14/2022
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
ms.openlocfilehash: 53f45f469c39f9e389763aa0daed658e5a62d377
ms.sourcegitcommit: 6a269db08e8bb3bb3405c9f4a512091d13c80faa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/14/2022
ms.locfileid: "8119518"
---
# <a name="data-mart-resets-faq"></a>Vanlige spørsmål om tilbakestilling av datatorg

Dette emnet gir svar på noen vanlige spørsmål om tilbakestilling av datatorg. En tilbakestilling av datatorg kan være en tidkrevende prosess og, avhengig av omstendighetene, kan det hende at det ikke er den løsningen som kreves. Derfor inneholder dette emnet informasjon om forhold der en tilbakestilling av datatorg kan hjelpe, og også forhold der det sannsynligvis ikke vil hjelpe.

## <a name="what-is-a-data-mart-reset"></a>Hva er en tilbakestilling av datatorg?

En datatilbakestilling av datatorg vil deaktivere integreringsoppgavene, slette alle datatorgdata og deretter aktivere integreringen på nytt.

For å sikre at de gamle dataene ikke settes inn, kan en datatilbakestilling startes bare etter at eksisterende oppgaver er fullført. Hvis du prøver å tilbakestille datatorg før alle oppgavene er fullført, kan du for eksempel få meldingen: "Tilbakestilling av datatorg vil ikke kunne behandles på grunn av en aktiv oppgave. Prøv på nytt senere."

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a>Når må jeg tilbakestille et datatorg?

Hvis én eller flere av de følgende erklæringene gjelder for din situasjon, kan organisasjonen dra nytte av en tilbakestilling av datatorg:

- **Programdatabasen ble gjenopprettet**.
- **Du har åpnet en støtteforespørsel** – En kundestøttetekniker har bedt deg om å tilbakestille datatorg som en del av et feilsøkingstrinn.
- **Stor prosentdel foreldede poster** – Foreldede poster alene gir ikke nødvendigvis en god grunn til å tilbakestille datatorg. Store prosentdeler med foreldede data kan redusere den samlede ytelsen ved rapportgenerering og -integrering og medføre ekstra bruk av databaseplass. Vi anbefaler at du foretar en tilbakestilling av datatorg for å fjerne foreldede data når det er mer enn 80 % foreldede data i datatorget.
 
> [!NOTE]
> Prosessen med å tilbakestille et datatorg påvirkes av antallet økonomi- og budsjettransaksjoner i databasen. Avhengig av antall transaksjoner i systemet, kan en tilbakestilling av datatorg fullføres på bare 15 minutter, eller det kan ta opptil fire timer. Hvis tilbakestillingen tar mer enn fire timer, anbefaler vi at du kontakter kundestøtte.
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a>Når blir et datatorg tilbakestilt på feil måte?

Her er noen omstendigheter der vi anbefaler at du ikke tilbakestiller et datatorg:

- Du har problemer med dataintegreringsytelsen.
- Du har et gjentakende tilbakestillingsmønster av en av følgende årsaker:

    - **Manglende eller uventede data i rapporten** – Hvis du ser at det mangler data, åpner du en støtteforespørsel hos Microsoft for å gå gjennom rapportformatet og mulige problemer med datasynkronisering.
    - **Fastlåst integreringstilstand**
   
## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Hvis jeg tilbakestiller datatorg, vil jeg miste rapporter som jeg allerede har utformet?

Nei. Rapportene dine lagres i SQL-tabeller som ikke påvirkes av en tilbakestilling av datatorg. Hvis du er opptatt av å miste rapporter du har utformet, kan du sikkerhetskopiere utformingene du ikke vil miste. Hvis du vil sikkerhetskopiere utforminger, åpner du Rapportutforming og går til **Firma \> Firmaer \> Byggesteiner \> Eksporter**.
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a>Må alle brukerne avslutte systemet før jeg kan tilbakestille datatorg?

Nei. Brukere kan fortsette å arbeide i systemet under tilbakestillingen av datatorg. De vil imidlertid ikke få tilgang til rapporter som ble opprettet med Financial Reporter før tilbakestillingen er fullført.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
