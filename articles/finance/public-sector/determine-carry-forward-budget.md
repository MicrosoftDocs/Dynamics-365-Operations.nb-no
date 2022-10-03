---
title: Oppdatere overføringsbudsjettet etter reduksjoner i bestillinger og fakturaer
description: Denne artikkelen beskriver hvordan du kan styre hva som skjer med overføringsbudsjettet når bestillinger annulleres eller reduseres, og når fakturaer reduseres.
author: TaylorVH
ms.date: ''
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: TaylorVH
ms.search.validFrom: 2022-02-01
ms.dyn365.ops.version: Version 1611
ms.search.form: LedgerFund
ms.openlocfilehash: 790f1e770fd77d5209436c1c89e0f6125aac150f
ms.sourcegitcommit: 1a7729a6ce4f3fcf68bdc4cfdad746a5553da3c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573053"
---
# <a name="update-the-carry-forward-budget-after-reductions-in-purchase-orders-and-invoices"></a>Oppdatere overføringsbudsjettet etter reduksjoner i bestillinger og fakturaer

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Denne artikkelen beskriver hvordan du kan styre hva som skjer med overføringsbudsjettet når bestillinger annulleres eller reduseres, og når fakturaer reduseres.

Hvis du vil ha informasjon om hvordan bestillinger behandles ved årsskiftet, kan du se [Behandle bestillinger ved årsskiftet](/dynamicsax-2012/appuser-itpro/process-purchase-orders-at-year-end).

## <a name="turn-carry-forward-budget-reductions-for-invoice-variances-on-or-off"></a>Aktivere eller deaktivere overføringsbudsjettreduksjoner for fakturaavvik

Systemet kan alltid oppdatere overføringsbudsjettet når en overføringsbestilling avbrytes eller reduseres. Hvis du imidlertid vil oppdatere overføringsbudsjettet når en faktura reduseres, må du aktivere funksjonen *Reduser overføringsbudsjett når en faktura mot en bestilling reduseres med et avvik*. Administratorer kan aktivere eller deaktivere denne funksjonaliteten i arbeidsområdet **[Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)**.

## <a name="purchase-order-reductions-and-cancellations"></a>Reduksjoner og annulleringer av bestillinger

Uansett om budsjettet for funksjonen *Reduser overføringsbudsjett når en faktura mot en bestilling reduseres med et avvik* er aktivert, vil overføringsbudsjettet oppdateres når en kvalifiserende bestilling annulleres eller reduseres. Du kan angi at hvert finansfond skal svare på en av følgende måter:

- Behold overføringsbudsjettet slik det ble opprettet.
- Juster overføringsbudsjettet automatisk for å fjerne det annullerte eller reduserte beløpet.

Bare bestillingslinjer som har distribusjoner som omfatter et fond, er tilgjengelige for automatisk budsjettjustering. Den automatiske budsjettjusteringen skjer når bestillingen er ferdig eller en bestillingsreduksjon bekreftes.

## <a name="invoice-reductions"></a>Fakturareduksjoner

Når funksjonen *Reduser overføringsbudsjett når en faktura mot en bestilling reduseres med et avvik* er aktivert, kan du angi om hvert fond skal redusere overføringsbudsjettet når en faktura reduseres, i tillegg til når en bestilling annulleres eller reduseres. Fakturaen må være for en bestilling som har et bærende budsjett. Reduksjoner omfatter prisavvik, gebyravvik og mva-avvik. Når en overføringsbestilling reduseres under fakturering, opprettes det et avvik. Når fakturaen er postert, vil bestillingsdisposisjoner reduseres med beløpet for avviket. Funksjonen oppretter også automatisk budsjettjustering for avviksbeløpet.

Når funksjonen *Reduser overføringsbudsjett når en faktura mot en bestilling reduseres med et avvik* er slått av, reduseres ikke overføringsbudsjettet i dette scenarioet. Derfor blir det gjenstående overføringsbudsjettet for avviksbeløpet værende.

## <a name="configure-the-carry-forward-budget-options-for-each-fund"></a>Konfigurere alternativene for overføringsbudsjett for hvert fond

Følg denne fremgangsmåten for hvert finansfond som skal kunne redusere overføringsbudsjett når en bestilling eller faktura reduseres.

1. Gå til **Økonomimodul \> Kontoplan \> Fond \> Fond**.
1. Velg fondet du vil opprette.
1. Under **Årsavslutningsprosess for bestilling** du kontrollere at alternativet **Overstyr valgt alternativ for årsavslutning** er satt til *Ja*.
1. Under **Status for overført budsjett** angir du feltet **Gjenoppta budsjettet når en overføringsbestilling avbrytes eller reduseres** etter behov. Innstillingene har litt forskjellige virkninger, avhengig av om budsjettet for *Reduser overføringsbudsjett når en faktura mot en bestilling reduseres med et avvik* er aktivert i systemet.

    - Når funksjonen er slått av, reaktiverer systemet bare annullerte eller reduserte bestillinger. Alternativinnstillingene fungerer på følgende måte:

        - *Nei* – Systemet oppretter en budsjettregisteroppføring for den gjenværende saldoen til bestillinger som er avbrutt eller redusert.
        - *Ja* – Systemet tillater at bestillinger kan avbrytes eller reduseres, men oppretter ikke en budsjettregisteroppføring. Overføringsbudsjettet er fortsatt tilgjengelig for forbruk av andre dokumenter.

    - Når funksjonen er slått på, reaktiverer systemet både på fakturavariasjoner og annullerte eller reduserte bestillinger. Alternativinnstillingene fungerer på følgende måte:

        - *Nei* – For fakturaavvik oppretter systemet en budsjettregisteroppføring mot bestillingen for avviksreduksjonsbeløpet. For annullerte eller reduserte bestillinger har denne innstillingen samme effekt som den har når funksjonen er slått av.
        - *Ja* – Når det gjelder fakturaavvik, tillater systemet fakturareduksjonen, men oppretter ikke en budsjettregisteroppføring. Overføringsbudsjettet er fortsatt tilgjengelig for forbruk av andre dokumenter. For annullerte eller reduserte bestillinger har denne innstillingen samme effekt som den har når funksjonen er slått av.

## <a name="additional-resources"></a>Tilleggsressurser

- [Behandle bestillinger ved årsavslutning](/dynamicsax-2012/appuser-itpro/process-purchase-orders-at-year-end)
- [Oppretthold generelle budsjettreservasjoner](general-budget-reservation-tasks.md)
- [Midler i offentlig sektor](funds-public-sector.md)
- [Definere finansiering i offentlig sektor](tasks/set-up-fund-public-sector.md)
