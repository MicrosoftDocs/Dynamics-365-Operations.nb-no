---
title: Oversikt over utgående prosess
description: Denne artikkelen gir en oversikt over utgående prosess i Lagerstyring.
author: yufeihuang
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "274363"
- intro-internal
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 4e3c97862858e219d98b4ef9a81b52c6ab1623ab
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852483"
---
# <a name="outbound-process-overview"></a>Oversikt over utgående prosess

[!include [banner](../includes/banner.md)]

Denne artikkelen gir en oversikt over utgående prosess i Lagerstyring.

## <a name="output-orders"></a>Utleveringsordrer

Utleveringsordrer brukes for å koble salgsordrelinjer og overføringsordrelinjer med utgående plukkingprosesser som bruker plukklister.

Når plukklister genereres fra enten salgsordrer eller overføringsordrer, opprettes utleveringsosrdrer og forsendelser automatisk. En plukkliste har en en-til-en-relasjon med en forsendelse. Forsendelsen for overføringsordren eller pakkseddelen for salgsordren kan behandles fra forsendelsen. 

De følgende diagrammer viser en oversikt over prosesesen for utleveringsordrer. 

[![Oversikt over utgående ordreprosess.](./media/outbound-order.png)](./media/outbound-order.png)

Du kan sette opp utgående regler for å definere hvordan programmet skal håndtere den utgående prosessen. Du kan bruke disse reglene for å kontrolere forsendelsesprosessene. Spesielt kan du bruke reglene for å kontrollere hvilket stadium i prosessen en forsendelse kan sendes under. Følgende innstillinger definerer hvordan utgående prosesser håndteres.

## <a name="picking-route-status-for-sales-and-transfer-orders"></a>Plukkrutestatus for salgs- og overføringsordrer 

Gå til **Kundefordringer** \> **Oppsett** \> **Parametere for kundefordringer** og deretter i fanen **Oppdateringer** velger du en verdi i feltet **Plukkrutestatus** .

[![Felt for plukkrutestatus for salgsordrer.](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)

Hvis feltet **Plukkrutestatus** er satt til **Fullført** vil plukkprosessenen skje automatisk som en del av prosessen for å generere plukklister. Hvis feltet er satt til **Aktivert** må plukklistelinjer oppdateres manuelt.

Det samme oppsett gjelder for overføringsordrer. Gå til **Lagerstyring** \> **Oppsett** \> **Parametere for lagerstyring og administrasjon**, og deretter i fanen **Transport** velger du en verdi i feltet **Plukkrutestatus**.

[![Felt for plukkrutestatus for overføringsordrer.](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)

## <a name="end-output-inventory-orders"></a>Avsluttende lagerordre

Gå til **Lagerstyring** \> **Oppsett** \> **Parametere for lagerstyring og administrasjon**, og deretter i fanen **Generelt** velger du et alternativ i feltet **Lagerordre**.

[![Valg for å avslutte utgående lagerordre.](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)

Hvis lagerarbeideren reduserer antallet på plukklisten, fjernes de tilsvarende lagerantallene fra forsendelsen. Når plukklisten oppdateres på et tidspunkt, blir de gjenstående antallene rapportert tilbake til ordren hvis alternativet **Avslutt utleveringslagerordre** er satt til **Ja**. Hvis alternativet **Avslutt utleveringslagerordre** er satt til **Nei**, beholdes de gjenstående antallene som en åpen utgående ordremengde og må legges til en ny plukkliste som en del av funksjonen **Åpne utleveringsordrer**. 

[![Åpne utgangsordrerkommandoen i Funksjonsmenyen.](./media/open-output-order.png)](./media/open-output-order.png)

[![Funksjonsmenyen på siden Åpne utgående ordre.](./media/open-output-order-function.png)](./media/open-output-order-function.png)

## <a name="reduce-quantity"></a>Reduser antall

Den tredje parameteren du kan bruke som en del av prosessen med å generere plukklister, er **Reduser antallsparameteren** Innstillingen av dette parameterer arbeider sammen med **Reservasjon**-innstillingen som utløser en reservasjonsprosess som en del av frigivelsen til lageret.

[![Reduser antallsparameteren.](./media/reduce-quantity.png)](./media/reduce-quantity.png)

## <a name="example-of-an-outbound-process-for-a-sales-order"></a>Eksempel på en utgående prosess for en salgsordre

For dette eksempelet er det en salgsordre for to elementer. Under plukklistegenerering kan du velge **Redusere antall**-paremeteret. Derfor frigir du og oppretter plukklinjer kun for tilgjengelig lager på stedet. Plukkingen må rapporteres via en registreringsprosess for plukklister (**Plukkrutestatus** = **Aktivert**).

Lagerbeholdningen som ikke allerede er reservert, er reservert under plukklistegenerering. Den utilgjengelige beholdningen kan enten fjernes fra salgsordren eller frigis til lageret for utgående prosess senere, når lager er tilgjengelig for plukking.

[![Oppdater plukklisten.](./media/update-picking-list.png)](./media/update-picking-list.png)

Så snart alle plukklinjer er plukket på siden **Plukklisteregistrering**, er den tilknyttede forsendelsen komplett. Prosessen for pakksedler for salgsordrer kan deretter initialiseres basert det på plukkede inventar.

[![Oppdater ugående forsendelser.](./media/outbound-shipments.png)](./media/outbound-shipments.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]