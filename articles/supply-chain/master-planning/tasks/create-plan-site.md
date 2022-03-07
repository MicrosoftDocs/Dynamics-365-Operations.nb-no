---
title: Opprette en plan for et område
description: Produksjonsplanleggeren beregner material- og kapasitetsbehovene for produksjonen av en bestemt vare.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5ac906617d7c10c2c2884636d1b694bb878bb37c9946e873456da59e72f695c2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714312"
---
# <a name="create-a-plan-for-a-site"></a>Opprette en plan for et område

[!include [banner](../../includes/banner.md)]

Produksjonsplanleggeren beregner material- og kapasitetsbehovene for produksjonen av en bestemt vare. Når forespørselsforslagene er opprettet, finner vedkommende ordrene på området som planlegges, og bekrefter ordrene, fra og med de som haster. De viktigste ordrene er de som skal bekreftes på gjeldende dato. Bruk USMF-demodatafirmaet til å utføre disse oppgavene.


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a>Opprette en material- og kapasitetsplan for en vare
1. Klikk på Hovedplanlegging.
    * Du må gå til standard instrumentbord.  
2. Klikk på Kjør.
3. Utvid delen Poster som skal inkluderes.
4. Klikk på Filter.
5. Merk den valgte raden i listen.
6. Skriv inn en verdi i Kriterier-feltet.
    * Eksempel: D0001  
7. Klikk på OK.
8. Klikk på OK.
    * Dette kan ta noen minutter.  
9. Oppdater siden.

## <a name="identify-the-urgent-planned-orders-for-the-item"></a>Identifisere viktige planlagte bestillinger for varen
1. Åpne kolonnefilter for varenummer.
2. Bruk et filter på feltet "Varenummer" , med verdien "D0001", ved hjelp av filteroperatoren "begynner med".
3. Åpne kolonnefilteret Bestillingsdato.
4. Bruke et filter i feltet "Bestillingsdato" med en verdi for gjeldende dato, ved hjelp av filteroperatoren "er nøyaktig".

## <a name="firm-all-the-urgent-orders-for-the-item"></a>Bekrefte alle viktige bestillinger for varen
1. Merk eller fjern merking for alle rader i listen.
2. Klikk på Bekreft.
3. Klikk på OK.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]