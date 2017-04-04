---
title: Vedlikehold planlagte ordrer
description: Denne artikkelen gir informasjon om hvordan du behandler planlagte ordrer. Den beskriver hvordan du kan oppdatere statusen for planlagte ordrer, autorisere dem og filtrere etter planlagte ordrer som har samme status som en valgt planlagt ordre.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: c01a192e637bfe74a60370290db72c439faf40d0
ms.lasthandoff: 03/31/2017


---

# <a name="maintain-planned-orders"></a>Vedlikehold planlagte ordrer

Denne artikkelen gir informasjon om hvordan du behandler planlagte ordrer. Den beskriver hvordan du kan oppdatere statusen for planlagte ordrer, autorisere dem og filtrere etter planlagte ordrer som har samme status som en valgt planlagt ordre.

Du kan administrere planlagte bestillinger fra arbeidsområdet **Hovedplanlegging**, listen **Planlagt bestilling** eller listene **Planlagte produksjonsordrer**, **Planlagte bestillinger** og **Overføringsforslag**. Du kan bruke **Status**-feltet til å spore fremdriften. Følgende verdier brukes:

-   Når hovedplanlegging genererer planlagte ordrer, har de planlagte ordrene statusen **Ubehandlet**.
-   Hvis du velger ikke å autorisere en planlagt bestilling, kan du gi den statusen **Fullført**.
-   Når du velger å autorisere en planlagt bestilling, kan du gi den statusen **Godkjent**. Denne statusen innebærer at du godkjenner autoriseringen av den planlagte bestillingen, men den er ikke autorisert ennå.

**Obs!** En godkjent planlagt bestilling overføres i gjeldende tilstand til neste hovedplanberegning. Du kan autorisere planlagte bestillinger ved å klikke **Autoriser**. Du kan autorisere følgende planlagte bestillinger:

-   Den planlagte bestillingen som er merket.
-   Flere planlagte bestillinger.
-   Planlagte bestillinger som genereres gjennom en nedbryting fra siden **Nedbryting**. Klikk **Planlagte bestillinger**, merk den planlagte bestillingen, og klikk deretter **Autoriser**.

Når en planlagt bestilling autoriseres, flyttes den til bestillingsdelen i den aktuelle modulen. **Obs!** Du kan høyreklikke en planlagt bestilling med en bestemt status og filtrere etter andre planlagte bestillinger med samme status. Denne funksjonen er nyttig hvis du for eksempel vil filtrere etter alle planlagte bestillinger med statusen **Godkjent**, slik at du deretter kan autorisere dem.

<a name="see-also"></a>Se også
--------

[Master plans](master-plans.md)


