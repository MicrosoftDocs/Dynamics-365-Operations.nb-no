---
title: Opprette en konsernintern plan
description: Denne fremgangsmåten viser hvordan du oppretter en konsernintern plan.
author: t-benebo
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c2486ce6f03d03982a7ae9c43af447923aabfed2
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469568"
---
# <a name="create-an-intercompany-plan"></a>Opprette en konsernintern plan

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du oppretter en konsernintern plan. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.

## <a name="set-up-an-intercompany-planning-group"></a>Konfigurere en konsernintern planleggingsgruppe

1. I **navigasjonsruten** går du til **Moduler > Hovedplanlegging >Oppsett > Grupper for konsernintern planlegging**.
2. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på Navn-feltet med verdien 10.
3. Merk den valgte raden i listen.
4. Velg **Slett**. Dette trinnet er nødvendig for å forkorte kjøringen av den konserninterne planleggingen.   Konsernintern planlegging kjører hovedplanlegging i alle selskaper i en planleggingsgruppe, fra den laveste planleggingssekvensen.  
5. Velg **Ja**.
6. Lukk siden.

## <a name="create-an-intercompany-master-plan"></a>Opprette en konsernintern hovedplan

1. I **navigasjonsruten** går du til **Moduler > Hovedplanlegging >Arbeidsområder > Hovedplanlegging**.
2. Velg **Konsernintern hovedplanlegging**.  
3. Velg rullegardinknappen i feltet **Konsernintern planleggingsgruppe** for å åpne oppslaget.
4. Velg koblingen i den valgte raden i listen. Velg konsernintern planleggingsgruppe 10.  
5. Angi 2 i feltet **Antall konserninterne planleggingsgjentakelser.**. Konsernintern planleggingsgruppe 10 har to medlemmer. For å overføre forsinkelsene fra kildefirmaet (USMF) til kunden (DEMF), må du kjøre konsernintern i begge firmaene to ganger. Den første gjentakelsen vil overføre behovet og identifisere forsinkelsene i kildeselskapet (USMF). Den andre gjentakelsen vil overføre forsinkelsene fra USMF til DEMF.  
6. Velg Ny generering i feltet **Første gjentakelse**.
7. Velg Ny generering i feltet **Etterfølgende gjentakelser**.
8. Angi et tall i feltet **Antall tråder**. Dette representerer antall parallelle tråder som brukes til planlegging.  
9. Velg **OK**.

## <a name="view-the-result-of-the-plan"></a>Vise resultatet av planen

1. Velg rullegardinknappen i **Plan**-feltet for å åpne oppslaget.
2. Velg koblingen i den valgte raden i listen. Velg koblingen for StaticPlan. Du må være i selskapet USMF.  
3. Velg **Planlagte ordrer**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]