---
title: Opprette et budsjett fra transaksjonskontoer og totalkontoer
description: "Denne artikkelen inneholder en oversikt over prosessen for å opprette budsjetter basert på totalkontoer. Den beskriver også hvordan du aktiverer budsjettkontroll for totalkontoer, hvis budsjettkontroll er nødvendig."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 89ddb0f246eb1d874ff0f2b5305f30355905c45e
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a>Opprette et budsjett fra transaksjonskontoer og totalkontoer

[!include[banner](../includes/banner.md)]


Denne artikkelen inneholder en oversikt over prosessen for å opprette budsjetter basert på totalkontoer. Den beskriver også hvordan du aktiverer budsjettkontroll for totalkontoer, hvis budsjettkontroll er nødvendig.

Både dokumenter for budsjettplan og for budsjettregisteroppføring tillater budsjettering på hovedkontoer som har en hovedkonto av typen **Total**. Faktiske beløp kan bare posteres til transaksjonshovedkontoer. 

Når det gjelder den periodiske prosessen **Generer budsjettplan fra økonomimodul**, kan du angi **Total**-hovedkontotypen som et kriterium i **Kilde**-fanen. I dette tilfellet blir hver totalhovedkonto tatt med i målbudsjettplanen, og beløpet svarer til totalbeløpet for de utvalgte hovedkontoene. 

Du kan aktivere budsjettkontroll for hovedkontoer av **Total**-typen. Denne funksjonaliteten støttes gjennom bruk av budsjettgrupper. For hver totalhovedkonto må budsjettet som skal kontrolleres for en budsjettgruppe, opprettes på siden **Budsjettkontrollkonfigurasjon**. Kriteriene du angir, må inneholde totalhovedkontoen og kontoområdet. Hvis du vil opprette budsjettgrupper raskere, kan du bruke dataenheten Budsjettkontrollgrupper. 

Når et budsjett brukes i rapportering, for eksempel i et regnskapsoppgjør, består budsjettsummen for totalkontoen av følgende beløp:

-   Budsjettene som er opprettet fra hver finanskonto for transaksjon, i intervallet til totalkontoen.
-   Budsjettbeløpet som er angitt direkte i totalkontoen

Derfor kan du opprette egne budsjetter for de viktigste transaksjonskontoene i intervallet til totalkontoen og deretter legge til det tilgjengelige budsjettbeløpet i totalkontoen.




