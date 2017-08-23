--- 
title: "Opprette en tidsplan for et område"
description: "Denne fremgangsmåten viser hvordan du planlegger produksjonsordrer som ennå ikke er startet for et område."
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: a611cb773919284b2bbe55395a7ec2b947d5c0b4
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-schedule-for-a-site"></a>Opprette en tidsplan for et område

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du planlegger produksjonsordrer som ennå ikke er startet for et område.  USMF-demodatafirmaet brukes til å utføre denne prosedyren.


## <a name="identify-production-orders-that-are-not-started"></a>Identifisere produksjonsordrer som ikke er startet
1. Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.
2. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på Område-feltet med verdien 1.
    * 1 representerer et område i USMF. Hvis du ikke bruker USMF, velger du et område fra firmaet ditt.  
3. Åpne kolonnefilteret Status.
4. Bruk et filter på "Status"-feltet, med verdien "Planlagt", ved hjelp av filteroperatoren "er nøyaktig".

## <a name="create-a-schedule"></a>Opprette en tidsplan
1. Merk eller fjern merking for alle rader i listen.
2. Klikk Planlegg i handlingsruten.
3. Klikk Planlegg jobber.
4. Velg Bakover fra leveringsdato i Planleggingsretning-feltet.
5. Velg Nei i Begrenset kapasitet-feltet.
6. Velg Nei i Begrenset materiale-feltet.
7. Klikk OK.
    * Dette kan ta en stund.  

## <a name="view-the-result-of-scheduled-production-orders"></a>Vise resultatet av planlagte produksjonsordrer
1. Merk den valgte raden i listen.
    * Du kan merke en vilkårlig rad.  
2. Klikk Produksjonsordre i handlingsruten.
3. Klikk Alle jobber.
    * På denne siden kan du se listen over jobber. I kategorien Planlegging kan du se start- og sluttdato for en jobb.  
4. Klikk Materialer.
    * På denne siden kan du se det forventede materialforbruket for operasjonene i produksjonsordren og gjeldende tilgjengelig lager.  

