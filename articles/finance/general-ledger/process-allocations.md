---
title: Behandle tildelinger
description: Denne artikkelen inneholder informasjon om tildelinger, alternativene for behandling av dem i Microsoft Dynamics 365 Finance, og hvordan de kan brukes i planleggingen av budsjettet. Tildelinger brukes til å distribuere beløp på tvers av flere kombinasjoner av finanskonti. De bidrar til å sikre at utgifter eller inntekter belastes til riktig objekt i regnskapet.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: roschlom
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 30f445698eddba8bdbb2ac9a257142458fb5990f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815434"
---
# <a name="process-allocations"></a>Behandle tildelinger

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder informasjon om tildelinger, alternativene for behandling av dem og hvordan de kan brukes i planleggingen av budsjettet. Tildelinger brukes til å distribuere beløp på tvers av flere kombinasjoner av finanskonti. De bidrar til å sikre at utgifter eller inntekter belastes til riktig objekt i regnskapet.

Følgende funksjoner støtter denne prosessen:

-   Fordel transaksjonsbeløpene manuelt ved hjelp av Del-handlingen regnskapsdistribusjoner, eller ved å bruke standardmaler for finansdimensjon på et dokument. Hvis du vil ha mer informasjon, kan du se [Regnskapsdistribusjoner](../accounts-payable/accounting-distributions.md).
-   Fordel transaksjonsbeløp automatisk basert på fordelingsbetingelser som er definert på den individuelle hovedkontoen. Tildelingskontooppføringer genereres for hver journal basert på prosentandelen og finanskontoen når en regnskapsoppføring oppfyller vilkårene som er definert som kildefinanskontoen. Hvis du vil ha mer informasjon, kan du se [Tildelingsbetingelser for hovedkonto](../general-ledger/main-account-allocation-terms.md).
-   Fordel finanssaldoer eller faste beløp automatisk basert på finansfordelingsregler. Finansfordelingsreglene behandles på periodisk basis ved hjelp av fordelingsjournaler. Hvis du vil ha mer informasjon, kan du se [Tilordningsregler](../general-ledger/ledger-allocation-rules.md).

###  <a name="allocations-in-budget-planning"></a>Fordelinger i budsjettplanlegging

Finansfordelingsregler kan brukes for budsjettplaner. Når du bruker finansfordelingsregler i budsjettplanlegging, fungerer fordelingsreglene på samme måte som de hadde gjort i Finans, men kildedataene og måldataene kommer fra budsjettplanen. Du kan manuelt velge finansfordelingsregler som skal brukes for budsjettplaner. Alternativt kan du bruke en fordelingsplan som kjører som en del av en arbeidsflytprosess.

> [!NOTE]
> Du kan ikke bruke konserinterne finansfordelingsregler for budsjettplanlegging.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]