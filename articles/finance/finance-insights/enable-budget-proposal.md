---
title: Aktivere budsjettforslag
description: Dette emnet forklarer hvordan du aktiverer funksjonen for budsjettforslag i Finance Insights.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: ab65d1b0e366bfe6bdb07688f89d440662165063
ms.sourcegitcommit: 822aea26c5da259efe11ff3b3dc4cf1598425689
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/16/2021
ms.locfileid: "7386492"
---
# <a name="enable-budget-proposals"></a>Aktivere budsjettforslag

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du aktiverer funksjonen for budsjettforslag i Finance Insights.

1. Bruk informasjon fra miljøsiden i Microsoft Dynamics Lifecycle Services (LCS) til å koble til den primære forekomsten av Azure SQL for dette miljøet. Kjør følgende Transact-SQL-kommando (T-SQL) for å aktivere testversjoner for sandkassemiljøet. (Det kan hende at du må aktivere tilgang for IP-adressen din i LCS før du kan koble til Application Object Server \[AOS\] eksternt.)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > Hopp over dette trinnet hvis du bruker versjon 10.0.20 eller nyere, eller hvis du bruker en Service Fabric-distribusjon. Finance Insights-teamet skal allerede ha aktivert testversjonen for deg. Hvis du ikke ser funksjonen i arbeidsområdet **Funksjonsbehandling** eller får problemer når du prøver å aktivere den, kontakter du <fiap@microsoft.com>.

2. Åpne arbeidsområdet **Funksjonsbehandling**, og følg denne fremgangsmåten:

    1. Velg **Se etter oppdateringer**.
    2. Søk etter **Budsjettforslag**, og aktiver denne funksjonen.

3. Gå til **Budsjettering \> Oppsett \> Grunnleggende budsjettering \> Budsjettforslag (forhåndsversjon)**, og velg **Aktiver funksjon**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
