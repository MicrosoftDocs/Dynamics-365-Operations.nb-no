---
title: Reversere produksjonsordrestatusen
description: Dette emnet beskriver hvordan du tilbakefører statusen for en produksjonsordre.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdParmStatusDecrease, ProdSetupStatusDecrease
audience: Application User
ms.reviewer: kamaybac
ms.custom: 70131
ms.assetid: b1e0df43-b388-4326-8fb7-501f30c89776
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d3aa8b8ed35ec489ad48319ec15b66e75f9ab289
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819310"
---
# <a name="reverse-the-production-order-status"></a>Reversere produksjonsordrestatusen

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du tilbakefører statusen for en produksjonsordre. 

Hvis du tilbakestiller statusen for en produksjonsordre, tilbakestilles ordren og all operasjoner tilknyttet rutene, tilbake til et tidligere trinn i livssyklusen til produksjonen. Hvis du for eksempel en produksjonsordre har statusen **planlagte**, og du kan endre status tilbake til **opprettet**. I dette tilfellet må systemet først endre statusen til **Estimert**, som er statusen som er like forut for **Planlagt**. Statusen kan deretter endres til den statusen du ønsker, **Opprettet**. **Obs!** Hvis ordren har nådd statusen **Ferdigmeld**, kan du fremdeles tilbakestille den til en tidligere status. Du må imidlertid måtte kjøre anslag og grovplanlegging, finplanlegging eller begge typer planlegging på nytt, for å oppdatere informasjonen i ordren. Dette må gjøres fordi alle reserveringer av gjenværende vareforbruk og forbruk av operasjonsressurser også må tilbakestilles. Resten av denne artikkelen forklarer hva som skjer når du tilbakefører statusen for en produksjonsordre på følgende måter:

-   Fra **Estimert** til **Opprettet**
-   Fra **Planlagt** til **Estimert**
-   Fra **Frigitt** til **Planlagt**
-   Fra **Startet** til **Frigitt**

## <a name="from-estimated-to-created"></a>Fra Estimert til Opprettet
Når du tilbakefører statusen for en produksjonsordre fra **Estimert** til **Opprettet**, blir vareforbruket som ble beregnet for varene i stykklisten fjernet. Lagertransaksjoner på produksjonslinjen slettes, og **Gjenværende status**-feltet i produksjonsordrens stykklistelinjer tilbakestilles til **Avsluttet**. Når alternativene **Avledede innkjøp** og **Avledet produksjon** er valgt, slettes alle underliggende bestillinger eller produksjonsordrer. Hvis du har estimert kostnadene for produksjonsordren, eller hvis du manuelt har reservert varer slik at de kan brukes i produksjonen, fjernes disse transaksjonene.

## <a name="from-scheduled-to-estimated"></a>Fra Planlagt til Estimert
Når du tilbakefører statusen til en produksjonsordre fra **Planlagt** til **Estimert**, fjernes de planlagte start- og sluttdatoene og klokkeslettene. Kapasitetsreserveringer som ble gjort under planlegging, fjernes, og jobber som ble opprettet under finplanlegging, slettes. All informasjon som er registrert om grovplanlegging og finplanlegging på siden **Produksjonsordredetaljer**, tilbakestilles.

## <a name="from-released-to-scheduled"></a>Fra Frigitt til Planlagt
Når du tilbakefører statusen for en produksjonsordre fra **Frigitt** til **Planlagt**, er det eneste resultatet en endring i statusfeltet.

## <a name="from-started-to-released"></a>Fra Startet til Frigitt
Når du tilbakefører statusen for en produksjonsordre fra **Startet** til **Frigitt**, blir alle varer som er rapportert som avsluttet, tilbakestilt. Hvis emballasje er plukket, eller inngående og utgående leveringer er gjort til produksjon, tilbakeføres også disse innstillingene. **Gjenværende status**-feltet på stykklistelinjene i produksjonsordren endres fra **Avsluttet** til **Materialforbruk**. Hvis tidspunkt er registrert, eller hvis antall er blitt rapportert som fullført for operasjonene i produksjonsruten, tilbakeføres disse innstillingene. **Gjenværende status**-feltet endres fra **Avsluttet** til **Ruteforbruk** i produksjonsruten. Innstillingene for alle varer som blir postert som pågår eller varer i arbeid, blir tilbakeført. På siden **Produksjonsordredetaljer** tilbakestilles felt som viser et antall som ble startet eller ferdigmeldt. Datoene for disse transaksjonene tilbakestilles også.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]