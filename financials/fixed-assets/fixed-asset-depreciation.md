---
title: Avskrivning av anleggsmidler
description: Denne artikkelen gir en oversikt over avskrivning for anleggsmidler.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetBonus, AssetBookTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: b0c82708209fd937a5399aa8cc64775b3fb739e6
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="fixed-asset-depreciation"></a>Avskrivning av anleggsmidler

[!include[banner](../includes/banner.md)]


Denne artikkelen gir en oversikt over avskrivning for anleggsmidler.

Avskrivning er en periodisk transaksjon som vanligvis reduserer verdien til anleggsmidlene i balansen, og kostnadsføres som en utgift i en resultatkonto. Derfor brukes vanligvis en hovedkonto til å kreditere den periodiske avskrivningen i balansen. En motkonto er en konto i resultatdelen av kontoplanen.

## <a name="depreciation-adjustment"></a>Avskrivningsjustering
Vanligvis posteres kun en korrigering til en postert avskrivningstransaksjon som en avskrivningsjustering. Derfor konfigureres både hovedkontoen og motkontoen på samme måte som avskrivningskontoen. En avskrivningsjustering kan være et positivt eller negativt beløp, men funksjonaliteten for hovedkontoen (som en balansekonto) og motkontoen (vanligvis som en resultatkonto) er den samme.

## <a name="extraordinary-depreciation"></a>Ekstraordinær avskrivning
Ekstraordinær avskrivning fungerer som grunnleggende avskrivning. Derfor brukes en hovedkonto til å kreditere avskrivningsbeløpet i balansen og redusere verdien til anleggsmidlet. En motkonto er en resultatkonto, der avskrivningen som beregnes for regnskapsperioden, kostnadsføres som en utgift. 

Ekstraordinær avskrivning fungerer uavhengig av grunnleggende avskrivning. Når du har ekstraordinær avskrivning som en separat transaksjonstype, kan du postere og rapportere den ekstraordinære avskrivningen separat fra den vanlige, grunnleggende avskrivningen.

## <a name="special-depreciation-allowance"></a>Særskilte avskrivningsfradrag
Du kan bruke særskilte avskrivningsfradrag til å ta ekstra avskrivningsbeløp første året et anleggsmiddel settes i drift og avskrives. Særskilte avskrivningsfradrag må utføres før alle andre avskrivningsberegninger. Fordi særskilte avskrivningsfradrag ofte er ukjente før senere i levetiden for anleggsmidlet, er det best å bruke denne typen avskrivning i et tablå som ikke posteres til økonomimodulen. Du kan bruke funksjonen Slett transaksjoner som ikke er postert til økonomimodulen, til å slette transaksjonsloggen for disse tablåene. Du kan deretter slette avskrivningsloggen for anleggsmiddeltablået, postere det særskilte avskrivningsfradraget når det er kjent, og deretter postere de gjenværende avskrivningstransaksjonene for året. 

Du kan opprette et ubegrenset antall poster for særskilte avskrivningsfradrag. Når du har tildelt disse postene til et tablå for anleggsmiddelgruppe, brukes de for anleggsmiddeltablået. 

Et særskilt avskrivningsfradrag angis som en prosent eller et fast beløp. Når du posterer avskrivningsforslag, posteres transaksjoner med særskilte avskrivningsfradrag til tablået som transaksjoner som er separate fra avskrivningstransaksjonene.

## <a name="depreciation-calendars"></a> Avskrivningskalendere
Hvert tablå inneholder en kalender som skal brukes ved avskrivning av anleggsmidler. Tablået bruker regnskapskalenderen for finans som standard hvis du ikke angir en kalender for tablået. Du må velge en regnskapskalender for et tablå når avskrivningsprofilen som er knyttet til tablået, bruker et avskrivningsår. 

Du kan opprette delte kalendere ved hjelp av siden **Økonomiske kalendere** i økonomimodulen.

Hvis du vil ha mer informasjon, se [Avskrivningsmetoder og -konvensjoner](depreciation-methods-conventions.md).




