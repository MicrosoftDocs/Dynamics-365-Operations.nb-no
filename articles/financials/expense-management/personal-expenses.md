---
title: Personlige utgifter i en reiseregning
description: Dette emnet beskriver to metoder for håndtering av en arbeiders personlige utgifter i Microsoft Dynamics 365 for Finance and Operations.
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
ms.openlocfilehash: b072fa9e78563d3e89b4d60e9ce61473902fee76
ms.sourcegitcommit: ef08bf1258aefb525d56bf85ef19311be26ab94c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/30/2019
ms.locfileid: "1795001"
---
# <a name="personal-expenses-on-an-expense-report"></a>Personlige utgifter i en reiseregningsrapport

[!include [banner](../includes/banner.md)]

På forretningsreise kan det hende at den ansatte belaster personlige utgifter med firmakredittkortet. Hvis du ikke definerer en prosess for håndtering av personlige utgifter, kan godkjenningsprosessen for reiseregning blir avbrutt når den ansatte sender den spesifiserte reiseregningen. 

I Microsoft Dynamics 365 for Finance and Operations finnes to metoder for håndtering av personlige utgifter:

- **Betalt av ansatt** – organisasjonen betaler ikke personlige utgifter som vises på regningen for firmakredittkortet. I stedet opprettes det en rapport som viser personlige utgifter sammen med firmaets utgifter som er belastet firmakredittkortet.
- **Betalt av firma** - firmaet betaler hele regningen som er betalt med firmakredittkortet, og debiterer den ansattes konto for de personlige utgiftene.

Du kan velge metoden som organisasjonen din bruker på siden **Parametere for reiseregning**.
