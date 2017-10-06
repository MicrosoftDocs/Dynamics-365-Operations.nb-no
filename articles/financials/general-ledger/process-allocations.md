---
title: Behandle tildelinger
description: "Denne artikkelen inneholder informasjon om tildelinger, alternativene for behandling av dem i Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, og hvordan de kan brukes i planleggingen av budsjettet. Tildelinger brukes til å distribuere beløp på tvers av flere kombinasjoner av finanskonti. De bidrar til å garantere at utgifter eller inntekter belastes til riktig objekt i regnskapet."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 298ac47e2253f8add1aa3938dda15afe186afbeb
ms.openlocfilehash: e6d88503972850f6163aba6b45547a111f44abab
ms.contentlocale: nb-no
ms.lasthandoff: 06/20/2017


---

# <a name="process-allocations"></a>Behandle tildelinger

[!include[banner](../includes/banner.md)]


Denne artikkelen inneholder informasjon om tildelinger, alternativene for behandling av dem i Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, og hvordan de kan brukes i planleggingen av budsjettet. Tildelinger brukes til å distribuere beløp på tvers av flere kombinasjoner av finanskonti. De bidrar til å garantere at utgifter eller inntekter belastes til riktig objekt i regnskapet.

Microsoft Dynamics 365 for Finance and Operations har følgende funksjonalitet for å støtte denne prosessen:

-   Fordel transaksjonsbeløpene manuelt ved hjelp av Del-handlingen regnskapsdistribusjoner, eller ved å bruke standardmaler for finansdimensjon på et dokument. Hvis du vil ha mer informasjon, kan du se [Regnskapsdistribusjoner](../accounts-payable/accounting-distributions.md).
-   Fordel transaksjonsbeløp automatisk basert på fordelingsbetingelser som er definert på den individuelle hovedkontoen. Tildelingskontooppføringer genereres for hver journal basert på prosentandelen og finanskontoen når en regnskapsoppføring oppfyller vilkårene som er definert som kildefinanskontoen.
-   Fordel finanssaldoer eller faste beløp automatisk basert på finansfordelingsregler. Finansfordelingsreglene behandles på periodisk basis ved hjelp av fordelingsjournaler. 

###  <a name="allocations-in-budget-planning"></a>Fordelinger i budsjettplanlegging

Finansfordelingsregler kan brukes for budsjettplaner. Når du bruker finansfordelingsregler i budsjettplanlegging, fungerer fordelingsreglene på samme måte som de hadde gjort i Finans, men kildedataene og måldataene kommer fra budsjettplanen. Du kan manuelt velge finansfordelingsregler som skal brukes for budsjettplaner. Alternativt kan du bruke en fordelingsplan som kjører som en del av en arbeidsflytprosess.

> [!NOTE]
> Du kan ikke bruke konserinterne finansfordelingsregler for budsjettplanlegging.





