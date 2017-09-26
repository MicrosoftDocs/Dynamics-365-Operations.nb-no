--- 
title: Opprette en konsernintern plan
description: "Denne fremgangsmåten viser hvordan du oppretter en konsernintern plan."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 7c7f466add55fb9a24c3fb8f1f92df712a8622e3
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="create-an-intercompany-plan"></a>Opprette en konsernintern plan

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du oppretter en konsernintern plan. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.


## <a name="set-up-an-intercompany-planning-group"></a>Konfigurere en konsernintern planleggingsgruppe 
1. Gå til konserninterne planleggingsgrupper.
    * Hovedplanlegging > Oppsett > Konserninterne planleggingsgrupper  
2. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på Navn-feltet med verdien 10.
3. Merk den valgte raden i listen.
4. Klikk Slett.
    * Dette trinnet er nødvendig for å forkorte kjøringen av den konserninterne planleggingen.   Konsernintern planlegging kjører hovedplanlegging i alle selskaper i en planleggingsgruppe, fra den laveste planleggingssekvensen.  
5. Klikk Ja.
6. Lukk siden.

## <a name="create-an-intercompany-plan"></a>Opprette en konsernintern plan
1. Klikk Konsernintern hovedplanlegging.
    * Dette er i Hovedplanlegging-arbeidsområdet.  
2. Klikk rullegardinknappen i feltet Konsernintern planleggingsgruppe for å åpne oppslaget.
3. Klikk koblingen i den valgte raden i listen.
    * Velg konsernintern planleggingsgruppe 10.  
4. Angi 2 i feltet Antall konserninterne planleggingsgjentakelser.
    * Konsernintern planleggingsgruppe 10 har to medlemmer. For å overføre forsinkelsene fra kildefirmaet (USMF) til kunden (DEMF), må du kjøre konsernintern i begge firmaene to ganger. Den første gjentakelsen vil overføre behovet og identifisere forsinkelsene i kildeselskapet (USMF). Den andre gjentakelsen vil overføre forsinkelsene fra USMF til DEMF.  
5. Velg et alternativ i feltet Første gjentakelse.
6. Velg Ny generering i feltet Første gjentakelse.
7. Velg Ny generering i feltet Etterfølgende gjentakelser.
8. Angi et tall i feltet Antall tråder.
    * Dette representerer antall parallelle tråder som brukes til planlegging.  
9. Klikk OK.

## <a name="view-the-result-of-the-plan"></a>Vise resultatet av planen
1. Klikk rullegardinknappen i Plan-feltet for å åpne oppslaget.
2. Klikk koblingen i den valgte raden i listen.
    * Klikk koblingen for StaticPlan. Du må være i selskapet USMF.  
3. Klikk Planlagte bestillinger.


