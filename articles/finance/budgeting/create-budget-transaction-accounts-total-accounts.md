---
title: Opprette et budsjett fra transaksjonskontoer og totalkontoer
description: Denne artikkelen inneholder en oversikt over prosessen for å opprette budsjetter basert på totalkontoer. Den beskriver også hvordan du aktiverer budsjettkontroll for totalkontoer, hvis budsjettkontroll er nødvendig.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: roschlom
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e296118b3b806a5267e29c2b2d4d859c1aea1977
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827392"
---
# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a>Opprette et budsjett fra transaksjonskontoer og totalkontoer

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder en oversikt over prosessen for å opprette budsjetter basert på totalkontoer. Den beskriver også hvordan du aktiverer budsjettkontroll for totalkontoer, hvis budsjettkontroll er nødvendig.

Både dokumenter for budsjettplan og for budsjettregisteroppføring tillater budsjettering på hovedkontoer som har en hovedkonto av typen **Total**. Faktiske beløp kan bare posteres til transaksjonshovedkontoer. 

Når det gjelder den periodiske prosessen **Generer budsjettplan fra økonomimodul**, kan du angi **Total**-hovedkontotypen som et kriterium i **Kilde**-fanen. I dette tilfellet blir hver totalhovedkonto tatt med i målbudsjettplanen, og beløpet svarer til totalbeløpet for de utvalgte hovedkontoene. 

Du kan aktivere budsjettkontroll for hovedkontoer av **Total**-typen. Denne funksjonaliteten støttes gjennom bruk av budsjettgrupper. For hver totalhovedkonto må budsjettet som skal kontrolleres for en budsjettgruppe, opprettes på siden **Budsjettkontrollkonfigurasjon**. Kriteriene du angir, må inneholde totalhovedkontoen og kontoområdet. Hvis du vil opprette budsjettgrupper raskere, kan du bruke dataenheten Budsjettkontrollgrupper. 

Når et budsjett brukes i rapportering, for eksempel i et regnskapsoppgjør, består budsjettsummen for totalkontoen av følgende beløp:

-   Budsjettene som er opprettet fra hver finanskonto for transaksjon, i intervallet til totalkontoen.
-   Budsjettbeløpet som er angitt direkte i totalkontoen

Derfor kan du opprette egne budsjetter for de viktigste transaksjonskontoene i intervallet til totalkontoen og deretter legge til det tilgjengelige budsjettbeløpet i totalkontoen.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]