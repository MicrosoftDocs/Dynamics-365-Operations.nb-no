---
title: Vedlikeholde planlagte ordrer
description: Dette emnet gir informasjon om hvordan du behandler planlagte ordrer. Den beskriver hvordan du kan oppdatere statusen for planlagte ordrer, autorisere dem og filtrere etter planlagte ordrer som har samme status som en valgt planlagt ordre.
author: roxanadiaconu
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7f97dc4627f9bb3a0ac2020b966de7e58aafcedc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833671"
---
# <a name="maintain-planned-orders"></a>Vedlikeholde planlagte ordrer

[!include [banner](../includes/banner.md)]

Dette emnet gir informasjon om hvordan du behandler planlagte ordrer. Den beskriver hvordan du kan oppdatere statusen for planlagte ordrer, autorisere dem og filtrere etter planlagte ordrer som har samme status som en valgt planlagt ordre.

Du kan administrere planlagte bestillinger fra arbeidsområdet **Hovedplanlegging**, listen **Planlagt bestilling** eller listene **Planlagte produksjonsordrer**, **Planlagte bestillinger** og **Overføringsforslag**. 

## <a name="planned-order-status"></a>Status for planlagt ordre
Du kan bruke **Status**-feltet til å spore fremdriften. Følgende verdier brukes:

-   Når hovedplanlegging genererer planlagte ordrer, har de planlagte ordrene statusen **Ubehandlet**.
-   Hvis du velger ikke å autorisere en planlagt bestilling, kan du gi den statusen **Fullført**.
-   Hvis du vil autorisere en planlagt ordre, kan du endre statusen til **Godkjent**. Planlagte ordrer med **Godkjent**-status overholdes av hovedplanlegging, slik at de ikke blir endret eller slettet under en senere kjøring av hovedplanlegging. For å oppnå dette kopierer planleggingslogikken de **godkjente** planlagte bestillingene fra den gamle planversjonen til den nye planversjonen under hovedplanlegging.

## <a name="firming-planned-orders"></a>Autorisere planlagte ordrer 
Ved å autorisere planlagte ordre opprettes det reelle ordrer. Disse kalles også *frigitte* eller *åpne ordrer*. Når en planlagt bestilling autoriseres, flyttes den til bestillingsdelen i den aktuelle modulen.

Du kan velge to autorisasjonsalternativer fra siden **Planlagte ordrer**:

-   **Autoriser** – Dette vil autorisere én eller flere valgte, planlagte ordrer.
-   **Autoriser alle** – Dette vil autorisere alle planlagte ordrer i filteret. Hvis du bruker **Autoriser alle** trenger du ikke velge den planlagte ordren. Alle planlagte ordrer i filteret bli autorisert. Dette alternativet kan være nyttig hvis du autoriserer et stort antall planlagte ordrer.

> [!NOTE]
> Du kan spore en planlagt ordre som ble autorisert fra **Autorisasjonshistorikk** under **skjemaet Planlagte ordrer > Vis > Autorisasjonshistorikk**.

## <a name="parallelize-firming"></a>Parallelliser autorisasjon
Hvis du planlegger å autorisere mange ordrer samtidig, kan parallellisering av kjøringen forbedre kjøretiden eller ytelsen. Dette alternativet er tilgjengelig ved autorisering av flere planlagte orderer med **Autoriser** eller **Autoriser alle**. Følgende parametere er tilgjengelige:

-   **Parallellisering av autorisering** – Hvis **Ja**, vil autoriseringsprosessen parallelliseres med antallet tråder som er definert i **Antall tråder**.
-   **Antall tråder** – Bestemmer antall tråder som brukes til å parallellisere autoriseringsprosessen. Parameteren vises bare når **Parallellisering av autorisering** er satt til **Ja.**

> [!NOTE]
> Alternativet for **Parallelliser autorisasjon** vises bare når du har mer enn én planlagt bestilling som er valgt for autorisasjon.

<a name="additional-resources"></a>Tilleggsressurser
--------

[Oversikt over hovedplaner](master-plans.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]