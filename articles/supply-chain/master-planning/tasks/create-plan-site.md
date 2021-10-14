---
title: Opprette en plan for et område
description: Produksjonsplanleggeren beregner material- og kapasitetsbehovene for produksjonen av en bestemt vare.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f7da319d4c28af311d79dc01bb93a9fe2f76480
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568597"
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