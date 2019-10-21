---
title: Personlige utgifter i en reiseregning
description: Dette emnet beskriver to metoder for håndtering av en arbeiders personlige utgifter i Microsoft Dynamics 365 Finance.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 825b6c131c8a65b99d5b7ebdadcd6389886f2d11
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179213"
---
# <a name="personal-expenses-on-an-expense-report"></a>Personlige utgifter i en reiseregningsrapport

[!include [banner](../includes/banner.md)]

På forretningsreise kan det hende at den ansatte belaster personlige utgifter med firmakredittkortet. Hvis du ikke definerer en prosess for håndtering av personlige utgifter, kan godkjenningsprosessen for reiseregning blir avbrutt når den ansatte sender den spesifiserte reiseregningen. 

Det finnes to metoder for håndtering av personlige utgifter:

- **Betalt av ansatt** – organisasjonen betaler ikke personlige utgifter som vises på regningen for firmakredittkortet. I stedet opprettes det en rapport som viser personlige utgifter sammen med firmaets utgifter som er belastet firmakredittkortet.
- **Betalt av firma** - firmaet betaler hele regningen som er betalt med firmakredittkortet, og debiterer den ansattes konto for de personlige utgiftene.

Du kan velge metoden som organisasjonen din bruker på siden **Parametere for reiseregning**.
