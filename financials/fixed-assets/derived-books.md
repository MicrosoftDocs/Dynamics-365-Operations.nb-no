---
title: "Avledede tablåer"
description: "Denne artikkelen inneholder en oversikt over den avledede tablåfunksjonaliteten."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetBookTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 39035fe2e22987305b2ec6731e5c3b3390043a2a
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="derived-books"></a>Avledede tablåer

[!include[banner](../includes/banner.md)]


Denne artikkelen inneholder en oversikt over den avledede tablåfunksjonaliteten.

Formålet med avledede tablåer er å forenkle postering av anleggsmiddeltablåtransaksjoner som er planlagt for regelmessige intervaller.  Du kan velge ett tablå som det primære tablået. Dette er vanligvis tablået som brukes til regnskapsavskrivning. Du knytter det deretter til de andre tablåene som brukes til å postere transaksjoner i samme intervaller som det primære tablået. Tablåer for avskrivning av skatt brukes ofte som avledede tablåer. 

De vanligste transaksjonene som brukes til å postere til avledede tablåer, er anskaffelse, anskaffelsesjusteringer og anleggsmidler. 

## <a name="example"></a>Eksempel

Tablå B og tablå C er satt opp som avledede tablåer for tablå A for anskaffelsestransaksjonstypen. I tablå A oppgir du en anskaffelsestransaksjon på 1500,00 for anleggsmiddel 123. 

Når transaksjonen er postert, genereres en anskaffelsestransaksjon på 1500,00 som posteres for anleggsmiddel 123 i tablå B, og for anleggsmiddel 123 i tablå C. Når du forbereder transaksjonene for det primære tablået som skal posteres i anleggsmiddeljournalen, kan du også vise og endre transaksjonene til de avledede tablåene. Hvis du forbereder de primære tablåtransaksjonene i en annen journal, vises ikke transaksjonene til den avledede verdien. De posteres imidlertid til de passende kontoene og posteringslagene når du posterer de primære tablåtransaksjonene.

> [!NOTE]                                                                                                                               
> Tablåer som brukes til å postere transaksjoner i intervaller som er forskjellig fra intervallene til det primære tablået, må knyttes til de faste anleggsmidlene som separate tablåer, og ikke som avledede tablåer.  

Hvis du vil ha mer informasjon, kan du se [Postere med avledede tablåer](post-derived-value-models.md).




