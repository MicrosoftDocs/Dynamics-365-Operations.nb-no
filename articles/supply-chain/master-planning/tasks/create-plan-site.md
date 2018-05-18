--- 
title: "Opprette en plan for et område"
description: Produksjonsplanleggeren beregner material- og kapasitetsbehovene for produksjonen av en bestemt vare.
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1452c5d6f5dd8d0dd4cb08eb5cc9a48fd8f875f9
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-plan-for-a-site"></a>Opprette en plan for et område

[!include [task guide banner](../../includes/task-guide-banner.md)]

Produksjonsplanleggeren beregner material- og kapasitetsbehovene for produksjonen av en bestemt vare. Når du har opprettet forespørselsforslagene, finner han ordrene på området som han planlegger og bekrefter ordrene, fra de som haster. De viktigste ordrene er de som skal bekreftes på gjeldende dato. Bruk USMF-demodatafirmaet til å utføre disse oppgavene.


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a>Opprette en material- og kapasitetsplan for en vare
1. Klikk Hovedplanlegging.
    * Du må gå til standard instrumentbord.  
2. Klikk Kjør.
3. Utvid delen Poster som skal inkluderes.
4. Klikk Filter.
5. Merk den valgte raden i listen.
6. Skriv inn en verdi i Kriterier-feltet.
    * Eksempel: D0001  
7. Klikk OK.
8. Klikk OK.
    * Dette kan ta noen minutter.  
9. Oppdater siden.

## <a name="identify-the-urgent-planned-orders-for-the-item"></a>Identifisere viktige planlagte bestillinger for varen
1. Åpne kolonnefilter for varenummer.
2. Bruk et filter på feltet "Varenummer" , med verdien "D0001", ved hjelp av filteroperatoren "begynner med".
3. Åpne kolonnefilteret Bestillingsdato.
4. Bruke et filter i feltet "Bestillingsdato" med en verdi for gjeldende dato, ved hjelp av filteroperatoren "er nøyaktig".

## <a name="firm-all-the-urgent-orders-for-the-item"></a>Bekrefte alle viktige bestillinger for varen
1. Merk eller fjern merking for alle rader i listen.
2. Klikk Bekreft.
3. Klikk OK.


