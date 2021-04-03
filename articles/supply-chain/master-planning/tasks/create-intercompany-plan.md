---
title: Opprette en konsernintern plan
description: Denne fremgangsmåten viser hvordan du oppretter en konsernintern plan.
author: ShylaThompson
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5b64ababa618d58feb6095704e5978295060c96f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5261123"
---
# <a name="create-an-intercompany-plan"></a>Opprette en konsernintern plan

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du oppretter en konsernintern plan. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.


## <a name="set-up-an-intercompany-planning-group"></a>Konfigurere en konsernintern planleggingsgruppe 
1. I **navigasjonsruten** går du til **Moduler > Hovedplanlegging >Oppsett > Grupper for konsernintern planlegging**. 
2. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på Navn-feltet med verdien 10.
3. Merk den valgte raden i listen.
4. Klikk på **Slett**. Dette trinnet er nødvendig for å forkorte kjøringen av den konserninterne planleggingen.   Konsernintern planlegging kjører hovedplanlegging i alle selskaper i en planleggingsgruppe, fra den laveste planleggingssekvensen.  
5. Klikk på **Ja**.
6. Lukk siden.

## <a name="create-an-intercompany-plan"></a>Opprette en konsernintern plan
1. I **navigasjonsruten** går du til **Moduler > Hovedplanlegging >Arbeidsområder > Hovedplanlegging**.
2. Klikk på **Konsernintern hovedplanlegging**.  
3. Klikk på rullegardinknappen i feltet **Konsernintern planleggingsgruppe** for å åpne oppslaget.
4. Klikk på koblingen i den valgte raden i listen. Velg konsernintern planleggingsgruppe 10.  
5. Angi 2 i feltet **Antall konserninterne planleggingsgjentakelser.**. Konsernintern planleggingsgruppe 10 har to medlemmer. For å overføre forsinkelsene fra kildefirmaet (USMF) til kunden (DEMF), må du kjøre konsernintern i begge firmaene to ganger. Den første gjentakelsen vil overføre behovet og identifisere forsinkelsene i kildeselskapet (USMF). Den andre gjentakelsen vil overføre forsinkelsene fra USMF til DEMF.  
6. Velg Ny generering i feltet **Første gjentakelse**.
7. Velg Ny generering i feltet **Etterfølgende gjentakelser**.
8. Angi et tall i feltet **Antall tråder**. Dette representerer antall parallelle tråder som brukes til planlegging.  
9. Klikk på **OK**.

## <a name="view-the-result-of-the-plan"></a>Vise resultatet av planen
1. Klikk på rullegardinknappen i **Plan**-feltet for å åpne oppslaget.
2. Klikk på koblingen i den valgte raden i listen. Klikk på koblingen for StaticPlan. Du må være i selskapet USMF.  
3. Klikk på **Planlagte bestillinger**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]