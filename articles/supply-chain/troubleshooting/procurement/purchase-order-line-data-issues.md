---
title: Dataavvik på bestillingslinje
description: Du ser dataavvik eller skadede data på bestillingslinjene.
author: SmithaNataraj
ms.date: 12/07/2021
ms.topic: troubleshooting
ms.search.form: PurchLineManualCorrection, PurchTable, PurchLine, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-12-07
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: ee2cb9a07c8a00a92c71e3e99d8ec20aa27fb20e
ms.sourcegitcommit: b9799a58d6ec221df86788bc37c4fbd28b435e89
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/08/2022
ms.locfileid: "8100805"
---
# <a name="purchase-order-line-data-discrepancies"></a>Dataavvik på bestillingslinje

## <a name="symptoms"></a>Symptomer

Når du undersøker linjene i en bestilling, legger du merke til et eller flere av følgende problemer:

- Det er et dataavvik eller skadede data i leverings- eller fakturarester på bestillingslinjen.
- Det er skadede data på en bestillingslinje eller i en hodestatus.
- Du kan ikke fakturere en bestilling fordi du for eksempel får en eller flere av følgende feilmeldinger:

    - «Stoppet (feil): Transaksjonen er allerede postert.»
    - «Antallet kan ikke faktureres på grunn av utilstrekkelige lagertransaksjoner med status mottatt.»
    - «Utilstrekkelige lagertransaksjoner med statusen Kjøpt for antallet %1 av varen %0.»

- Du kan ikke fullføre eller lukke en bestilling på grunn av for eksempel et av følgende problemer:

    - **Fullfør**-knappen er ikke tilgjengelig.
    - Du kan ikke annullere det bestilte antallet på en bestillingslinje for en bestilling som med statusen bekreftet eller mottatt.

## <a name="cause"></a>Årsak

Årsaken til disse problemene er vanligvis skadede data eller et avvik i restantallene for en eller flere bestillingslinjer.

## <a name="resolution"></a>Løsning

Du kan vanligvis løse disse problemene ved å oppdatere bestillingsstatusen, leveringsrestene og/eller fakturarestene for de relevante bestillingslinjene, som beskrevet i fremgangsmåten nedenfor.

1. Gå til **Innkjøp og leverandører \> Periodiske oppgaver \> Opprydding \> Korriger bestillingslinjer manuelt**.
1. I **Bestilling**-feltet finner og velger du bestillingen som gir deg problemer.
1. Velg en linje der du fant et avvik, i **Bestillingslinjer**-delen.
1. I **Lagertransaksjoner**-delen undersøker du dataene som vises. Hvis du legger merke til inkonsekvenser mellom en bestillingslinje og lagertransaksjonene, velger du en av følgende kommandoer i handlingsruten, avhengig av hvor du ser inkonsekvensene:

    - **Omberegn \> Omberegn leveringsrest** – Oppdater bestillingslinjen og hodestatusene automatisk. Denne funksjonen fungerer bare for lagerførte bestillingslinjer (det vil si linjer der varen er en lagerført vare). Det er foreløpig ikke støtte for ikke-lagerførte varer og faktisk vekt-varer.
    - **Omberegn \> Omberegn fakturarest** – Oppdater bestillingslinjen og hodestatusene automatisk. Denne funksjonen fungerer bare for lagerførte bestillingslinjer (det vil si linjer der varen er en lagerført vare). Det er foreløpig ikke støtte for ikke-lagerførte varer og faktisk vekt-varer.
    - **Omberegn \> Omberegn status** – Omberegn statusen for den valgte linjen. Denne beregningen er basert på den eksisterende logikken. Hodestatusen for bestillingen oppdateres derfor etter behov, basert på den nye statusen for bestillingslinjen.

1. Hvis du fortsatt ser inkonsekvenser i restantallene, kan du bruke følgende felter til å redigere dem direkte etter behov:

    - Leveringsrest
    - Leveringsrest for lager
    - Fakturarest
    - Fakturarest for lager
