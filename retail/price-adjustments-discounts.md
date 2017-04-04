---
title: Prisjusteringer og rabatter
description: Denne artikkelen inneholder informasjon om prisjusteringer og rabatter i detaljhandelen og handel i Microsoft Dynamics 365 for operasjoner.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 01f249cbdabc6febf23dcd7103d4587cecdaad08
ms.lasthandoff: 03/31/2017


---

# <a name="price-adjustments-and-discounts"></a>Prisjusteringer og rabatter

Denne artikkelen inneholder informasjon om prisjusteringer og rabatter i detaljhandelen og handel i Microsoft Dynamics 365 for operasjoner.

I Dynamics 365 for operasjoner - detaljhandel, du kan justere prisen til produkter, og kan også sette opp rabatter som gjelder for et linjeelement eller en transaksjon ved salg (POS), i en samtale center ordre eller i en online-bestillingen. Både prisjusteringer og rabatter kan knyttes til prisgrupper. Du kan angi én enkelt startdato og sluttdato eller en regelmessig periode, en rabattkode og noen ytterligere attributter for både prisjusteringer og rabatter. Prisjusteringer og rabatter kan brukes på produkter, varianter eller hierarkier. Hvis mer enn én rabatt gjelder for et produkt, kan en kunde få enten en av rabattene eller en kombinert rabatt, avhengig av konfigurasjonen av rabatten. Dynamics 365 for operasjoner bruker automatisk rabatt eller kombinasjon av rabatter som gir den beste prisen til kunden. Når du definerer en prisjustering eller rabatt, må du bekrefte at prisgrupper tilordnes til riktige kanaler, kataloger, tilknytninger eller fordelsprogrammer som du vil at rabatten skal gjelde for. Hvis du i tillegg vil generere rabatt-ID-en automatisk, kan du definere nummerserier på **Detaljhandelsparametere**-siden før du definerer en ny rabatt eller prisjustering. **Obs!** Du kan slette en prisjustering eller rabatt. Statistisk informasjon går imidlertid tapt.

### <a name="types-of-discounts"></a>Rabattyper

Det finnes fire typer detaljhandelsrabatter:

-   **Enkel rabatt** – en enkelt prosent eller et enkelt beløp.
-   **Kvantumsrabatt** – en rabatt som brukes når to eller flere varer som kjøpes.
-   **Samlerabatt** – en rabatt som brukes ved kjøp av en bestemt kombinasjon av produkter.
-   **Terskelrabatt** – en rabatt som brukes når totalen for transaksjonen er mer enn et bestemt beløp.

Både prisjusteringer og rabatter kan knyttes til prisgrupper. Prisgrupper kan deretter knyttes til kanaler, kataloger, tilknytninger og fordelsprogrammer.


