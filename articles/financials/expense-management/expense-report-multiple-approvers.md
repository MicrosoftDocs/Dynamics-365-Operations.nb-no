---
title: Reiseregninger og flere godkjennere
description: Dette emnet gir informasjon om reiseregninger som må godkjennes av flere personer.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d83a473e2e894856c12b36b4d005c6cb06b765a
ms.sourcegitcommit: ef08bf1258aefb525d56bf85ef19311be26ab94c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/30/2019
ms.locfileid: "1795130"
---
# <a name="expense-reports-and-multiple-approvers"></a>Reiseregninger og flere godkjennere

[!include [banner](../includes/banner.md)]

Avhengig av organisasjonens policyer for godkjenning av reiseregninger, kan det være at flere personer må godkjenne en utgiftsrapport som sendes av en ansatt. Når du definerer arbeidsflytprosessen for godkjenning av reiseregninger, kan du legge til arbeidsflytelementer som inneholder oppgaver eller trinn for en eller flere godkjennere av reiseregninger. Du kan for eksempel kreve at alle reiseregninger skal godkjennes først av lederen for den ansatte som sendte regningen og deretter av en leverandørkoordinator.

Hvis du vil kreve flere godkjennere for reiseregninger, kan du legge til arbeidsflytelementene på en av følgende måter:

- Legge til ett godkjenningselement som har ett trinn. Trinnet kan for eksempel kreve at en reiseregning tilordnes til en brukergruppe, og at det skal godkjennes av 50 prosent av brukergruppens medlemmer.
- Legge til ett godkjenningselement som har flere trinn. Godkjenningselementet kan for eksempel inneholde følgende:

    1. Lederen til den ansatte som sendte inn reiseregningen godkjenner regningen.
    2. Regnskapsassistenten kontrollerer kvitteringene og varene som står på reiseregningen.
    3. Budsjetteieren godkjenner reiseregningen.

- Legge til flere godkjenningselementer, der hvert element har ett trinn. Du kan for eksempel legge til et eget godkjenningselement for hvert av følgende trinn:

    1. Lederen til den ansatte godkjenner reiseregningen.
    2. Budsjetteieren godkjenner reiseregningen.
