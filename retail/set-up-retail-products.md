---
title: Definere detaljprodukter
description: Denne artikkelen beskriver hvordan definerer detaljhandelsprodukter i Microsoft Dynamics 365 for Operations - Retail.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 116c49174989ff14982027cc235640c2ad7322f2
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-retail-products"></a>Definere detaljprodukter

[!include[banner](includes/banner.md)]


Denne artikkelen beskriver hvordan definerer detaljhandelsprodukter i Microsoft Dynamics 365 for Operations - Retail.

Før du kan tilby produkter for videresalg i kanaler for detaljhandel, må du opprette og konfigurere produktene i Dynamics 365 for Operations - Retail. Detaljhandel bruker produktfunksjonene i Dynamics 365 for Operations til å lage produkter for hele organisasjonen i produktstandarden. Du kan opprette produktene, definere produktegenskaper og -attributter og tilordne produktene til detaljhandelskategorihierarkier. Hvis du vil gjøre varene tilgjengelig for kanaler for detaljhandel og legge dem til et aktivt sortiment, må du frigi produkter til juridiske enheter der de er tilgjengelige. Hvis du vil definere produktene som selges ved hjelp av kanaler for detaljhandel, kan du utføre følgende oppgaver.

1.  Definer et detaljprodukthierarki. Ved hjelp av kategorihierarkifunksjonene i Dynamics 365 for Operations kan du definere detaljhandelskategorihierarkier for å gruppere og kategorisere produktene som distribueres til kanaler for detaljhandel. Brukerdefinerte attributter og systemattributter kan defineres på kategorinivå. Deretter arver alle produkter som er tilordnet til kategorien, disse attributtene. Du kan definere flere kategorihierarkier, og hvert produkt kan tilordnes flere hierarkier. Men i et enkelt hierarki kan hvert produkt tilordnes bare én kategori.
2.  Legg til produkter og produktvarianter i produktstandarden. Produkter som er lagt til i produktstandarden, representerer en global liste over produkter. Du kan legge til produkter manuelt, ett om gangen, eller du kan importere produktdata fra leverandører.
3.  Frigi produktene til juridiske enheter. Det er bare produkter som er frigitt til juridiske enheter, som kan gjøres tilgjengelig for detaljhandelskanalene. Når du først definerer et produkt, kan du definere det på et nivå for hele organisasjonen. Du kan deretter velge én eller flere juridiske enheter som produktet skal frigis til. Produktet blir da tilgjengelig for flere kanaler for detaljhandel på tvers av organisasjonen. Du kan bruke denne funksjonen til å opprette et produkt én gang, legge til og oppdatere produktattributter og -egenskaper på ett sted, og deretter distribuere produktet på tvers av organisasjonen, til detaljhandelskanalene hvor det er tilgjengelig.
4.  Legg til produkter i sortimenter. Et sortiment representerer en samling produkter som du tilbyr i kanaler for detaljhandel. Du kan definere ett eller flere sortimenter, og hvert produkt kan tilordnes til ett eller flere sortimenter. Du kan tilordne produkter til kanaler for detaljhandel ved å tilordne sortimentene til disse kanalene for detaljhandel. Når du oppretter et sortiment, kan du legge til produkter som ennå ikke er frigitt til en juridisk enhet. Du må imidlertid frigi produktene til en juridisk enhet før de kan gjøres tilgjengelige for detaljhandelskanalene.
5.  Legge til produkter i navigasjonshierarkier. Før du kan bla gjennom produkter elektronisk eller på et salgssted, må de kategoriseres i et navigasjonshierarki for detaljhandel.
6.  Legg til produkter i kataloger. Selv om dette trinnet er valgfritt for salgssted, krever Internett-butikker at produkter skal inkluderes i minst én katalog.





