---
title: Partiattributter
description: Denne artikkelen inneholder informasjon om bunkeattributter. Partiattributter er egenskaper til råvarer og ferdige produkter som utgjør lagerpartier. Artikkelen forklarer også hvordan du tilordner bunkeattributter, og hvordan du kan søke etter dem når du reserverer partier.
author: johanhoffmann
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup, WHSBatchAttribReserve
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e5f5a03df63cf4fa90b5e9e67082a0d60eef9afc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899389"
---
# <a name="batch-attributes"></a>Partiattributter

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder informasjon om bunkeattributter. Partiattributter er egenskaper til råvarer og ferdige produkter som utgjør lagerpartier. Artikkelen forklarer også hvordan du tilordner bunkeattributter, og hvordan du kan søke etter dem når du reserverer partier.

Partiattributter er egenskaper til råvarer og ferdige produkter som utgjør lagerpartier. Partiattributter kan variere, avhengig av en rekke faktorer, for eksempel miljøfaktorer eller kvaliteten på råvarene som er brukt til å produsere partiet, eller resultatet av det ferdige produktet. Antallet av og typene partiattributter som brukes, kan variere kraftig i de ulike bransjene. Her er to eksempler som viser hvordan du bruker partiattributter:

-   I osteindustrien kan melk, som er en av råvarene som brukes i produksjonen av ost, ha attributter som for eksempel fettinnhold og prosentvekt. Osten som produseres av melken, kan ha andre attributter, for eksempel fuktighet og alder.
-   I stålindustrien kan jern som produseres, ha attributter som for eksempel prosenter av magnesiuminnhold, sølvinnhold og sinkinnhold.

For å få bedre styring av antall og typer attributter, kan du bruke partiattributtgrupper. På denne måten trenger du ikke legge til hvert attributt individuelt.

## <a name="assign-batch-attributes"></a>Tilordne partiattributter
Du kan tilordne partiattributter til individuelle produkter som er i lagerparti, eller du kan tilordne dem til produkter som er knyttet til bestemte kunder. Før du kan tilordne et partiattributt på kundenivå, må du tilordne det på produktnivå. Produktet må ha partidimensjonen satt til **Aktiv** i sporingsdimensjonsgruppen. Hvis du vil tilordne et partiattributt til et enkelt produkt, kan du bruke produktspesifikk-siden. Hvis attributtet er spesifikt for et produkt for en kunde, bruker du kundespesifikk-siden. Når du legger til et attributt til et produkt, kan du også angi andre parametere. Her er noen eksempler:

-   Minimums- og maksimumsområdene for et attributt av typen **Heltall** eller **Brøk**.
-   Toleransehandlinger for et attributt av typen **heltall** eller **brøk**. Hvis verdien til attributtet faller utenfor minimums- og maksimumsområdet, kan handlingen enten være en advarsel eller en feilmelding.
-   Målverdien for attributtet. Denne verdien er den optimale verdien for attributtet, og den gjelder for alle attributtyper.

Du kan få tilgang til sidene for produkter som du velger på siden **Frigitte produkter** i Behandling av produktinformasjon. Når du har tilordnet partiattributter til et produkt, kan du legge til bestemte verdier i attributtene på siden **Lagerpartiattributter**.

## <a name="reserve-batches"></a>Reservere partier 
Du kan søke i partiattributter når du utfører partireservasjoner for en salgsordre for å oppfylle en kundeordre, eller når du plukker og reserverer partier for en produksjonsordre. Søket bidrar til å finne et lagerparti som inneholder produktet som har partiattributtet du vil bruke. Når du har funnet partiet eller partiene, kan du reservere produktet til den opprinnelige lagertransaksjonslinjen.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]