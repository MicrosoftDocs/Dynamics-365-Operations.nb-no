---
title: Ofte stilt spørsmål om salgsordrer
description: Denne siden tar opp vanlige spørsmål som dukker opp når du arbeider med salgsordrer i Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 3cee75b1d740e7cb414c674157dde0146e8faa50
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571623"
---
# <a name="sales-order-faqs"></a>Vanlige spørsmål om salgsordre

Denne siden tar opp vanlige spørsmål som dukker opp når du arbeider med salgsordrer i Dynamics 365 Supply Chain Management.

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a>Kan jeg koble en bestilling til en salgsordre for å imøtekomme etterspørselen?

Du kan opprette en bestilling fra en salgsordre. Hvis du vil ha mer informasjon, se [Opprette en bestilling fra en salgsordre](/dynamics365/supply-chain/sales-marketing/tasks/create-purchase-order-sales-order).

## <a name="can-i-cancel-or-delete-a-sales-order-or-return-order"></a>Kan jeg avbryte eller slette en salgsordre eller returordre?

Du kan bare kansellere salgsordrer og returordrer som har statusen *Opprettet*. Hvis du vil ha mer informasjon, se [Annullere en returordre](/dynamics365/supply-chain/service-management/cancel-return-order).

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a>Kan jeg gjenopprette en fakturert salgsordre som er slettet?

Hvis en fakturert salgsordre ble slettet ved en feiltakelse, kan du gjenopprette den eller vise detaljene for den.

Gå til **Kundekonto \> Transaksjoner \> Opprinnelig dokument \> Vis detaljer**. Finn fakturaen du er på jakt etter, og velg den for å vise detaljene for den. Disse detaljene omfatter salgsordrereferansen. Du bør også få tilgang til salgsordredetaljene fra denne siden.

## <a name="how-do-i-delete-orphaned-sales-order-records"></a>Hvordan sletter jeg frittstående salgsordreposter?

Hvis du vil rydde opp i frittstående salgsordreposter, kan du kjøre den periodiske jobben *Salgsordresletting* ved å gå til et av følgende steder:

- Salg og markedsføring \> Periodiske oppgaver \> Opprydding \> Slett salgsordrer
- Detaljhandel og handel \> IT for Detaljhandel og handel \> Opprydding \> Slett salgsordrer

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a>Finnes det en måte å beregne provisjon på fakturaer som allerede er postert?

Supply Chain Management støtter for øyeblikket ikke beregningen av provisjoner for posterte fakturaer.
