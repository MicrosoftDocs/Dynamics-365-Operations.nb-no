---
title: Opprette en konsernintern plan
description: Denne fremgangsmåten viser hvordan du oppretter en konsernintern plan.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 194bb78eed5a673030f7cead031cf286cddbe77c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845215"
---
# <a name="create-an-intercompany-plan"></a>Opprette en konsernintern plan

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

