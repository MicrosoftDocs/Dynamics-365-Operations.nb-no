---
title: "Utgående prosess"
description: "Dette emnet gir en oversikt over utgående prosess i Lagerstyring."
author: perlynne
manager: AnnBe
ms.date: 10/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: 9c09a7bd314bb9005eb0b6c69d7cccad1c30cfdb
ms.openlocfilehash: 7b395cab2184f8f9f3f50a7a595c6ed782645323
ms.contentlocale: nb-no
ms.lasthandoff: 10/04/2017

---

# <a name="outbound-process"></a>Utgående prosess

[!include[banner](../includes/banner.md)]

Dette emnet gir en oversikt over utgående prosess i Lagerstyring.

## <a name="output-orders"></a>Utleveringsordrer

Utleveringsordrer brukes for å koble salgsordrelinjer og overføringsordrelinjer med utgående plukkingprosesser som bruker plukklister.

Når plukklister genereres fra enten salgsordrer eller overføringsordrer, opprettes utleveringsosrdrer og forsendelser automatisk. En plukkliste har en en-til-en-relasjon med en forsendelse. Forsendelsen for overføringsordren eller pakkseddelen for salgsordren kan behandles fra forsendelsen. 

De følgende diagrammer viser en oversikt over prosesesen for utleveringsordrer. 

[![Oversikt over utgående ordreprosess](./media/outbound-order.png)](./media/outbound-order.png)

Du kan sette opp utgående regler for å definere hvordan programmet skal håndtere den utgående prosessen. Du kan bruke disse reglene for å kontrolere forsendelsesprosessene. Spesielt kan du bruke reglene for å kontrollere hvilket stadium i prosessen en forsendelse kan sendes under. Følgende innstillinger definerer hvordan utgående prosesser håndteres.

## <a name="picking-route-status-for-sales-and-transfer-orders"></a>Plukkrutestatus for salgs- og overføringsordrer 

Gå til **Kundefordringer** \> **Oppsett** \> **Parametere for kundefordringer** og deretter i kategorien **Oppdateringer** velger du en verdi i feltet **Plukkrutestatus** .

[![Felt for plukkrutestatus for salgsordrer](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)

Hvis feltet **Plukkrutestatus** er satt til **Fullført** vil plukkprosessenen skje automatisk som en del av prosessen for å generere plukklister. Hvis feltet er satt til **Aktivert** må plukklistelinjer oppdateres manuelt.

Det samme oppsett gjelder for overføringsordrer. Gå til **Lagerstyring** \> **Oppsett** \> **Parametere for lagerstyring og administrasjon**, og deretter i kategorien **Transport** velger du en verdi i feltet **Plukkrutestatus**.

[![Felt for plukkrutestatus for overføringsordrer](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)

## <a name="end-output-inventory-orders"></a>Avsluttende lagerordre

Gå til **Lagerstyring** \> **Oppsett** \> **Parametere for lagerstyring og administrasjon**, og deretter i kategorien **Generelt** velger du et alternativ i feltet **Lagerordre**.

[![Valg for å avslutte utgående lagerordre](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)

Noen ganger kan enkelte elementer i lager ikke plukkes som en del av plukklisteprosessen. For eksempel kan denne situasjonen oppstå hvis en lagerarbeider reduserer mengdene på plukklinjer og behandler plukklisten. Hvis valget **Avslutt utgående lagerordre** er satt til **Ja**, vil gjenværende uplukkede antall rapporteres tilbake til ordrenivå. Hvis dette alternativet er satt til **Nei**, vil gjenværende uplukkede antall beholdes som en åpen utgående ordremengde. I dette tilfellet forblir mengdene frigitt til lageret og må legges til en ny plukkliste som en del av funksjonaliteten **Åpne utgangsordrer**.

[![Åpne utgangsordrerkommandoen i Funksjonsmenyen](./media/open-output-order.png)](./media/open-output-order.png)

[![Funksjonsmenyen på siden Åpne utgående ordre](./media/open-output-order-function.png)](./media/open-output-order-function.png)

## <a name="reduce-quantity"></a>Reduser antall

Den tredje parameteren du kan bruke som en del av prosessen med å generere plukklister, er **Reduser antallsparameteren** Innstillingen av dette parameterer arbeider sammen med **Reservasjon**-innstillingen som utløser en reservasjonsprosess som en del av frigivelsen til lageret.

[![Reduser antallsparameteren](./media/reduce-quantity.png)](./media/reduce-quantity.png)

## <a name="example-of-an-outbound-process-for-a-sales-order"></a>Eksempel på en utgående prosess for en salgsordre

For dette eksempelet er det en salgsordre for to elementer. Under plukklistegenerering kan du velge **Redusere antall**-paremeteret. Derfor frigir du og oppretter plukklinjer kun for tilgjengelig lager på stedet. Plukkingen må rapporteres via en registreringsprosess for plukklister (**Plukkrutestatus** = **Aktivert**).

Lagerbeholdningen som ikke allerede er reservert, er reservert under plukklistegenerering. Den utilgjengelige beholdningen kan enten fjernes fra salgsordren eller frigis til lageret for utgående prosess senere, når lager er tilgjengelig for plukking.

[![Oppdater plukklisten](./media/update-picking-list.png)](./media/update-picking-list.png)

Så snart alle plukklinjer er plukket på siden **Plukklisteregistrering**, er den tilknyttede forsendelsen komplett. Prosessen for pakksedler for salgsordrer kan deretter initialiseres basert det på plukkede inventar.

[![Oppdater ugående forsendelser](./media/outbound-shipments.png)](./media/outbound-shipments.png)
