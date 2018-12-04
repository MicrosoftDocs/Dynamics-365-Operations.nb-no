--- 
title: Planlegge en produksjonsordre med operasjoner og finplanlegging
description: "Denne fremgangsmåten fokuserer på å planlegge en produksjonsordre med grovplanlegging og finplanlegging."
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d4aac437876862e9f776264fc81f246c820bdf45
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a>Planlegge en produksjonsordre med operasjoner og finplanlegging

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten fokuserer på å planlegge en produksjonsordre med grovplanlegging og finplanlegging. Ingen jobber opprettes med grovplanlegging, mens jobber opprettes med finplanlegging. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven. Denne fremgangsmåten er ment for produksjonssjef, produksjonsplanlegger eller arbeidsleder som arbeider i et atskilt produksjonsmiljø.


## <a name="create-a-production-order"></a>Opprette en produksjonsordre
1. Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.
2. Klikk Ny produksjonsordre.
3. Angi eller velg en verdi i Varenummer-feltet.
    * Velg varenummer D0001.  
4. Klikk Opprett.

## <a name="schedule-operations-for-the-production-order"></a>Planlegge operasjoner for produksjonsordren
1. Merk den valgte raden i listen.
    * Velg produksjonsordren du nettopp opprettet. Den bør være på toppen av listen.      
2. Klikk Planlegg i handlingsruten.
3. Klikk Planlegg operasjoner.
4. Velg Fremover fra planleggingsdato i Planleggingsretning-feltet.
5. Angi en dato i Planleggingsdato-feltet.
    * Velg en fremtidig dato, for eksempel i dag pluss én uke. Med den valgte planleggingsretningen, vil produksjonsordren bli planlagt fremover fra denne datoen.  
6. Klikk OK.
7. Merk den valgte raden i listen.
    * Vær oppmerksom på at statusen endres til Planlagt.  
8. Klikk koblingen i den valgte raden i listen.
9. Klikk Alle jobber.
    * Vær oppmerksom på at ingen jobber opprettes med grovplanlegging.  
10. Lukk siden.

## <a name="schedule-jobs-for-the-production-order"></a>Planlegge jobber for produksjonsordren
1. Klikk Planlegg i handlingsruten.
2. Klikk Planlegg jobber.
3. Velg Fremover fra planleggingsdato i Planleggingsretning-feltet.
4. Angi en dato i Planleggingsdato-feltet.
    * Velg en fremtidig dato, for eksempel i dag pluss én uke. Med den valgte planleggingsretningen, vil produksjonsordren bli planlagt fremover fra denne datoen.  
5. Klikk OK.
6. Klikk Produksjonsordre i handlingsruten.
7. Klikk Alle jobber.
    * Vær oppmerksom på at basert på den aktive ruten, opprettes fem jobber med finplanlegging.  


