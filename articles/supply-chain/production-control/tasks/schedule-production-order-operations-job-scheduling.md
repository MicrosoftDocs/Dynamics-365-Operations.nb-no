---
title: Planlegge en produksjonsordre med operasjoner og finplanlegging
description: Denne artikkelen fokuserer på å planlegge en produksjonsordre med grovplanlegging og finplanlegging.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d82d5439e57c02ddc9db4222a946bd15f4ed67e4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903934"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a>Planlegge en produksjonsordre med operasjoner og finplanlegging

[!include [banner](../../includes/banner.md)]

Denne artikkelen fokuserer på å planlegge en produksjonsordre med grovplanlegging og finplanlegging. Ingen jobber opprettes med grovplanlegging, mens jobber opprettes med finplanlegging. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven. Denne fremgangsmåten er ment for produksjonssjef, produksjonsplanlegger eller arbeidsleder som arbeider i et atskilt produksjonsmiljø.


## <a name="create-a-production-order"></a>Opprette en produksjonsordre
1. I navigasjonsruten går du til **Moduler > Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer**.
2. Velg **Ny produksjonsordre**.
3. Angi eller velg en verdi i **Varenummer**-feltet. Velg varenummer **D0001**.  
4. Velg **Opprett**.

## <a name="schedule-operations-for-the-production-order"></a>Planlegge operasjoner for produksjonsordren
1. Merk den nyopprettede raden.      
2. Velg **Planlegg** i handlingsruten.
3. Velg **Planlegg operasjoner**.
4. Velg **Fremover fra planleggingsdato** i **Planleggingsretning**-feltet.
5. Angi en dato i **Planleggingsdato**-feltet. Velg en fremtidig dato, for eksempel i dag pluss én uke. Med den valgte planleggingsretningen, vil produksjonsordren bli planlagt fremover fra denne datoen.  
6. Velg **OK**.
7. Merk den valgte raden i listen. Vær oppmerksom på at statusen endres til **Planlagt**. 
8. Velg **Alle jobber**. Vær oppmerksom på at ingen jobber opprettes med grovplanlegging.  
9. Lukk siden.

## <a name="schedule-jobs-for-the-production-order"></a>Planlegge jobber for produksjonsordren
1. Velg **Planlegg** i handlingsruten.
2. Velg **Planlegg jobber**.
3. Velg **Fremover fra planleggingsdato** i **Planleggingsretning**-feltet.
4. Angi en dato i **Planleggingsdato**-feltet. Velg en fremtidig dato, for eksempel i dag pluss én uke. Med den valgte planleggingsretningen, vil produksjonsordren bli planlagt fremover fra denne datoen.  
5. Velg **OK**.
6. Velg **Produksjonsordre** i handlingsruten.
7. Velg **Alle jobber**. Vær oppmerksom på at basert på den aktive ruten, opprettes fem jobber med finplanlegging.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]