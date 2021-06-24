---
title: Aktivere budsjettforslag (forhåndsversjon)
description: Dette emnet forklarer hvordan du aktiverer funksjonen for budsjettforslag i Finance Insights.
author: ShivamPandey-msft
ms.date: 06/03/2021
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
ms.openlocfilehash: 948a3e051e5964c5c773cefd90c8587cf833a450
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222540"
---
# <a name="enable-budget-proposals-preview"></a>Aktivere budsjettforslag (forhåndsversjon)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

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
